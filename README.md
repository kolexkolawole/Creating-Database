# DESCRIPTION
# Creating-Database
PHP and MySQL-userAuthMySQL-2


# TASK:

With the provided code skeleton inside userAuthMySQL folder, your task is to complete the following files

- ## `database`

 You are going the work on the database your had in the previous task called zuriphp which contains the following columns

  -  Id,  Full_names,  Country,  Email, Gender,  password

- import the sql file called users.sql to have some initial users in your database for testing `this is incase you had not done that before`

Task `1` Database Connection

 Inside the classes folder and the `Dbh` file,

 - create a class called `Dbh.php` with the following properties

   - hostname,  username, password, dbname

   All of the above should have initial values set which are the default credentials of your database for [hostname, username, password and database name respectively]

 - create a method called `connect()` which is set to protected visibility and creates a connection to the database  and returns the connection

- Task `2` UserAuthentication Logic Class

 Inside the classes Folder In the `UserAuth.php` file

 - import the `Dbh` class

 - Create a classes called UserAuth which has the following

   - Extends (Inherits from) the Dbh class

   - Contains the following properties by name

     - db [set to Private]

   - Has a constructor as such

     public function __construct(){

       $this->db = new Dbh();

     }

   - Has the following methods

     - `validatePassword($password, $confirmPassword)`: Takes in the two passwords passed from the form and checks if they are equal(If equal return true) else returns false

     - `checkEmailExist($email)`

       Checks if User Exist by email, this will be user later by the register method, returns true if user with email=$email exist, else returns false

     - `register($fullname, $email, $password, $confirmPassword, $country, $gender)`

 Register the User based on the `full names, email, country, gender and password`.

     - `login($email, $password)`

       Takes in the email and passwords and logs the user in if credentials are correct,

if so, set Session to `email ` and redirect the user to the dashboard else it redirects the user back to the login page

     - `updateUser($username, $password)` Updates User Password (This will first called the checkEmailExist method). if useremailExist then update the password and redirect to the login page, else redirect to password reset page

     - `deleteUser($id)` Deletes A User By the id.this method deletes the user with the given email from the button on the front-end (the button name is ‘email’ you can access it within the post array when the button is pressed

- Task `3` Router Logic File

 Inside the classes folder the the `Route.php` file

 - create a class called `FormController` which extends the `UserAuth` class with the following properties

   -  `fullname;`

   -  `email`;

   -  `password;`

   -  `confirmPassword;`

   -  `country;`

   -  `gender;`

 - create a constructor that instantiates a new Dbh class (same a constructor created earlier)

 - create a method called handle form and paste in the following code

 This simplifies the routing for you so that you concentrate on the other tasks above,

 Take Your time, read the task over and over till you understand it before attempting, you are free to create meetings to discuss this.

 good luck
TIPS/RESOURCES: 
How To Create A OOP PHP Login System For Beginners | OOP PHP & PDO | OOP PHP Tutorial
ZURI PHP_2022
OOP PHP OFFICIAL DOCUMENTATION
CODEBASE SKELETON

UserAuthOOPMYSQL.zip
