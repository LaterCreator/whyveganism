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
    <h1>Dairy</h1>
    <div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%;">
        <iframe 
            src="https://drive.google.com/file/d/1CBEONkl0h0BEoGLVi_Cq06dQssbLzvhM/preview" 
            frameborder="0" 
            allowfullscreen 
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
        </iframe>
    </div>
    <br><p></p>
     <ul>
   <li><a href="https://animalsaustralia.org/our-work/farmed-animals/what-happens-to-dairy-calves/" target="_blank" rel="noopener noreferrer">Everything you need to know about dairy</a></li>
    <li><a href="https://www.kinderworld.org/videos/dairy-industry/shooting-baby-calves-dairy-horrors/" target="_blank" rel="noopener norefferrer">Fate of "Bobby Calfs"</a></li>
    </ul>
    <h1>Eggs</h1>
    <div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%;">
        <iframe 
            src="https://drive.google.com/file/d/1X5zYk6hZIfOdSpOPTRcgvBhmoI2NGfcT/preview" 
            frameborder="0" 
            allowfullscreen 
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
        </iframe>
    </div>
  </div> <!-- Closed div for Ethical Reasons -->

  <div id="Health" class="tab-content">
    <h2>Health Reasons</h2>
    <p>The cool thing about veganism is that you are not only acting in a way that coincides with your ethical values, you also benefit from it health-wise.</p>

    <h1>Sources:</h1>
    <ul>
      <li><a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4991921/" target="_blank" rel="noopener noreferrer">Health benefits</a></li>
      <li><a href="https://pubmed.ncbi.nlm.nih.gov/38032644/" target="_blank" rel="noopener noreferrer">Twin study</a></li>
      <li><a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6790443/" target="_blank" rel="noopener noreferrer">Eggs</a></li>
      <li><a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8210981/" target="_blank" rel="noopener noreferrer">Another study</a></li>
    </ul>
    <h1>Documentaries</h1>
    <li><a href="https://www.youtube.com/watch?v=EjTWFoqLy34&t=2152s" target="_blank" rel="noopener noreferrer">Forks over knives</a></li>
   <li><a href="https://www.youtube.com/watch?v=obx7cJtk3fE&t=2817s" target="_blank" rel="noopener noreferrer">What the health</a></li>
  </div>

  <div id="Sustainability" class="tab-content">  
    <h2>Sustainability Reasons</h2>

    <h1>Impacts of animal agriculture on climate change</h1>


  <h2>How are they connected?</h2>

<p>Animal agriculture is one of the main driver's of climate change, the impact of that industry on the planet's health is often downplayed, because the industry has such far reaching power and influence on every level of society, but especially politics. Here I would just like to recommend a really great documentary that helped me understand this issue much better: <a href="https://www.youtube.com/watch?v=LaPge01NQTQ" target="_blank" rel="noopener noreferrer">eating2extinction</a>
</p>

<br><p>To get a grasp on the full impact of this industry on the climate there are multiple important factors to take into consideration. I highlighted Methanes instantenous GWP, because using methanes impact over a 100 year scale takes away its actual impact. The oceans store heat so the immediate impact this gas has is essential.</p>
<p>These are the ressources I can recommend:</p>
<br><strong><li><a href="https://climate.mit.edu/ask-mit/what-makes-methane-more-potent-greenhouse-gas-carbon-dioxide" target="_blank" rel="noopener noreferrer">Methane's instantenous GWP</a></li></strong>
<br><strong><li><a href="https://climate.nasa.gov/vital-signs/ocean-warming/?intent=121" target="_blank" rel="noopener noreferrer">Ocean warming</a></li></strong>
<br><strong><li><a href="https://ourworldindata.org/carbon-opportunity-costs-food" target="_blank" rel="noopener noreferrer">Carbon opportunity cost of food</a></li></strong>
<br><strong><li><a href="https://ourworldindata.org/agricultural-land-by-global-diets#:~:text=Livestock%20takes%20up%20nearly%2080,required%20to%20produce%20our%20food." target="_blank" rel="noopener noreferrer">Where do humans get most of their calories?</a></li></strong>
<br><strong><li><a href="https://www.surgeactivism.org/animalagsubsidiesexplained" target="_blank" rel="noopener noreferrer">how are animal prodcuts so cheap?</a></li></strong>


    <h2>How much CO2 has already been released, how much is released a year and what are the planet's reserves?</h2>
    <p>
        <a href="https://informationisbeautiful.net/visualizations/how-many-gigatons-of-co2/" target="_blank" rel="noopener noreferrer">CO2-Statistics</a>
    </p>

    <h2>What greenhouse gases exist, what is their GWP and what are the causes? <strong>(Global Warming Potential)</strong></h2>
  
    <p>     
<br><a href="https://ourworldindata.org/emissions-by-sector#agriculture-forestry-and-land-use-18-4" target="_blank" rel="noopener noreferrer">Emissions by sector</a>
<br><a href="https://ourworldindata.org/greenhouse-gas-emissions" target="_blank" rel="noopener noreferrer">Greenhouse gases comparison</a>
    </p>

    <h2>If CO2 stays in the atmosphere for potentially thousands of years and we are emitting more CO2 every year, what can we do?</h2>
    <p>We need time to reduce the emissions, time to change our societies, time to adapt. This time can be gained by simply abstaining from animal products that hurt you, the planet, and most importantly the victims.</p>
    <p>
        What can you and I do about a most likely catastrophic future? Are you the kind of person that puts their trust in the people in power (politicians, large corporations, shady governmental institutions, etc.)? Or do you look at it with skepticism and desire for finding out what you can do right now to do your part in the most important social movement of human history? It is important to realize that the industry is only destroying the planet because of an accumulation of individual decisions. More comfort, faster everything, better everything, shinier everything, consume, consume, consume. It would be inconceivable to even bring up the thought of consequences because that might reduce the profit. Corporations need that number to go up, no matter the cost, no matter what.
    </p>
    <p>
        While I am on my ramble let me bring up maybe the worst corporation of all: <strong>Nestle</strong>. Here are five of the probably worst things Nestle has done:
    </p>
    <ul>
        <li>No.1: Causing the death of millions of infants.</li>
        <li>No.2: Child slave labor.</li>
        <li>No.3: Exploiting drought-ridden areas to make a profit (California).</li>
        <li>No.4: Plastic pollution. (Their solution to this is to burn the plastic, nothing can go wrong when you do that, am I right?).</li>
        <li>No.5: Exploiting drought-ridden areas (Pakistan) to not only make a profit, but also wasting half the water and contaminating the groundwater.</li>
    </ul>
    <p>
        Great job, Nestle! So how is it possible that Nestle still exists and is to this day one of the biggest corporations in Europe? <strong>Manipulation :)</strong>
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

    // Simulate a click on the first tab button to display the first tab by default
    document.addEventListener("DOMContentLoaded", function() {
      document.querySelector(".tab-button").click();
    });
  </script>
</body>
</html>
