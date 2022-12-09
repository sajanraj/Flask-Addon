   JS  - Java Script
    
    
        <!DOCTYPE html>
        <html>
        <body>

        <h2>Making responsive pages using JS</h2>

        <p id="demo">JavaScript can change HTML content.</p>

        <button type="button" onclick="document.getElementById('demo').innerHTML = 'Hello JavaScript!'">Change Text!</button>

        </body>
        </html>
   ### In line- 
   
   Here js will execute onclick property for button type button
          
            onclick="document.getElementById('demo').innerHTML = 'Hello JavaScript!'"
            
   ### Using  script tags
        Exaple for event
        <element event='some JavaScript'>

  
                  <script>
                  document.getElementById("demo").innerHTML = "My First JavaScript";
                  </script>
   ### case 2
   
         in html 

              <button type="button" id="demo">Change Text!</button>
         in script 

              // define id to button          
              var button = document.getElementById("demo");
              button.addEventListener("click",function(e){
                  document.getElementById('demo').innerHTML = 'Hello JavaScript!';
              },false);
      
  ## Declare Variables
  
  - Using var
  - Using let
  - Using const
  - Using nothing
  
        // How to create variables:
        var x;
        let y;
        
use 

      let a, b, c;  // Declare 3 variables
      a = 2;        // Assign the value 2 to a
      b = 8;        // Assign the value 8 to b
      c = a + b;    // Assign the sum of a and b to c
      
 ## comments
 
 Single line command  start with // .
 
 Multi-line comments start with /* and end with */.
 
 ## JavaScript Function Syntax
A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

      function name(parameter1, parameter2, parameter3) {
        // code to be executed
      }
      
  example
  
        function myFunction(a, b) {
        return a * b;
      }
 
Js Object Creation
const car = {type:"Fiat", model:"500", color:"white"}; 
 
 # alert and log
 
    alert(“Let’s go down the first road!”); //open popup window
    console.log(“hi”); // can be visible in js console
