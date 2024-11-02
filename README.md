<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dropdown Menu Interface</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      flex-direction: column;
    }

    /* Dropdown button styling */
    .dropdown {
      position: absolute;
      top: 20px;
      right: 20px;
    }

    .dropdown-button {
      background-color: #007BFF;
      color: white;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }

    /* Dropdown menu styling */
    .dropdown-menu {
      display: none; /* Hidden by default */
      position: absolute;
      top: 50px;
      right: 20px;
      background-color: #f9f9f9;
      box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
      border-radius: 5px;
      overflow: hidden;
      z-index: 1;
    }

    /* Dropdown items */
    .dropdown-menu button {
      width: 100%;
      padding: 12px 16px;
      font-size: 16px;
      color: #333;
      background-color: #f1f1f1;
      border: none;
      text-align: left;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .dropdown-menu button:hover {
      background-color: #ddd;
    }

    /* Tab content styling */
    .tab-content {
      display: none; /* Hidden by default */
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      width: 80%;
      margin-top: 20px;
      text-align: left;
    }

    .tab-content h2 {
      margin-top: 0;
    }
  </style>
</head>
<body>

  <!-- Dropdown menu button -->
  <div class="dropdown">
    <button class="dropdown-button" onclick="toggleDropdown()">Menu</button>
    <div class="dropdown-menu" id="dropdownMenu">
      <button onclick="openTab('Home')">Home</button>
      <button onclick="openTab('Ethics')">Ethics</button>
      <button onclick="openTab('Health')">Health</button>
      <button onclick="openTab('Sustainability')">Sustainability</button>
      <button onclick="openTab('Activism')">How to Activism</button>
    </div>
  </div>

  <!-- Tab content sections -->
  <div id="Home" class="tab-content">
    <h2>Home</h2>
    <p>Welcome to the home section. This is the main overview of the site.</p>
  </div>

  <div id="Ethics" class="tab-content">
    <h2>Ethics</h2>
    <p>Content about ethical reasons for going vegan or plant-based.</p>
  </div>

  <div id="Health" class="tab-content">
    <h2>Health</h2>
    <p>Health benefits of adopting a vegan or plant-based lifestyle.</p>
  </div>

  <div id="Sustainability" class="tab-content">
    <h2>Sustainability</h2>
    <p>Information on sustainability and environmental impact of plant-based diets.</p>
  </div>

  <div id="Activism" class="tab-content">
    <h2>How to Activism</h2>
    <p>Ways to get involved in activism for the plant-based and vegan movement.</p>
  </div>

  <script>
    // Toggle dropdown visibility
    function toggleDropdown() {
      const dropdown = document.getElementById("dropdownMenu");
      dropdown.style.display = dropdown.style.display === "block" ? "none" : "block";
    }

    // Function to open a specific tab
    function openTab(tabName) {
      // Hide dropdown
      document.getElementById("dropdownMenu").style.display = "none";

      // Hide all tab contents
      const tabContents = document.querySelectorAll(".tab-content");
      tabContents.forEach(content => content.style.display = "none");

      // Show the selected tab
      document.getElementById(tabName).style.display = "block";
    }

    // Close the dropdown if the user clicks outside
    document.addEventListener("click", function(event) {
      const dropdown = document.getElementById("dropdownMenu");
      const dropdownButton = document.querySelector(".dropdown-button");

      if (!dropdown.contains(event.target) && event.target !== dropdownButton) {
        dropdown.style.display = "none";
      }
    });
  </script>
</body>
</html>
