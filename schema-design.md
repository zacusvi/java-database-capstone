## MySQL Database Desing

### Table: admin
- id: INT, Primary key, Auto Increment
- name: VARCHAR(255), not null
- email: VARCHAR(255), not null, not repeat
- password: VARCHAR(255), not null
- creation_date: TIMESTAMP

### Table: doctor
- id: INT, Primary key, Auto Increment
- name: VARCHAR(255), not null
- email: VARCHAR(255), not null, not repeat
- password: VARCHAR(255), not null
- phone: VARCHAR(255), 
- speciality: VARCHAR(255)
- creation_date: TIMESTAMP

### Table: patient
- id: INT,Primary key, Auto Increment
- name: VARCHAR(255), not null
- email: VARCHAR(255), not null
- password: VARCHAR(255), not null
- creation_date: TIMESTAMP

### Table: appointment
- id: INT,Primary key, Auto Increment
- doctor_id: INT, foreign key -> doctor(id), not null
- patient_id: INT, foreign key -> patient(id), not null 
- status: INT
- appointment_date: TIMESTAMP, not null
- creation_date: TIMESTAMP, not null

### Table: appointment_slot
- id: INT, Primary key, Auto Increment
- slot_date: DATE, not null
- start_time: TIME
- end_time: TIME 
- doctor_id_ INT, foreign key -> doctor(id)
- status: INT, not null


## MongoDB Collection Design

### Collection: prescriptions

```json
{
  "id": "ObjectId('64abc123456')",
  "patientName": "John Smith",
  "appointmentId": 51,
  "medication": "Paracetamol",
  "dosage": "500mg",
  "notes": "Take 1 tablet every 6 hours.",
  "refillCount": 2,
  "pharmacy": {
    "name": "Walgreens SF",
    "location": "Market Street"
  }
}
```

### Collection: feedback

```json
{
    "id":"ObjectId('64abc123456')",
    "idAppointment": 556,
    "description":"The doctor is good and kind",
    "rate":5,
    "suggestions":"Better music for the waiting room"    
}

```

### Collection: logs

```json
{
    "id":"ObjectId('64abc123456')",
    "appointmentId":112,
    "pattientName":"Jane doe",
    "patientId":613,
    "doctorId":15,
    "appmntSummary"{
        "symptoms":"Shes tired, feel painful, shes sleepy at work",
        "heartRate":"78ppm",
        "termperature":"100f"
        }
}
```
