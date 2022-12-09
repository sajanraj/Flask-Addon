
 Assaignment 1 - Design Student Form with name details and submit to backend server. From backend server process student data and sent a response with student name.
 
 ![alt text](https://github.com/sajanraj/Flask-Addon/blob/f031b0483f60f4c6bc054b87291609d4a7731032/static/images/Request%20Response.png)


# serving html page to specific path

      Frontend- html,css,js
      Backend -python, Flask

Creating a student card with html page frontend and submit the data to backend server. 

## ExampleDomain.com/student


### Step 1:
Open Editor in cloud console

Add header 

      from flask import request
      
add path for specifica page in your app's  .py file
Create a path/url student in flask app

            @app.route('/student',,methods=['GET','POST']) 
            def  student_page_response():
            if request.method == GET:
              return render_template('student.html')
            else:
              name = request.form[‘fname’]
              return render_template(welcome.html',name=name)



### Step 2:


Create a text file with extension .html - student.html

Dir structure

          /templates
            /student.html
            /welcome.html
          …
          …
          hello.py

Add contents in html page 

All HTML documents must start with a document type declaration:
 <!DOCTYPE html>.
The HTML document itself begins with <html> and ends with </html>.
student.html

        <!DOCTYPE html>
        <html>
        <head>
        <title>Page Title</title>
        <!-- Add css and header files here -->
        </head>
        <body>

        <h1>My First Heading</h1>
        <p>My first paragraph.</p>

        <form action="/student_process" method="post">

          <label for="fname">First name:</label><br>

          <input type="text" id="fname" name="fname"><br>

          <label for="lname">Last name:</label><br>

          <input type="text" id="lname" name="lname">

        </form>

        </body>
        <!-- Add js and footer files here -->
        </html>


Welcome.html


        <!DOCTYPE html>
        <html>
        <head>
        <title>Page Title</title>
        <!-- Add css and header files here -->
        </head>
        <body>

        <h1>{{name}}</h1>

        <p> Welcome</p>


        </body>
        <!-- Add js and footer files here -->
        </html>
        
### Step 3:
In cloud console
            # Run Flask app using
            cd /Flask-Addon
            python hello.py
### Step 3:

Use the web preview and add port 5000 to view page in gcloud platform





