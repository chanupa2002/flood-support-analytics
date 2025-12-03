🌊 Flood Support Analytics Dashboard

Data Cleaning • Geospatial Analysis • Humanitarian Insights • Visualization

This project analyzes real flood-related support requests collected from communities across Sri Lanka. The goal is to understand where people requested help, what type of support they needed, and how severe the situations were across districts.

The final output is a full interactive analytics dashboard built with Python, Plotly, Folium, and HTML.

📌 Project Overview

During a recent flood situation in Sri Lanka, hundreds of individuals made support requests across multiple districts.
Each request contains:

City and district
Latitude & longitude
Urgency level
Type of help needed (Food, Water, Medicine, Rescue, etc.)


This project transforms that raw dataset into actionable analytics by:

✔ Cleaning and standardizing the city/district data
✔ Mapping locations to actual districts
✔ Encoding assistance types into usable numeric features
✔ Performing exploratory analysis
✔ Visualizing patterns and hotspot areas
✔ Clustering similar requests
✔ Building a fully interactive dashboard


1. Data Cleaning & Pre-processing

  Key cleaning steps performed:
      Removed invalid cities (uppercase-only, with special characters, with numbers except Colombo 1–15)
      Extracted city name from full address
      Normalized city names (case-insensitive)
      Mapped each city → district using an external reference CSV
      Used LLM fallback for unknown district detection (only for uncategorized cities)
      Removed all rows where district remained “Unknown”
      One-hot encoded support types (Food, Water, Baby Items, Boats, etc.)
  This produced a clean, structured dataset ready for analysis.


2. Exploratory Data Analysis & Visualizations

  The following insights were analyzed and visualized:
    ✔ Requests by District: Shows which districts had the highest number of flood support requests.
    ✔ District × Urgency Heatmap: Reveals where emergency and high-urgency cases were concentrated.
    ✔ Assistance Type Totals: Identifies the most requested types of help across the entire country.
    ✔ Needs by District: Each district has a different support "signature", showing what kind of help people needed the most.
    ✔ Urgency vs Assistance Heatmap: Shows which types of needs are associated with severe/emergency conditions.
    ✔ Geographic Distributions: Scatter map showing all locations on Sri Lanka, Density heatmap showing hotspot areas of distress
    ✔ K-Means Clustering

  Groups requests into meaningful clusters:
   ✔Rescue-heavy clusters
   ✔Basic needs clusters
   ✔Medical-heavy clusters
   ✔Low-urgency clusters


3. Interactive Dashboard
   
  A full multi-tab dashboard was created using HTML, JavaScript, and embedded Plotly/Folium charts.

  Features:
    Clean horizontal tab navigation
    Full-screen graphs
    Scrollable insight descriptions under each plot
    About page with project summary
    Footer crediting the author

  fully interactive visual analytics views

  To run locally: python3 -m http.server 8000
  Then open: http://localhost:8000/flood_dashboard_new.html


4. Tools & Technologies Used
   
  Purpose	                          Tools
  Data Cleaning	                    Python, Pandas
  Plotting	                        Plotly Express
  Geospatial Maps	                  Folium
  Clustering & ML	                  Scikit-learn
  Dashboard	Custom                  HTML/CSS/JS
  LLM-based District Matching	      Gemini 2.5 Flash

  
📁 Project Structure (Suggested)
├── cleaned_dataset.csv
├── district_city_mapping.csv
├── flood_dashboard_new.html
├── Total_Support_Requests_by_District.html
├── Support_Requests_by_District_and_Urgency_Level.html
├── Total_Assistance_Types_Requested.html
├── Top_Assistance_Needs_by_District.html
├── Urgency_Level_vs_Assistance_Types_Heatmap.html
├── Geographical_Distribution_of_Flood_Support_Requests.html
├── flood_requests_heatmap_SL.html
├── District_vs_Assistance_Types_Needs_Heatmap.html
├── KMeans_Clustering_of_Help_Request_Profiles.html
└── README.md

👤 Author

Developed & Analysed by:
Chanupa Athsara
📧 athsara141@gmail.com


📜 License & Usage
This project is intended for:
  Humanitarian analysis
  Research
  Educational use
  Disaster response planning

Please ensure privacy and data protection when using real-world human support records. Do not redistribute sensitive information without proper clearance.

