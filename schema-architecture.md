

This spring boot project use and MVC with REST controllers. The Thymeleaf templates are the selected option to create the view of the administration, dashboards and diferent type of data needed. Java with Spring boot is handling the backend of the app creating, modifing, deleting and reading the information stored in the databases, those databases are Mysql and MongoDB. The main functions for the user will be creating appointments, patient dashboards and patient records this interactions will be handled for the REST APIs who will interact with MongoDb using JPA Document structures. For the doctors dashboards and the Administration the Thymeleaf controllers will be managing the intractions with the MySql db using JPA entities to normalize the relational schema.



1. User accesses to the AdminDashBoard or Appointment
2. User action is routed to the appropiate path Thymeleaf or REST controller.
3. The controller call the service layer to apply the bussines logic.
4. The service logic use the repository layer to manage data and make queries.
5. The repository access the database to complete the transaction requested.
6. Entity (relational) or Document (MongoDB) returned, mapped back to DTO/model.
7. The MVC models are passed to the Thymeleaf templates to be displayed in the browser or the REST APIs serializes the JSON and displays the information.