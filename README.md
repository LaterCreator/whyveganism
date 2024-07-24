<html lang="en">
<head>
<link rel="stylesheet" type="text/css" href="styles.css" />
  <script>function openTab(evt, tabName) {
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
});</script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tabbed Interface</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  {
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
    <p>Here are some sustainability reasons...</p>
  </div>

  <script src="scripts.js"></script>
</body>
</html>
