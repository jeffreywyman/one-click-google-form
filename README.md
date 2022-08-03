## Convert Your Pre-Filled Link Into A Single-Click Submission


<html>
  <head>
    <title>One Click Google Form Submission</title>
    <style>
.tooltip {
  position: relative;
  display: inline-block;
}

.tooltip .tooltiptext {
  visibility: hidden;
  width: 140px;
  background-color: #555;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 5px;
  position: absolute;
  z-index: 1;
  bottom: 150%;
  left: 50%;
  margin-left: -75px;
  opacity: 0;
  transition: opacity 0.3s;
}

.tooltip .tooltiptext::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: #555 transparent transparent transparent;
}

.tooltip:hover .tooltiptext {
  visibility: visible;
  opacity: 1;
}
</style>
  </head>
  <body>
    <p></p>
    <input type="text" placeholder="Paste URL Here" id="inputId">
    <button type="button" onclick="getInputValue();">Get Value</button>
    <div id="my_field">Result</div>
<div class="tooltip">
<button onclick="myFunction()" onmouseout="outFunc()">
  <span class="tooltiptext" id="myTooltip">Copy to clipboard</span>
  Copy text
  </button>
</div>
    <script>
      function getInputValue() {
        // Selecting the input element and get its value 
        var inputVal = document.getElementById("inputId").value;

        inputVal = inputVal.replace("viewform?", "formResponse?");

        // Displaying the value
        document.getElementById("my_field").innerText = inputVal;
      }
    </script>
    <script>
function myFunction() {
                    var range = document.createRange();
                    range.selectNode(document.getElementById("my_field"));
                    window.getSelection().removeAllRanges(); // clear current selection
                    window.getSelection().addRange(range); // to select text
                    document.execCommand("copy");
                    window.getSelection().removeAllRanges();// to deselect


  
  var tooltip = document.getElementById("myTooltip");
  tooltip.innerHTML = "Copied!;
}

function outFunc() {
  var tooltip = document.getElementById("myTooltip");
  tooltip.innerHTML = "Copy to clipboard";
}
</script>
  </body>
</html>
