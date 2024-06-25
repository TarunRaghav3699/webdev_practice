# webdev_practice
In this i will practice about our web dev practice questions

1. **What attribute specifies the URL of an external script file in HTML?**
   ```html
   <script src="script.js"></script>
   ```

2. **Which CSS property is used to create space around elements, outside of any defined borders?**
   ```css
   margin: 10px;
   ```

3. **In JavaScript, what keyword is used to declare a block-scoped local variable?**
   ```javascript
   let variableName;
   ```

4. **What is the term used for adjusting content to fit different screen sizes in CSS?**
   ```css
   Responsive Design
   ```

5. **What is the JavaScript method used to periodically execute a function at specified intervals?**
   ```javascript
   setInterval(function, interval);
   ```

6. **State one function of Django as a high-level Python web framework.**
   ```python
   Handling web requests and responses.
   ```

7. **What is the Git command that shows the commit logs?**
   ```bash
   git log
   ```

8. **Match the following: Branching, Pull Request, Clone with their descriptions.**
   - **Branching:** Creating a separate line of development.
   - **Pull Request:** Requesting to merge changes from one branch to another.
   - **Clone:** Copying a repository to a local machine.

9. **What are Django models used for?**
   ```python
   Defining the structure of the database tables.
   ```

10. **What addresses security concerns related to unauthorized actions performed by a user on a web application in Django?**
    ```python
    CSRF (Cross-Site Request Forgery) protection.
    ```

11. **What are the advanced Python features used for adding functionality to existing functions and creating anonymous functions?**
    ```python
    Decorators and Lambda functions.
    ```

12. **What is the purpose of Bootstrap?**
    ```html
    To design responsive and mobile-first web pages.
    ```

13. **Write the syntax for a Lambda function in Python.**
    ```python
    lambda arguments: expression
    ```

14. **What is the function of SASS in web development?**
    ```css
    To provide advanced CSS features like variables, nesting, and mixins.
    ```

15. **What are event listeners in JavaScript?**
    ```javascript
    Functions that wait for an event to occur and then execute a specified function.
    ```

16. **Match the following: DOM, Event Handlers, Django with their descriptions.**
    - **DOM:** The Document Object Model, a representation of the HTML structure.
    - **Event Handlers:** Functions that are triggered by user actions or events.
    - **Django:** A high-level Python web framework.

17. **Describe the Python decorator @staticmethod and provide an example.**
    ```python
    class MyClass:
        @staticmethod
        def my_static_method():
            print("This is a static method.")
    ```

18. **Describe the Python decorator @classmethod and provide an example.**
    ```python
    class MyClass:
        @classmethod
        def my_class_method(cls):
            print("This is a class method.")
    ```

19. **Explain the Model-View-Template (MVT) architecture in Django with examples for each component.**
    - **Model:** Defines the database schema.
    ```python
    from django.db import models

    class Book(models.Model):
        title = models.CharField(max_length=100)
        author = models.CharField(max_length=100)
    ```
    - **View:** Handles the logic and processes user requests.
    ```python
    from django.shortcuts import render
    from .models import Book

    def book_list(request):
        books = Book.objects.all()
        return render(request, 'book_list.html', {'books': books})
    ```
    - **Template:** Defines the HTML structure.
    ```html
    <!-- book_list.html -->
    <h1>Book List</h1>
    <ul>
      {% for book in books %}
        <li>{{ book.title }} by {{ book.author }}</li>
      {% endfor %}
    </ul>
    ```

20. **Design a responsive login page using HTML and CSS. Include the code and explain how the design is responsive.**
    ```html
    <!-- login.html -->
    <html>
    <head>
      <style>
        body {
          font-family: Arial, sans-serif;
          background-color: #f2f2f2;
          display: flex;
          justify-content: center;
          align-items: center;
          height: 100vh;
        }
        .login-container {
          background-color: white;
          padding: 20px;
          border-radius: 10px;
          box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
          width: 300px;
        }
        .login-container input[type="text"], .login-container input[type="password"] {
          width: 100%;
          padding: 10px;
          margin: 10px 0;
          border: 1px solid #ccc;
          border-radius: 5px;
        }
        .login-container button {
          width: 100%;
          padding: 10px;
          background-color: #4CAF50;
          color: white;
          border: none;
          border-radius: 5px;
          cursor: pointer;
        }
        .login-container button:hover {
          background-color: #45a049;
        }
      </style>
    </head>
    <body>
      <div class="login-container">
        <form>
          <label for="username">Username:</label>
          <input type="text" id="username" name="username">
          <label for="password">Password:</label>
          <input type="password" id="password" name="password">
          <button type="submit">Login</button>
        </form>
      </div>
    </body>
    </html>
    ```
    The design is responsive due to the use of `flex` properties in the CSS, ensuring the login form is centered regardless of the screen size.

21. **Write a JavaScript function to manipulate DOM elements to show/hide content based on user clicks. Provide HTML and JavaScript code.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <style>
        .content {
          display: none;
        }
      </style>
    </head>
    <body>
      <button onclick="toggleContent()">Show/Hide Content</button>
      <div id="content" class="content">
        This is the content to be toggled.
      </div>
      <script>
        function toggleContent() {
          var content = document.getElementById('content');
          if (content.style.display === 'none') {
            content.style.display = 'block';
          } else {
            content.style.display = 'none';
          }
        }
      </script>
    </body>
    </html>
    ```

22. **Explain the use and syntax of JOIN queries in SQL and provide an example combining user and order data from two tables.**
    ```sql
    SELECT users.name, orders.order_id
    FROM users
    JOIN orders ON users.user_id = orders.user_id;
    ```

23. **Describe the role of indexing in databases and demonstrate with SQL code how indexing can improve query performance.**
    ```sql
    CREATE INDEX idx_user_id ON users(user_id);
    ```
    Indexing improves query performance by allowing faster retrieval of rows from a table based on the indexed column.

24. **Write HTML and CSS code to create a web page layout that includes a header, a three-column content section, and a footer using CSS Flexbox or Grid. Ensure the layout is responsive.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <style>
        body {
          display: flex;
          flex-direction: column;
          min-height: 100vh;
          margin: 0;
        }
        header, footer {
          background: #333;
          color: white;
          padding: 1rem;
          text-align: center;
        }
        .content {
          flex: 1;
          display: flex;
          flex-wrap: wrap;
        }
        .content > div {
          flex: 1;
          min-width: 300px;
          padding: 1rem;
          box-sizing: border-box;
        }
      </style>
    </head>
    <body>
      <header>Header</header>
      <div class="content">
        <div>Column 1</div>
        <div>Column 2</div>
        <div>Column 3</div>
      </div>
      <footer>Footer</footer>
    </body>
    </html>
    ```

25. **Write a regular JavaScript function that represents an object and call the function. Provide an example using an arrow function.**
    ```javascript
    // Regular function
    function createObject(name, age) {
      return {
        name: name,
        age: age
      };
    }

    let person = createObject('John', 30);
    console.log(person);

    // Arrow function
    const createObjectArrow = (name, age) => ({ name, age });

    let personArrow = createObjectArrow('Jane', 25);
    console.log(personArrow);
    ```

26. **Code a simple web page layout that includes a header, footer, sidebar, and main content area using CSS Grid and Flexbox. Ensure it

 is responsive.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <style>
        body {
          display: grid;
          grid-template-areas: 
            'header header header'
            'sidebar main main'
            'footer footer footer';
          grid-template-rows: auto 1fr auto;
          grid-template-columns: 200px 1fr 1fr;
          height: 100vh;
          margin: 0;
        }
        header {
          grid-area: header;
          background: #333;
          color: white;
          text-align: center;
          padding: 1rem;
        }
        footer {
          grid-area: footer;
          background: #333;
          color: white;
          text-align: center;
          padding: 1rem;
        }
        .sidebar {
          grid-area: sidebar;
          background: #f4f4f4;
          padding: 1rem;
        }
        .main {
          grid-area: main;
          padding: 1rem;
        }
      </style>
    </head>
    <body>
      <header>Header</header>
      <div class="sidebar">Sidebar</div>
      <div class="main">Main Content</div>
      <footer>Footer</footer>
    </body>
    </html>
    ```

27. **Develop a Django application to manage a bookstore, including models for books, authors, and publishers. Show how to use Django admin to manage these models.**
    ```python
    # models.py
    from django.db import models

    class Publisher(models.Model):
        name = models.CharField(max_length=100)

    class Author(models.Model):
        name = models.CharField(max_length=100)

    class Book(models.Model):
        title = models.CharField(max_length=100)
        author = models.ForeignKey(Author, on_delete=models.CASCADE)
        publisher = models.ForeignKey(Publisher, on_delete=models.CASCADE)

    # admin.py
    from django.contrib import admin
    from .models import Book, Author, Publisher

    admin.site.register(Book)
    admin.site.register(Author)
    admin.site.register(Publisher)
    ```

28. **Implement a full-stack web application feature using Django and JavaScript:**
    - **Backend: Create a Django view to handle form data submitted for a new user registration. Include the view and URL configuration code.**
    ```python
    # views.py
    from django.shortcuts import render, redirect
    from django.http import HttpResponse
    from .forms import RegistrationForm

    def register(request):
        if request.method == 'POST':
            form = RegistrationForm(request.POST)
            if form.is_valid():
                form.save()
                return HttpResponse('Registration successful')
        else:
            form = RegistrationForm()
        return render(request, 'register.html', {'form': form})

    # urls.py
    from django.urls import path
    from . import views

    urlpatterns = [
        path('register/', views.register, name='register'),
    ]
    ```

    - **Frontend: Write JavaScript code to validate the user registration form data on the client side before submission. Include HTML form and JavaScript validation code.**
    ```html
    <!-- register.html -->
    <html>
    <head>
      <script>
        function validateForm() {
          var username = document.forms["registration"]["username"].value;
          var password = document.forms["registration"]["password"].value;
          if (username == "" || password == "") {
            alert("Username and Password must be filled out");
            return false;
          }
          return true;
        }
      </script>
    </head>
    <body>
      <form name="registration" action="/register/" method="post" onsubmit="return validateForm()">
        {% csrf_token %}
        <label for="username">Username:</label>
        <input type="text" id="username" name="username">
        <label for="password">Password:</label>
        <input type="password" id="password" name="password">
        <button type="submit">Register</button>
      </form>
    </body>
    </html>
    ```

29. **Implement a simple currency converter using HTML forms, JavaScript, and local storage. Provide all code and explain how local storage is used to store the conversion rate.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <script>
        function convertCurrency() {
          var rate = localStorage.getItem('conversionRate');
          if (!rate) {
            rate = 74.85; // Example conversion rate
            localStorage.setItem('conversionRate', rate);
          }
          var amount = document.getElementById('amount').value;
          var result = amount * rate;
          document.getElementById('result').innerText = result;
        }
      </script>
    </head>
    <body>
      <h1>Currency Converter</h1>
      <form>
        <label for="amount">Amount in USD:</label>
        <input type="text" id="amount">
        <button type="button" onclick="convertCurrency()">Convert</button>
      </form>
      <p>Amount in INR: <span id="result"></span></p>
    </body>
    </html>
    ```

30. **Write a program to access student IDs from a database using Callback, Promises, and Async-Await. Identify the differences in using these processes.**
    ```javascript
    // Using Callbacks
    function getStudentIDs(callback) {
      setTimeout(() => {
        callback([1, 2, 3, 4]);
      }, 1000);
    }

    getStudentIDs((ids) => {
      console.log('Callback:', ids);
    });

    // Using Promises
    function getStudentIDsPromise() {
      return new Promise((resolve) => {
        setTimeout(() => {
          resolve([1, 2, 3, 4]);
        }, 1000);
      });
    }

    getStudentIDsPromise().then((ids) => {
      console.log('Promise:', ids);
    });

    // Using Async-Await
    async function getStudentIDsAsync() {
      const ids = await getStudentIDsPromise();
      console.log('Async-Await:', ids);
    }

    getStudentIDsAsync();
    ```

31. **Create a dynamic to-do list application using HTML, CSS, and JavaScript. The application should allow users to add, remove, and mark tasks as completed. Provide all code.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <style>
        .completed {
          text-decoration: line-through;
        }
      </style>
      <script>
        function addTask() {
          var task = document.getElementById('task').value;
          if (task === '') return;
          var ul = document.getElementById('taskList');
          var li = document.createElement('li');
          li.appendChild(document.createTextNode(task));
          li.onclick = function () {
            this.classList.toggle('completed');
          };
          ul.appendChild(li);
          document.getElementById('task').value = '';
        }
        function clearTasks() {
          document.getElementById('taskList').innerHTML = '';
        }
      </script>
    </head>
    <body>
      <h1>To-Do List</h1>
      <input type="text" id="task">
      <button onclick="addTask()">Add</button>
      <button onclick="clearTasks()">Clear</button>
      <ul id="taskList"></ul>
    </body>
    </html>
    ```

32. **Develop a Django web application that includes a form for user registration. Use Django forms to validate input data and display success or error messages.**
    ```python
    # forms.py
    from django import forms
    from django.contrib.auth.models import User

    class RegistrationForm(forms.ModelForm):
        password = forms.CharField(widget=forms.PasswordInput)

        class Meta:
            model = User
            fields = ['username', 'password']

    # views.py
    from django.shortcuts import render, redirect
    from .forms import RegistrationForm

    def register(request):
        if request.method == 'POST':
            form = RegistrationForm(request.POST)
            if form.is_valid():
                form.save()
                return render(request, 'register.html', {'success': True})
        else:
            form = RegistrationForm()
        return render(request, 'register.html', {'form': form})

    # register.html
    <html>
    <body>
      <h1>Register</h1>
      {% if success %}
        <p>Registration successful!</p>
      {% else %}
        <form method="post">
          {% csrf_token %}
          {{ form.as_p }}
          <button type="submit">Register</button>
        </form>
      {% endif %}
    </body>
    </html>
    ```

33. **Write a Python script to demonstrate the use of decorators in Django.**
    ```python
    # decorators.py
    from django.http import HttpResponse

    def my_decorator(view_func):
        def _wrapped_view(request, *args, **kwargs):
            return HttpResponse("This is a decorated response")
        return _wrapped_view

    # views.py
    from django.shortcuts import render
    from .decorators import my_decorator

    @my_decorator
    def my_view(request):
        return render(request, 'my_view.html')
    ```

34. **Create a responsive navigation bar using HTML and CSS.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <style>


        body {
          font-family: Arial, sans-serif;
        }
        .navbar {
          display: flex;
          background-color: #333;
        }
        .navbar a {
          color: white;
          padding: 14px 20px;
          text-decoration: none;
          text-align: center;
        }
        .navbar a:hover {
          background-color: #ddd;
          color: black;
        }
        .navbar .icon {
          display: none;
        }
        @media screen and (max-width: 600px) {
          .navbar a:not(:first-child) {display: none;}
          .navbar a.icon {
            float: right;
            display: block;
          }
        }
        @media screen and (max-width: 600px) {
          .navbar.responsive {position: relative;}
          .navbar.responsive .icon {
            position: absolute;
            right: 0;
            top: 0;
          }
          .navbar.responsive a {
            float: none;
            display: block;
            text-align: left;
          }
        }
      </style>
    </head>
    <body>
      <div class="navbar" id="myNavbar">
        <a href="#home">Home</a>
        <a href="#news">News</a>
        <a href="#contact">Contact</a>
        <a href="javascript:void(0);" class="icon" onclick="myFunction()">&#9776;</a>
      </div>
      <script>
        function myFunction() {
          var x = document.getElementById("myNavbar");
          if (x.className === "navbar") {
            x.className += " responsive";
          } else {
            x.className = "navbar";
          }
        }
      </script>
    </body>
    </html>
    ```

35. **Explain how JavaScript event delegation works with an example.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <script>
        document.addEventListener('DOMContentLoaded', (event) => {
          document.getElementById('parent').addEventListener('click', (e) => {
            if (e.target && e.target.nodeName === 'LI') {
              alert('List item ' + e.target.innerText + ' clicked');
            }
          });
        });
      </script>
    </head>
    <body>
      <ul id="parent">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
      </ul>
    </body>
    </html>
    ```

36. **Implement a Django REST API endpoint and demonstrate how to consume it using JavaScript.**
    - **Django REST API Endpoint**
    ```python
    # serializers.py
    from rest_framework import serializers
    from .models import Book

    class BookSerializer(serializers.ModelSerializer):
        class Meta:
            model = Book
            fields = '__all__'

    # views.py
    from rest_framework import viewsets
    from .models import Book
    from .serializers import BookSerializer

    class BookViewSet(viewsets.ModelViewSet):
        queryset = Book.objects.all()
        serializer_class = BookSerializer

    # urls.py
    from django.urls import path, include
    from rest_framework.routers import DefaultRouter
    from .views import BookViewSet

    router = DefaultRouter()
    router.register(r'books', BookViewSet)

    urlpatterns = [
        path('', include(router.urls)),
    ]
    ```

    - **JavaScript to Consume the API**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <script>
        async function fetchBooks() {
          let response = await fetch('http://127.0.0.1:8000/books/');
          let data = await response.json();
          let bookList = document.getElementById('bookList');
          data.forEach(book => {
            let li = document.createElement('li');
            li.textContent = book.title;
            bookList.appendChild(li);
          });
        }
      </script>
    </head>
    <body onload="fetchBooks()">
      <h1>Book List</h1>
      <ul id="bookList"></ul>
    </body>
    </html>
    ```

37. **Develop a web page that uses AJAX to load data dynamically from a server.**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <script>
        function loadData() {
          var xhr = new XMLHttpRequest();
          xhr.onreadystatechange = function () {
            if (this.readyState == 4 && this.status == 200) {
              document.getElementById("data").innerHTML = this.responseText;
            }
          };
          xhr.open("GET", "data.txt", true);
          xhr.send();
        }
      </script>
    </head>
    <body>
      <h1>Dynamic Data Loading</h1>
      <button type="button" onclick="loadData()">Load Data</button>
      <div id="data"></div>
    </body>
    </html>
    ```

38. **Create a JavaScript module and demonstrate its use in a web application.**
    - **Module File (math.js)**
    ```javascript
    export function add(a, b) {
      return a + b;
    }

    export function subtract(a, b) {
      return a - b;
    }
    ```

    - **Main File (index.html)**
    ```html
    <!-- index.html -->
    <html>
    <head>
      <script type="module">
        import { add, subtract } from './math.js';
        console.log('Add:', add(2, 3));
        console.log('Subtract:', subtract(5, 3));
      </script>
    </head>
    <body>
      <h1>JavaScript Modules</h1>
    </body>
    </html>
    ```

39. **Explain the use of middleware in Django with an example.**
    ```python
    # middleware.py
    from django.utils.deprecation import MiddlewareMixin

    class SimpleMiddleware(MiddlewareMixin):
        def process_request(self, request):
            print("Request URL:", request.path)

    # settings.py
    MIDDLEWARE = [
        'django.middleware.security.SecurityMiddleware',
        'django.contrib.sessions.middleware.SessionMiddleware',
        'django.middleware.common.CommonMiddleware',
        'django.middleware.csrf.CsrfViewMiddleware',
        'django.contrib.auth.middleware.AuthenticationMiddleware',
        'django.contrib.messages.middleware.MessageMiddleware',
        'django.middleware.clickjacking.XFrameOptionsMiddleware',
        'myapp.middleware.SimpleMiddleware',
    ]
    ```

40. **Write a SQL query to demonstrate the use of subqueries and nested queries.**
    ```sql
    -- Find customers who have made more than one order
    SELECT customer_id, COUNT(order_id) AS order_count
    FROM orders
    GROUP BY customer_id
    HAVING COUNT(order_id) > 1;

    -- Find products that have never been ordered
    SELECT product_id, product_name
    FROM products
    WHERE product_id NOT IN (SELECT product_id FROM order_details);
    ```

41. **Explain the concept of context managers in Python with an example.**
    ```python
    # Using context manager with 'with' statement
    with open('file.txt', 'w') as file:
        file.write('Hello, world!')

    # Custom context manager
    class MyContextManager:
        def __enter__(self):
            print("Entering the context")
            return self

        def __exit__(self, exc_type, exc_val, exc_tb):
            print("Exiting the context")

    with MyContextManager() as cm:
        print("Inside the context")
    ```

42. **Describe the process of setting up a virtual environment in Python and its importance.**
    ```bash
    # Create a virtual environment
    python -m venv myenv

    # Activate the virtual environment (Windows)
    myenv\Scripts\activate

    # Activate the virtual environment (Unix or MacOS)
    source myenv/bin/activate

    # Install packages in the virtual environment
    pip install django

    # Importance: 
    # - Isolates project dependencies
    # - Avoids version conflicts
    # - Simplifies dependency management
    ```

43. **Write a JavaScript function to filter and sort an array of objects.**
    ```javascript
    const products = [
      { name: 'Laptop', price: 1000 },
      { name: 'Phone', price: 500 },
      { name: 'Tablet', price: 700 }
    ];

    // Filter products above a certain price
    const filteredProducts = products.filter(product => product.price > 600);

    // Sort products by price in ascending order
    const sortedProducts = filteredProducts.sort((a, b) => a.price - b.price);

    console.log(sortedProducts);
    ```

44. **Create a Django custom template filter and demonstrate its use.**
    ```python
    # templatetags/custom_filters.py
    from django import template

    register = template.Library()

    @register.filter(name='multiply')
    def multiply(value, arg):
        return value * arg

    # settings.py
    INSTALLED_APPS = [
        # ...
        'myapp.templatetags.custom_filters',
    ]

    # template.html
    {% load custom_filters %}
    {{ 3|multiply:2 }}  {# Outputs: 6 #}
    ```

45. **Discuss the differences between synchronous and asynchronous programming in JavaScript.**
    - **S

ynchronous Programming**
      - Code is executed in sequence.
      - Blocking: each operation must complete before the next one starts.
      - Example:
        ```javascript
        console.log('Start');
        console.log('Middle');
        console.log('End');
        ```

    - **Asynchronous Programming**
      - Code execution can be paused and resumed.
      - Non-blocking: operations can run concurrently.
      - Example:
        ```javascript
        console.log('Start');
        setTimeout(() => console.log('Middle'), 1000);
        console.log('End');
        ```

46. **Implement a Python function to read a CSV file and return data as a list of dictionaries.**
    ```python
    import csv

    def read_csv(file_path):
        with open(file_path, mode='r') as file:
            csv_reader = csv.DictReader(file)
            return list(csv_reader)

    data = read_csv('data.csv')
    print(data)
    ```

47. **Explain the concept of closures in JavaScript with an example.**
    ```javascript
    function outerFunction() {
      let outerVariable = 'I am outside!';

      function innerFunction() {
        console.log(outerVariable);
      }

      return innerFunction;
    }

    const closure = outerFunction();
    closure(); // Outputs: 'I am outside!'
    ```

48. **Create a Django model with custom validation.**
    ```python
    from django.db import models
    from django.core.exceptions import ValidationError

    def validate_positive(value):
        if value < 0:
            raise ValidationError('Value must be positive')

    class Product(models.Model):
        name = models.CharField(max_length=100)
        price = models.DecimalField(max_digits=10, decimal_places=2, validators=[validate_positive])
    ```

49. **Write a Python script to send an email with an attachment.**
    ```python
    import smtplib
    from email.mime.multipart import MIMEMultipart
    from email.mime.text import MIMEText
    from email.mime.base import MIMEBase
    from email import encoders

    def send_email(subject, body, to_email, attachment_path):
        from_email = 'your_email@example.com'
        password = 'your_password'

        # Create the email
        msg = MIMEMultipart()
        msg['From'] = from_email
        msg['To'] = to_email
        msg['Subject'] = subject

        # Attach the body
        msg.attach(MIMEText(body, 'plain'))

        # Attach the file
        attachment = open(attachment_path, 'rb')
        part = MIMEBase('application', 'octet-stream')
        part.set_payload(attachment.read())
        encoders.encode_base64(part)
        part.add_header('Content-Disposition', f'attachment; filename={attachment_path}')
        msg.attach(part)

        # Send the email
        server = smtplib.SMTP('smtp.example.com', 587)
        server.starttls()
        server.login(from_email, password)
        server.sendmail(from_email, to_email, msg.as_string())
        server.quit()

    send_email('Subject', 'Email body', 'to_email@example.com', 'file.txt')
    ```

50. **Explain the Model-View-Controller (MVC) architecture with an example in Django.**
    - **Model:** Represents the data structure. In Django, this is typically a class inheriting from `models.Model`.
      ```python
      from django.db import models

      class Book(models.Model):
          title = models.CharField(max_length=100)
          author = models.CharField(max_length=100)
      ```

    - **View:** Handles the request and returns the response. In Django, views are functions or classes.
      ```python
      from django.shortcuts import render
      from .models import Book

      def book_list(request):
          books = Book.objects.all()
          return render(request, 'book_list.html', {'books': books})
      ```

    - **Controller:** Manages the relationship between the model and the view. In Django, this is handled by the framework itself through URL routing and view handling.

    - **URL Configuration:**
      ```python
      from django.urls import path
      from . import views

      urlpatterns = [
          path('books/', views.book_list, name='book_list'),
      ]
      ```

    - **Template:**
      ```html
      <!-- book_list.html -->
      <html>
      <body>
        <h1>Book List</h1>
        <ul>
          {% for book in books %}
            <li>{{ book.title }} by {{ book.author }}</li>
          {% endfor %}
        </ul>
      </body>
      </html>
      ```