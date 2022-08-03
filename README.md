<html>
  <head>
    <title>One Click Google Form Submission</title>
    <script src="https://cdn.tailwindcss.com"></script>
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

<div class="relative w-full">

    <div>
       <div class="container px-8 md:px-12 xl:max-w-5xl mx-auto lg:px-7 xl:px-0">
           <div class="md:flex md:gap-12 pt-40 lg:py-56">
                <div class="md:w-7/12">
                    <h1 class="text-gray-900 font-bold text-4xl xl:text-5xl">Submit Google Forms with <span class="text-sky-500">one click</span>.</h1>
                    <p class="mt-8 text-gray-700">Transform your pre-filled Google Form link into one that gets submitted automatically when clicked.</p>
                    <div class="md:-mr-32">
                        <form action="" class="w-full mt-12">
                            
<div class=" relative ">
    <input type="text" placeholder="Paste URL Here" id="inputId" class=" rounded-lg border-transparent flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" placeholder="Your email"/>
    </div>


                        </form>
                    </div>
            </div>
        </div> 
    </div>
</div>
                                
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
  tooltip.innerHTML = "Copied!";
}

function outFunc() {
  var tooltip = document.getElementById("myTooltip");
  tooltip.innerHTML = "Copy to clipboard";
}
</script>
  </body>
</html>
