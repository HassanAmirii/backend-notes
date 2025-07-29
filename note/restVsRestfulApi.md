### REST VS RESTFUL API

##### RESTFUL

REST as in (Representational state transfer) is an architectural style for designing APIs. It makes use of the http methods, such as GET, POST, DELETE etc, as standard in communicating between softwares

##### RESTFUL API

On the other resful api is a mode of interacting with different softwares using the REST standard.

- It organizes data into resources such _students_ below
- Each resources has a unique URL (end point)
- The HTTP method you use defines the action (create, read, update, or delete).

eg

GET /students # Fetch students
POST /students # Add a student
GET /students/1 # Fetch student with ID 1
PUT /students/1 # Update student with ID 1
DELETE /students/1 # Delete student with ID 1
