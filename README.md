Hello, my name is Afsana Tarannum. I am a doctoral student, studying Urban Affairs at the University of Memphis. Currently I am working as a graduate assistant. I earned a Bachelor of Architecture from the University of Asia Pacific and then obtained a master’s degree in Urban and Regional Planning from Bangladesh University of Engineering and Technology. Simultaneously I worked for an architecture firm. Afterward, I moved to the United States, where I completed a master's degree in City and Regional Planning at the University of Memphis and also worked with Self+Tucker Architects. 

I was awared as runner-up at the American Planning Association Student Design Competition in 2023 and also received the Outstanding Student Project Award from the Tennessee Chapter of the American Planning Association in 2023. My research interests are nightlife vitality, age-friendly development, and accessible public space.

---

---

## Education

| Degree                                | Institution                 | Year               |
|:--------------------------------------|:----------------------------|:-------------------|
| PhD in Urban Affairs                  | University of Memphis at TN | (_2024 – Present_) |
| Master of City and Regional Planning  | University of Memphis at TN | (_2022 – 2024_)    |
| Master of Urban and Regional Planning |  BUET at Dhaka              | (_2018 – 2022_)    | 
| Bachelor of Architecture              | UAP at Dhaka                | (_2018 – 2022_)    |

---

## Research Experience
### **‘Night Life Reimagined – Designing Infill Module to Accommodate Positive Nightlife’**

The focus of this research was to identify the positive nighttime activities and places to accommodate positive nightlife activities in the Jackson Planning District. The paper also aimed to create an infill development module to accommodate the positive nightlife identified.

### **‘Momentum in Mason: 2054 Vison Plan’**

Momentum in Mason was a coursework project envisioning Mason’s future. Engagement activities were designed specifically for Mason residents, leading to public meetings and surveys that highlighted common concerns and aspirations. A SWOT analysis and a review of current conditions were conducted to shape the document's Vision Statement, Guiding Principles, Goals, Objectives, and Action Items for Mason’s growth.

### **‘Stanton Step 1: 2045 Vision Plan’**

Stanton Step 1, developed as part of a coursework project, presents a comprehensive vision for Stanton's future based on resident feedback and data analysis. It synthesizes the key issues, ideas, and strategies raised during the planning process, capturing the community's vision for the town. This document aims to guide the upcoming Stanton comprehensive planning process by capturing the community's values and concerns alongside an analysis of current conditions. It serves as a foundation for further planning efforts in anticipation of regional developments.

### **‘The Triangle Plan, Regenerative Healing for the Logan Triangle, Philadelphia’**

The Triangle Plan was a submission to the American Planning Association Student Design Competition, 2023. The plan articulates a physical vision for Philadelphia’s vacant Logan Triangle site which is consistent with the goals and values that Logan residents identified during the 2016 Logan Neighborhood planning process. While the plan primarily serves to illustrate this physical vision, it also offers a series of policy recommendations aimed at making it a reality. Additionally, the plan provides a 10-year phasing strategy, which defines timelines for both physical improvements and the adoption of recommended policies.

### **‘Chattanooga Comprehensive Plan 2030 Review Report’**

The aim of the research was to analyze the quality of the Chattanooga Comprehensive Plan 2030 with the Godschalk (2015) assessment criteria which provided a useful basis for determining the comprehensive quality of the plan. The team members graded the plan according to the criteria individually and combined the ratings as a team to provide a thorough review of the plan's strengths and weaknesses.

### **‘Development of an Age-Friendly Environment Index and its Application on Dhaka City Corporations’**

This research project aimed to develop an evaluation framework to measure the age-friendliness of the built
environment considering the local context and generate an age-friendly map of Dhaka City Corporations.
‘GIS Analysis of Landslide Hazard: A Case Study on Chittagong Division, Bangladesh’
This study, in brief, was undertaken to assess land suitability from a landslide perspective. Obtained findings show that a huge portion of the area is vulnerable to landslides due to unplanned housing settlements and transportation systems.

### **‘Design of a Law-Enforcement Agency Headquarters at Dhaka, Bangladesh’**

Creating a common platform for the community and law enforcement agency was the primary focus of this project. The architectural design and function of the complex was designed in harmony with the existing natural environment.

---

---

## Work Experience
> **Graduate Assistant** (_September, 2024 – Present_) at University of Memphis, Memphis, TN
  
> **Intern Architect** (_May 2023 – August 2024_) at Self+Tucker Architects, Memphis, TN

> **Graduate Assistant** (_September, 2022 – April, 2023_) at University of Memphis, Memphis, TN

> **Junior Architect** (_July, 2017 – May, 2019_) at Tanya Karim N. R. Khan & Associates, Dhaka, Bangladesh 

---

---

## Technical Skills

<div style="display: flex; flex-wrap: wrap; gap: 20px;">
  <div style="flex: 1; min-width: 150px;">
    <ul>
      <li>ArcGIS</li>
      <li>AutoCAD</li>
      <li>Python</li>
      <li>Lumion</li>
    </ul>
  </div>
  <div style="flex: 1; min-width: 150px;">
    <ul>
      <li>Photoshop</li>
      <li>Adobe Illustrator</li>
      <li>Adobe InDesign</li>
      <li>Microsoft Office</li>
    </ul>
  </div>
  <div style="flex: 1; min-width: 150px;">
    <ul>
      <li>SketchUps</li>
      <li>Revit</li>
      <li>V-Ray</li>
      <li>Enscape</li>
    </ul>
  </div>
</div>

---

---
 
# Adv. GIS Course

In this section, I have demostrated diffeent scripts that I have worked so far. The Adv. GIS Repository is composite of branches where different scripts are store.


[Adv. GIS Repository](https://github.com/atarannum/Adv.-GIS-Repository.git)

---

### Highlights

Special factors or a part of the coding from the final project is illustraded here. This final project involves the development of a Python script that allows users to input specific amenities and select a state from which to plot the data. The program will fetch data from OpenStreetMap and plot the map.

```js
// Use of Overpass API to Fetch OpenStreetMap Data.

def get_amenities(amenity, bbox):
    # Overpass API URL
    overpass_url = "http://overpass-api.de/api/interpreter"
    
    # Overpass query to fetch data for the given amenity within the state's bounding box
    query = f'[out:json]; node["amenity"="{amenity}"]({bbox[0]},{bbox[1]},{bbox[2]},{bbox[3]}); out body;'
    
    # Send the request to the API
    response = requests.get(overpass_url, params={'data': query})

- This allows to retrieve real-time data from OpenStreetMap based on user-defined parameters.

- The script uses bounding boxes for specific states to limit the area from which the data is fetched. This means the data is not arbitrarily fetched but is constrained to the area of interest.

- The script is interactive and user-friendly. It allows the user to specify the state and types of amenities to visualize.

```

```ruby
# Visualization

import requests
import geopandas as gpd
import matplotlib.pyplot as plt
from shapely.geometry import Point

- This script takes the geographic coordinates from OpenStreetMap and uses librries such as GeoPandas and Shapely to manipulate and visualize the data on a map.

# Create a GeoDataFrame to store the data
            gdf = gpd.GeoDataFrame({'amenity': [amenity]*len(geometry)}, geometry=geometry)

            # Plot the amenity on the map with its specific color
            gdf.plot(ax=ax, marker='o', color=colors.get(amenity, 'black'), label=amenity, markersize=5)

- It is not just fetching data, the user could also handling it spatially and visualizing it in a map format.

```

---

## Projects

---
---

## Scripting

### [Data Scraping from Open Street Map](https://github.com/atarannum/Fetching_Online_Data_OSM.git)
<img src="assets/img/Data-scraping-1-1200x630.png"/>

This script gathers data from OpenStreetMap and help visualize different amenities amenities across U.S. states (like restaurants, parks, schools, hospitals, etc.). The idea is if a user enters the name of a state and the types of amenities they are interested in, the code will fetch the relevant data and plot it on a map. It pulls data from OpenStreetMap using a query system based on the state’s geographical boundaries. The result is a colorful map showing each amenity type in a different color.

---

### [Hi Ho Cherrie-O!!!](https://github.com/atarannum/Adv.-GIS-Repository/blob/31ce2fa1047dcadde6378def4d29b4dff3847612/CherryOnTree)

It simulates 1000 games of the Hi Ho! Cherry-O game. In each game, the player should start with 10 cherries, and the goal is to remove all cherries from the tree based on random spinner outcomes. The game ends when there are no cherries left on the tree. After running 1000 simulations, the program also calculates and return the average number of attempts it takes to win the game.

    ,-.
    ,  ,-.   ,-.
   / \  (   )-(   )
   \ |  ,.-(   );
    \|,'(   )-(   )
     Y___`-'   `-'
     |/__/  `-'
     |
     |
     |
     |__|_____________

---

### Are you cold? What's the temperature?
### [Temperature Evaluation Script ](https://github.com/atarannum/atarannum.github.io/blob/aa7be34591be2d18f9ba3d0cbc626ed20f3fbf31/Other%20Projects/Temp.%20Eva)

This script prompts the user to enter a temperature and the program tells whether it is too hot, too cold or it's just right! 

---

### Do you want to play a game? Let's play...
### [Rock, Paper, Scissors](https://github.com/atarannum/atarannum.github.io/blob/faedcc7bb23447cda30fcf30e464e3069618de28/Other%20Projects/Rock%2C%20Paper%2C%20Scissors)

The script simulates a Rock, Paper, Scissors game between two computer players. 

It  simulates 100 games between Player A and Player B. It tracks and prints how many games Player A wins, how many Player B wins, and how many games end in a draw.

After all 100 games are played, the program prints the percentage of games that were draws.

---

### Math is hard!

Use the following script for identifying the factorial number.

[Find the Prime Number](Other Projects/Fac num)

```js
// Funtion for finding the factorial number.

def factorialNumber(UserInput):   
    factorial = 1
    for i in range(UserInput):
        factorial *= (i+1)
    return(factorial)
    
factorialNumber(UserInput = int(input("Enter your number: ")))  

def Fac():
    user = int(input("Enter your number: "))
    factor = 1
    for i in range(user):
        factor *= i+1
    return factor
        
Fac()
```

---

### Need to batch reproject? But do not want to use arcpy?

Use the following link to find out the scripting!

### [Batch Reprojection (not using arcpy)](Other Projects/Batch Reprojection.pdf)

---

## Model Builder

- [Model Builder_New School Site](model_builder/annotated-NewSchoolSite.jpg.pdf)
- [Model Builder_New School Site with Existing Road](model_builder/annotated-NewSiteExistingRoad.jpg.pdf)
- [Model Builder_New School Site with Portion of Existing Road](model_builder/annotated-NewSchoolSiteWithPortionOfExistingRoad.jpg.pdf)

---

---

### Other Projects

- [Interactive Game - Kitchen Conundrum](Other Projects/Kitchen Conundrums.html)
- [Story Map - Bengali Language Movement](https://storymaps.arcgis.com/stories/f8f6c81673f045748a678c0a92286ab7)
- [Timeline - Bangladesh Liberation War](https://cdn.knightlab.com/libs/timeline3/latest/embed/index.html?source=12SmUCeM7UfwuzooLFEIW1EAJSlPhtKKr6CIMS5_s02o&font=Default&lang=en&initial_zoom=2&height=650)

---

---

### For more scripting, please visit

[Adv. GIS Repository](https://github.com/atarannum/Adv.-GIS-Repository.git)


---

---

