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
    }

    .plant-button {
      background-color: transparent;
      background-image ('[https://imgs.search.brave.com/1OjHTKaILaXkxp7qI7oJkFasa5NsFKd1KhdgqCpKCA4/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly90My5m/dGNkbi5uZXQvanBn/LzA1LzQ4LzY4Lzc4/LzM2MF9GXzU0ODY4/NzgyNF9LV3pjSW1U/QnNxenBWakdRdUEz/SjZuRW1nYW5tWnly/WC5qcGc]')
      background-size: contain;
      background-repeat: no-repeat;
      width: 50px;
      height: 50px;
      border: none;
      cursor: pointer;
      margin-top: 20px;
    }

    .dropdown-menu {
      display: none;
      position: absolute;
      top: 80px; /* Position below the plant button */
      background-color: #f9f9f9;
      border: 1px solid #ccc;
      padding: 10px;
      border-radius: 5px;
      box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
      z-index: 1;
    }

    .dropdown-menu button {
      display: block;
      width: 100%;
      padding: 8px 12px;
      font-size: 16px;
      background-color: #f1f1f1;
      border: none;
      text-align: left;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .dropdown-menu button:hover {
      background-color: #ddd;
    }

    .tab-content {
      display: none;
      padding: 20px;
      border: 1px solid #ccc;
      border-top: none;
      width: 80%;
      margin-top: 20px;
    }

    .tab-content h2 {
      margin-top: 0;
    }
  </style>
</head>
<body>
  <button class="plant-button" onclick="toggleDropdown()"></button>

  <div class="dropdown-menu" id="dropdownMenu">
    <button onclick="openTab(event, 'Ethical')">Ethical Reasons</button>
    <button onclick="openTab(event, 'Health')">Health Reasons</button>
    <button onclick="openTab(event, 'Sustainability')">Sustainability Reasons</button>
    <button onclick="openTab(event, 'Activism')">How to Become an Activist</button>
  </div>

  <div id="Ethical" class="tab-content">
    <h2>Ethical Reasons</h2>
    <!-- Content here... -->
  </div>

  <div id="Health" class="tab-content">
    <h2>Health Reasons</h2>
    <!-- Content here... -->
  </div>

  <div id="Sustainability" class="tab-content">
    <h2>Sustainability Reasons</h2>
    <!-- Content here... -->
  </div>

  <div id="Activism" class="tab-content">
    <h2>How to Become an Activist</h2>
    <p>Explore ways to support animal welfare and climate justice...</p>
  </div>

  <script>
    function toggleDropdown() {
      const dropdown = document.getElementById("dropdownMenu");
      dropdown.style.display = dropdown.style.display === "block" ? "none" : "block";
    }

    function openTab(evt, tabName) {
      // Close the dropdown
      document.getElementById("dropdownMenu").style.display = "none";

      // Hide all tab content
      const tabContent = document.getElementsByClassName("tab-content");
      for (let i = 0; i < tabContent.length; i++) {
        tabContent[i].style.display = "none";
      }

      // Show the selected tab content
      document.getElementById(tabName).style.display = "block";
    }

    // Close dropdown when clicking outside of it
    document.addEventListener("click", function(event) {
      const dropdown = document.getElementById("dropdownMenu");
      const plantButton = document.querySelector(".plant-button");

      if (!dropdown.contains(event.target) && event.target !== plantButton) {
        dropdown.style.display = "none";
      }
    });

    // Show the first tab content by default
    document.addEventListener("DOMContentLoaded", function() {
      openTab(event, 'Ethical');
    });
  </script>
</body>
</html>
