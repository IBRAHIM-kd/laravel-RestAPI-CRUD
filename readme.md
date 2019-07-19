STEPS TO RUN THIS PROJECT ----

Installation steps

Follow the bellow steps to install and set up the application.

Step 1: Download the Application

Step 2: Configure the Application

After you have download this project folder the project need to be set up by following commands-

In terminal go to your project directory and Run

  composer install 

Then copy the .env.example file to .env file in the project root folder

Edit the .env file and fill all required data for the below variables

  APP_URL=http://localhost //your application domain URL go here

  DB_HOST=127.0.0.1 // Your DB host IP. Here we are assumed it to be local host
  DB_PORT=3306 //Port if you are using except the default
  DB_DATABASE=name_of_your_database
  DB_USERNAME=db_user_name
  DB_PASSWORD=db_password

Create all the necessary tables need for the application by runing the below command.

  php artisan migrate

Fill default data if your need by running below command.

  php artisan db:seed

Thats all! The application is configured now.

Than run ---  $ php artisan serve | to start the Application server http://localhost:8000/api/employees | I used POSTMAN CLIENT TO TEST MY ENDPOINT.

API Endpoints and Routes

Laravel follows the Model View Controller (MVC) pattern I have creatd models associated with each resource. You can check in the routes/api.php file for all the routes that map to controllers in order to send out JSON data that make requests to our API.

Bellow are the all resources API endpoints -

GET request, you can send it through this URL:
http://localhost:8000/api/employees

POST request, you can send it through this URL:
http://localhost:8000/api/employee?emp_name=ibrahim&salary=25000&job=webdeveloper

PUT request, you can send it through this URL:
http://localhost:8000/api/employee/1?emp_name=abdullahi&salary=30000&job=webdeveloper

DELETE request, you can send it through this URL:
http://localhost:8000/api/employee/1