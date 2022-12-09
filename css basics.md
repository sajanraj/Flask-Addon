# CSS
Within header
### Internal  CSS

        <style>
        body {
          background-color: lightblue;
        }

        h1 {
          color: white;
          text-align: center;
        }
        </style>
### External CSS

Within header

    <link rel="stylesheet" href="mystyle.css">
    
then create mystyle.css file to import it from a file

### Inline CSS

    <p style="color:red;">This is a paragraph.</p>

#### Using class

    <style>
    p.one {
      border-style: solid;
      border-width: 5px 20px; /* 5px top and bottom, 20px on the sides */
    }

    .newcolor{
    Color:red;
    }

    </style>

<p class="one">Some text.</p>
<p class="newcolor">New Colour.</p>
