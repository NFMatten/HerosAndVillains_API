# HerosAndVillains_API
<br/>
Main Stories<br/>
<br/>
As a developer, I want to make good, consistent commits.<br/>
<br/>
As a developer, I want to create an ERD with two tables - Super and SuperType.<br/>
&emsp; The two tables should show all of the correct properties for both entities as well as the correct relationship between the two tables.<br/>
<br/>
As a developer, I want to create a SuperType model in a "super_types" app.<br/>
&emsp; Property names must be in snake_case and match the following exactly:<br/>
&emsp; &emsp; type - CharField<br/>
<br/>
As a developer, I want to register the SuperType model with the admin site so I can:<br/>
&emsp; 1. Register a new super user (python manage.py createsuperuser)<br/>
&emsp; 2. Visit the admin site<br/>
&emsp; 3. Seed two values ("Hero" and "Villain") into the "super_type" table<br/>
<br/>
As a developer, I want to create a Super model in a "supers" app. <br/>
&emsp; Property names must be in snake_case and match the following exactly:<br/>
&emsp; &emsp; name - CharField<br/>
&emsp; &emsp; alter_ego - CharField<br/>
&emsp; &emsp; primary_ability - CharField<br/>
&emsp; &emsp; secondary_ability - CharField<br/>
&emsp; &emsp; catchphrase - CharField<br/>
&emsp; &emsp; super_type - ForeignKey<br/>
<br/>
As a developer, I want my API to server the "supers" app's content on the following URL paths:<br/>
&emsp; Paths must match these exactly:
&emsp; '127.0.0.1:8000/api/supers/' - optional params<br/>
&emsp; '127.0.0.1:8000/api/supers/int:pk/'<br/>
<br/>
As a developer, I want to create a GET by id endpoint that does the following things:<br/>
&emsp; Accepts a value from the request's URL (the id of the super to retrieve).<br/>
&emsp; Returns a 200 status code.<br/>
&emsp; Respons with the super in the database that has the id that was sent through the URL.<br/>
<br/>
As a developer, I want to create a POST endpoint that does the following things:<br/>
&emsp; Accepts a body object from the request in the form of a Super model.<br/>
&emsp; Adds the new super to the database.<br/>
&emsp; Returns a 201 status code.<br/>
&emsp; Responds with the newly created super objet.<br/>
<br/>
As a delevoper, I want to create a PUT endpoint that does the following things:<br/>
&emsp; Accepts a value from the request's URL (The id of the super to be updated).<br/>
&emsp; Accepts a body object from the request in the form of a Super model.<br/>
&emsp; Finds the super in the Super table and updates that super with the properties that were sent in the request's body.<br/>
&emsp; Returns a 200 status code.<br/>
&emsp; Responds with the newly updated super object.<br/>
<br/>
As a developer, I want to create a DELETE endpoint that does the following things:<br/>
&emsp; Accepts a value from the request's URL.<br/>
&emsp; Deletes the correct super from the database.<br/>
&emsp; Returns a 204 status code (NO CONTENT).<br/>
<br/>
As a developer, I want to create a GET endpoint that responds with a 200 success status code and all of the supers within the supers table.<br/>
&emsp; This view function should be implemented in a way to accept a "type" parameter.<br/>
&emsp; &emsp; Example: "http://127.0.0.1:8000/api/supers?type=hero"<br/>
&emsp; If a type query parameter is sent to the view function with a value of "hero", the view function response should be a list of all supers that are associated with the type of "Hero".<br/>
&emsp; If a type query parameter is sent to the view function with a value of "villain", the view function response should be a list of all supers that are associated with the type of "Villain".<br/>
&emsp; If no type query parameter is sent, return a custom dictionary response with a "heroes" key set equal to a list of supers of type "Hero" and a "villains" key set equal to a list of supers of type "Villain"<br/>
<br/>
<br/>
Bonus Story:<br/>
<br/>
As a developer, I want to add full CRUD functionality for the "super_type" table within the "super_types" views.py file.