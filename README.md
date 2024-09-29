# LabW5
How to Run Your Django Web App and Access the "Hello World" JSON Response

    Set Up Your Virtual Environment:
        Start by creating a virtual environment for your project. Open your terminal and navigate to your desired project directory. Then run:

        bash

python -m venv venv

Activate the virtual environment:

    For Linux or macOS:

    bash

source venv/bin/activate

For Windows:

bash

        venv\Scripts\activate

Create a Directory for Your Project:

    Navigate to the location where you want to create your Django project:

    bash

    mkdir my_project_directory
    cd my_project_directory

Start Your Django Project:

    Create a new Django project using the following command:

    bash

django-admin startproject my_project

Navigate into your project directory:

bash

    cd my_project

Create a Django App (if needed):

    You may also want to create a Django app to handle your specific functionality:

    bash

    python manage.py startapp my_app

Modify Views:

    In my_app/views.py, create a view that returns a JSON response:

    python

    from django.http import JsonResponse

    def hello_world(request):
        return JsonResponse({"message": "Hello World"})

Configure URLs:

    In my_project/urls.py, include the view you created:

    python

    from django.contrib import admin
    from django.urls import path
    from my_app.views import hello_world

    urlpatterns = [
        path('admin/', admin.site.urls),
        path('hello/', hello_world, name='hello_world'),
    ]

Run the Development Server:

    Start the Django development server by running:

    bash

    python manage.py runserver

    By default, this will start the server at http://127.0.0.1:8000/.

Access the "Hello World" JSON Response:

    Open your web browser and navigate to:

    arduino

http://127.0.0.1:8000/hello/

You should see the JSON response:

json

        {
          "message": "Hello World"
        }

Conclusion

Follow these steps to successfully run your Django web app and access the "Hello World" JSON response in your browser. Feel free to modify the view and URL configurations to suit your needs!
