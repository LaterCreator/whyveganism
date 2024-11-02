<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tabbed Interface with Dropdown</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 20px;
    }

    /* Plant button */
    .plant-button {
      background-color: transparent;
      background-image: url('https://example.com/plant-icon.png'); /* Replace with actual plant icon URL */
      background-size: cover;
      background-repeat: no-repeat;
      width: 50px;
      height: 50px;
      border: none;
      cursor: pointer;
      margin-bottom: 20px;
    }

    /* Dropdown menu styling */
    .dropdown-menu {
      display: none; /* Hidden by default */
      position: absolute;
      top: 80px; /* Adjusts the position below the button */
      background-color: #f9f9f9;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
      z-index: 1;
    }

    /* Dropdown items */
    .dropdown-menu button {
      display: block;
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
    }

    .tab-content h2 {
      margin-top: 0;
    }
  </style>
</head>
<body>
  <!-- Plant button that triggers dropdown -->
  <button class="plant-button" onclick="toggleDropdown()"></button>

  <!-- Dropdown menu with options -->
  <div class="dropdown-menu" id="dropdownMenu">
    <button onclick="openTab('Ethical')">Ethical Reasons</button>
    <button onclick="openTab('Health')">Health Reasons</button>
    <button onclick="openTab('Sustainability')">Sustainability Reasons</button>
    <button onclick="openTab('Activism')">How to Become an Activist</button>
  </div>

  <!-- Tab content sections -->
  <div id="Ethical" class="tab-content">
    <h2>Ethical Reasons</h2>
    <p>Content about ethical reasons...</p>
  </div>

  <div id="Health" class="tab-content">
    <h2>Health Reasons</h2>
    <p>Content about health reasons...</p>
  </div>

  <div id="Sustainability" class="tab-content">
    <h2>Sustainability Reasons</h2>
    <p>Content about sustainability reasons...</p>
  </div>

  <div id="Activism" class="tab-content">
    <h2>How to Become an Activist</h2>
    <p>Content about activism...</p>
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

    // Close the dropdown if user clicks outside
    document.addEventListener("click", function(event) {
      const dropdown = document.getElementById("dropdownMenu");
      const plantButton = document.querySelector(".plant-button");

      if (!dropdown.contains(event.target) && event.target !== plantButton) {
        dropdown.style.display = "none";
      }
    });
  </script>
</body>
</html>
