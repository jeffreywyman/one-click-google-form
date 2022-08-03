## Welcome to GitHub Pages

<!DOCTYPE html>
<html>
  <head>
    <title>Title of the Document</title>
  </head>
  <body>
    <p></p>
    <input type="text" placeholder="Paste your Pre-filled Link Here" id="inputId">
    <button type="button" onclick="getInputValue();">Get Value</button>
    <div id="my_field">test</div>
    <script>
      function getInputValue() {
        // Selecting the input element and get its value 
        var inputVal = document.getElementById("inputId").value;

        inputVal = inputVal.replace("viewform?", "formResponse?");

        // Displaying the value
        document.getElementById("my_field").innerText = inputVal;
      }
    </script>
  </body>
</html>

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
