<h1 align="center">Expense Tracker</h1>
Managing personal finances efficiently has become increasingly important, whether you're saving for a vacation, planning for retirement, or simply trying to stay within a budget, keeping track of expenses is essential. To address this need, I have build an 'Expense Tracker' application using python/Django.

## Project overview
My project 'Expense Tracker' will include the following features:
- User Authentication: Allow users to register, login, and manage their accounts securely.
- Expense Management: Users can add, view, edit, and delete their expenses.
- Expense Categories: Expenses can be categorized for better organization and analysis.
- Responsive Design: Ensure the application is accessible and functional across various devices

## Detailing
To put it simple, I can describe the entire project in seperate segments such as
- Designing the user interface (UI) of the application
- Modeling the Database
- Building the form logic

## Designing the UI
In this part of project, we'll leverage a pre-existing UI created by a designer from CodePen to kickstart the development of our Expense Tracker web application. We'll integrate this UI with our own logic for expense management using Django. This approach allows us to focus on functionality while ensuring a visually appealing and user-friendly interface.
- Step 1: Setting up the project environment by running python-django commands for creating the project and app by specifying names which will create all the dependencies for the project requirements.
- Step 2: Create a templates folder where we will be storing the html file and css file 
- Step 3: I used codepen/io for the html and css templates and later modified and rewritten the code for the necessary UI part of the website and integrated in the project
- step 4: Once integrated I have created the necessary URL's for template rendering for the application
- step 5: Run the server by pushing the command 'python manage.py runserver' open the generated IP  and the ui part will starts to jump on the web.
<p align="center">
  <img src="screenshots/ui part.png" width="35%"/>
</p>

## Modeling the database
In our Expense Tracker project, efficient data modeling is essential to accurately record and manage users' expenses. We'll design a database schema using Django's ORM (Object-Relational Mapping) to represent key entities such as current balance, tracking history, and request logs.

- Step 1: Creating the django models in the django app's models.py file and define the following models Current balance,Tracking History.
- Step 2: Understanding the Models
**Current Balance**
  Represents the current balance of a user. It contains a single field current_balance of type FloatField.
**Trackin History**
  Records the history of expenses. It contains fields such as current_balance (linked to CurrentBalance model), amount, expense_type, description, and created_at.
- Step 3: **Migrations and database sync:** After defining the models, generate and apply migrations to create corresponding database tables by running the following python commands **"python manage.py makemigrations"** and **"python manage.py migrate"**
- Step 4: Admin panel registration: To interact with the defined models in admin interface register them in admin.py file by importin the models and executing the following line "admin.site.register(model name)"
- Step 5 :
  - Views and Template updating:
       -  Open index.html located in the templates directory and add a form to allow users to submit expenses 
  - Define Views to Handle Expense Tracking:
       -  In Django app's views.py, create a view function to handle expense tracking:

once updated you can add the transaction and will see the output in the terminal

To be precise I have used Mysql database hosting in the XAMPP server where the models will be available for the application.
screenshots/trackerhistory table .png
<p align="center">
  <img src="screenshots/trackerhistory table .png" width="70%"/>
  <img src="screenshots/currentbalnce table.png"width="70%"/>
</p>
Here we can see that the model Tracking History and Current Balance are created in the mysql xampp server with necessary columns/fields.



