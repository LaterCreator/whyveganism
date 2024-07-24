<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tabbed Interface</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }

    .tabs {
      display: flex;
      margin-bottom: 20px;
    }

    .tab-button {
      background-color: #f1f1f1;
      border: none;
      outline: none;
      cursor: pointer;
      padding: 14px 16px;
      transition: background-color 0.3s;
      font-size: 17px;
    }

    .tab-button:hover {
      background-color: #ddd;
    }

    .tab-button.active {
      background-color: #ccc;
    }

    .tab-content {
      display: none;
      padding: 20px;
      border: 1px solid #ccc;
      border-top: none;
    }

    .tab-content h2 {
      margin-top: 0;
    }
  </style>
</head>
<body>
  <div class="tabs">
    <button class="tab-button" onclick="openTab(event, 'Ethical')">Ethical Reasons</button>
    <button class="tab-button" onclick="openTab(event, 'Health')">Health Reasons</button>
    <button class="tab-button" onclick="openTab(event, 'Sustainability')">Sustainability Reasons</button>
  </div>

  <div id="Ethical" class="tab-content">
    <h2>Ethical Reasons</h2>
    <p>Here are some ethical reasons...</p>
  </div>

  <div id="Health" class="tab-content">
    <h2>Health Reasons</h2>
    <p>Here are some health reasons...</p>
  </div>

  <div id="Sustainability" class="tab-content">
    <h2>Sustainability Reasons</h2>
    <p><h1>Impacts of animal agriculture on climate change</h1>

<h2>How much CO2 has already been released, how much is released a year and what are the planet's reserves?</h2>

<a href="https://informationisbeautiful.net/visualizations/how-many-gigatons-of-co2/" target="_blank" rel="noopener noreferrer">CO2-Statistics</a>

<h2>What other greenhouse gases exist and what is their GWP? <strong>(Global Warming Potential</strong></h2>
<p>Methane's instantenous GWP is 120 times greater than that of CO2! Since oceans obviously store heat, it's important to remember.</p>

<br><a href="https://climate.mit.edu/ask-mit/what-makes-methane-more-potent-greenhouse-gas-carbon-dioxide" target="_blank" rel="noopener noreferrer">Methane's GWP</a><br>
<br><a href="https://climate.nasa.gov/vital-signs/ocean-warming/?intent=121" target="_blank" rel="noopener noreferrer">Ocean warming</a><br>
<br><a href="https://ourworldindata.org/greenhouse-gas-emissions" target="_blank" rel="noopener noreferrer">Grennhouse gases comparison</a><br>


<h2>If CO2 stays in the atmosphere for potentially thousands of years and we are running out of time, what can we do?</h2>

<p>Now I just want to clarify that I am not a specialist, I do not know everything, well I probably know very little considering the amount of data available. But I do know one thing: <strong>We need time</strong><br>
<br>To understand how we obtain more time there are some important facts to know. Maybe you already know them, maybe you don't but here they are nonetheless<br>
</p>
  </div>

  <script>
    function openTab(evt, tabName) {
      // Declare all variables
      var i, tabcontent, tabbuttons;

      // Get all elements with class="tab-content" and hide them
      tabcontent = document.getElementsByClassName("tab-content");
      for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
      }

      // Get all elements with class="tab-button" and remove the class "active"
      tabbuttons = document.getElementsByClassName("tab-button");
      for (i = 0; i < tabbuttons.length; i++) {
        tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
      }

      // Show the current tab, and add an "active" class to the button that opened the tab
      document.getElementById(tabName).style.display = "block";
      evt.currentTarget.className += " active";
    }

    // By default, open the first tab
    document.addEventListener("DOMContentLoaded", function() {
      document.querySelector('.tab-button').click();
    });
  </script>
</body>
</html>
