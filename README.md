## Convert Your Pre-Filled Link Into A Single-Click Submission


<html>
  <head>
    <title>One Click Google Form Submission</title>
  </head>
  <body>
    <p></p>
    <input type="text" placeholder="Paste URL Here" id="inputId">
    <button type="button" onclick="getInputValue();">Get Value</button>
    <div id="my_field">Result</div>
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
