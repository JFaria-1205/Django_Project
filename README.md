# Django_Project
IS601_Final_Project

*This is the readme for the final project.*

**Includes: Django Stack, HTML, CSS, JavaScript, Python, SQL, Git**

Initial configuration:

setup django environment in vscode using command "python -m venv djangoenv"
activate virtual environment "djangoenv\Scripts\activate" [can deactive this by typing 'deactivate']
install django - "py -m pip install django"
gives version of installed django project - "django-admin --version"
create project "django-admin startproject product-sales"
start server with command "python manage.py runserver". http://127.0.0.1:8000/.
Create App 'python manage.py startapp sales'
Steps for Github workflow:

Pull main branch to get updated changes.
Merge main branch into your branch.
Check merge changes, make sure nothing is broken.
Merge your branch into main branch.
Loading JSON data from file to sqlite db:

create model in models.py and run commands python manage.py makemigrations python manage.py migrate
After the model is created, load data from input_data.json to the Item model. The corresponding code is in sales/management/commands/loadDB.py (python manage.py loadDB)
updating count on cards:

From home.html incCount(id) and decCount(id) to script.js. which inturn makes AJAX(Asynchronous JavaScript and XML) request to django backend without refreshing web page.
the request is handled in views.py to update the count and send a response.
cart page:

shows the image, name and quantity of product along with a delete button at end of each selected element.
delete button will remove element from cart and resets its count to zero.
the submit button at end will redirect to submit page.
