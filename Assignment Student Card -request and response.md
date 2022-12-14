
 Assaignment 1 - Design Student Form with name details and submit to backend server. From backend server process student data and sent a response with student name.
 
 ![alt text](https://github.com/sajanraj/Flask-Addon/blob/f031b0483f60f4c6bc054b87291609d4a7731032/static/images/Request%20Response.png)


# serving html page to specific path

      Frontend- html,css,js
      Backend -python, Flask

Creating a student card with html page as frontend and submit the data in form to backend server.

## ExampleDomain.com/student

### (!! Warning - Do not copy paste- text encoding will be different -[ u+0060 \`] - [u+0027 ']- [u+2018 "] )
### Step 1:
Open Editor in cloud console

Using python Flask API for serving web pages.

Add header 

      # Comments starts with a #, and Python will ignore them:
      # header file to process html request from client 
      from flask import request
      # header used for importing Flask class
      from flask import Flask
      # header used for rendering html page from server side to client
      from flask import render_template
      # creating object using flask class
      app = Flask(__name__)
      
add path for specifica page in your app's  .py file
Create a path/url student in flask app

Eg: domain.com/*student*
 domain.com - This one stands for domain name of the application running in the server
 
 /student - stands for url path
 
 for each path you can serve webpages designed in html.


            @app.route('/student',methods=['GET','POST']) 
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

Add contents in html5 page 

[Reference](https://www.codeproject.com/Articles/546960/HTML5-Quick-Start-Web-Application)
All HTML documents must start with a document type declaration:
 <!DOCTYPE html>.
The HTML document itself begins with \<html\> and ends with \</html\>.
student.html

        <!DOCTYPE html>
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
          
           <input type="submit" Value='Enter'>

        </form>

        </body>
        <!-- Add js and footer files here -->
        </html>


Welcome.html


        <!DOCTYPE html>
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
            
            
            #clone repo from git using
            $ git clone https://github.com/sajanraj/Flask-Addon.git
            # Run Flask app using
            $ cd /Flask-Addon
            $ python hello.py
 help:-
 
     # To see the directry in your path
     $ ls
     # change the current path to the folder listed in your path
     $ cd dir_name
     # dir_name- can be either complete path or folder name listed in your current path
     
### Step 4:

Use the web preview and add port 5000 to view page in gcloud platform





