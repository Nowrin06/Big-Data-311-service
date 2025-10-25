### 2025_IA626_project_Hemamalini_Shifat

# A Visual Story of Public Complaints in New York City

## Overview
<p align="justify">
This project analyzes 311 Service Requests made in New York City, focusing on complaint trends year-by-year, complaint type distributions, and heatmaps for spatial and categorical complaint patterns.
The goal is to understand how complaints evolve over time and space and identify key trends across different complaint categories.
</p>

## Dataset

- Source: [NYC Open Data Portal - 311 Service Requests](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9)

- Data Period: 2015 to Present (filtered)
- Primary Fields Used:
    - Created Date
    - Complaint Type
    - Borough
    - Incident Zip
    - Latitude / Longitude

## Project Steps

### 1. Data Cleaning
- <p align="justify">Dropped null or missing values from important columns (Complaint Type, Created Date, Borough, Latitude, Longitude).
- <p align="justify">Parsed dates into datetime format for easier year extraction.
- <p align="justify">Filtered the dataset from 2015 onwards to maintain consistency and data quality.
- <p align="justify">Standardized complaint types where necessary (e.g., merging "Noise - Residential" and "Noise - Commercial" under "Noise").

### 2. Data Processing
- Extracted Year, Month, and Hour from the Created Date.
- Categorized complaints into broader categories:
    - <p align="justify">Noise Related: Noise, Noise - Residential, Noise - Commercial, etc.
    - Parking Related: Illegal Parking, Blocked Driveway
    - Food Related: Food Establishment, Food Poisoning
    - <p align="justify">Sanitation Related: Sanitation Condition, Rodent, Graffiti
    - <p align="justify">Other: Lost Property, Homeless Person Assistance, Animal Abuse
- <p align="justify">Grouped and counted complaints by Year, Complaint Type, and Borough.

### 3. Visualizations
**A. Year-by-Year Complaint Comparison**

- <p align="justify">Line Charts showing the total number of complaints each year. Figure 1 showed that the complaints are increasing with the year. Even though it is showing least complaints observed in the current years; however, it is understandable that the data was collected only until the month of April.
<img src="figure/Total 311 Complaints Per Year (2015–2025).png" width="500">

*Figure 1: Total number of complaints each year*

- <p align="justify">Grouped Bar Charts breaking down complaints by category each year. It showed that the most frequent complain is noise accross the year except 2023.
<img src="figure/Grouped Bar Chart Complaints by Category per Year (2015–2025).png" width="500">

*Figure 2: Total number of complaints by category in each year*
- <p align="justify">Heatmap showing the freqency of complaints over years regardless of the complaints category. It showed that the most frequent complaint was illegal parking in year 2024.
<img src="figure/All Complaint Types Over Time.png" width="500">

*Figure 3: Total number of complaints regardless of category in each year*

**B. Complaint Type Heatmaps**

- <p align="justify">Heatmap of Complaint Types: Show frequency of each complaint type across years.
    - <p align="justify">Heatmap for noise complains in relation to the borough showed that the most complains were files in the Broanx area and most prominet type of noise is the residential noise.
<img src="figure/Noise Complaint Types vs Borough Heatmap.png" width="500">

*Figure 4: Heatmap showing the spatial distribution of noise complaints in NYC*

- <p align="justify">Heatmap for food related complains in relation to the borough showed that the most frequent complain is food establishment in the Manhattan area.
<img src="figure/Food Related Complaint Types vs Borough Heatmap.png" width="500">

*Figure 5: Heatmap showing the spatial distribution of food complaints in NYC*

- <p align="justify">Heatmap for sanitation related complains in relation to the borough showed that the most frequent complain is about rodent and filed in the Brooklyn area.
<img src="figure/Sanitation Related Complaint Types vs Borough Heatmap.png" width="500">

*Figure 6: Heatmap showing the spatial distribution of sanitation complaints in NYC*

- <p align="justify">Heatmap for parking related complains in relation to the borough showed that the most frequent complain is illegal parking and filed in the Brooklyn area.
<img src="figure/Parking Related Complaint Types vs Borough Heatmap.png" width="500">

*Figure 7: Heatmap showing the spatial distribution of parking complaints in NYC*

- <p align="justify">Heatmap for other category complains in relation to the borough showed that the most frequent complain is street condition and filed in the Queens area.
<img src="figure/Other Complaint Types vs Borough Heatmap.png" width="500">

*Figure 8: Heatmap showing the spatial distribution of other complaints in NYC*



**C. Complaint Distribution**
- **Complaints distribution by borough:**
    <p align="justify">It showed that most and least number of complaints were filed in the Brooklyn and Staten Island area, respectively, regardless of the complaint category.
<img src="figure/Complaint Count by Borough.png" width="500">

*Figure 9: Complaints count by borough* 


- **Normalized comparison of 311 service complaints:** <p align="justify">Raw complaint counts can be misleading. For example:
Brooklyn might have the most total complaints, but if its population is also the largest, that doesn’t necessarily mean it has more problems.
The following bar graph corrects for that by adjusting for population size.
<img src="figure/Complaints per 100,000 Residents by Borough.png" width="500">

*Figure 10: Normalized complaints count by borough*

- **Top complaints across all years:** <p align="justify">Pie chart showed that the top six cpmplaints out of all 17 complaints.
<img src="figure/Top Complaint Types (All Years).png" width="500">

*Figure 11: Top complaints accross the years*

- **Unsolved complaints:**<p align="justify">Even though there are a lot of complained filed over the years, it showed that many of the complaints were not solved yet. The bar chart showed taht the most unsolved complain is Homeless person assistance.
<img src="figure/Top Complaint Types Missing Closed Date.png" width="500">

*Figure 12: Unsolved complaints accross the years*

## 🌐 Interactive Complaint Maps

Explore complaint clusters across New York City using the interactive maps below. Each map is grouped by year and displays complaint details via clickable popups. Markers have been sampled (max 300/year) for performance.

- <p align="justify">Geographical Heatmaps: Complaints plotted over NYC map (using latitude/longitude) to show hotspots for common complaints.
---

### 🔊 Noise-Related Complaints
 Includes: `Noise`, `Noise - Residential`, `Noise - Commercial`, `Noise - Street/Sidewalk`, `Noise - Vehicle`, `Noise - Park`

📁 **File**: `noise_complaints_cluster_popup_map.html`

---

### 🍽️ Food-Related Complaints 
Includes: `Food Establishment`, `Food Poisoning`, `Rodent`

📁 **File**: `food_complaints_cluster_popup_map.html`

---

### 🧹 Sanitation-Related Complaints
Includes: `Sanitation Condition`, `Graffiti`

📁 **File**: `sanitation_complaints_cluster_popup_map.html`

---

### 🚗 Parking & Street Complaints 
Includes: `Illegal Parking`, `Blocked Driveway`, `Street Condition`

📁 **File**: `parking_complaints_cluster_popup_map.html`

---

### 📦 Other Complaints 
Includes: `Lost Property`, `Animal Abuse`, `Homeless Person Assistance`

📁 **File**: `other_complaints_cluster_popup_map.html`

---

### 📌 Notes
- Markers are grouped using `folium.MarkerCluster` for better map readability.
- All maps are generated using Python (`folium`, `random`, `collections.defaultdict`) from sampled yearly data.

    
## Tools and Technologies

- Python
- Libraries Used:
    - csv for reading the csv file
    - defaultdict for automatically assigns a default value
    - matplotlib for plotting
    - numpy for numerical operations
    - folium for map visualizations (heatmaps)
    - datetime for working with dates and times
    - random for getting same random sample every time
    - Counter to count occurrences of elements in a list
## Running the Project

**1.Clone the repository:**
<pre><code>git clone https://github.com/Clarkson-Applied-Data-Science/2025_IA626_project_Hemamalini_Shifat.git

cd 2025_IA626_project_Hemamalini_Shifat </code></pre>
**2.Install the required libraries:**
<pre><code>pip/pip3(For macos) install csv defaultdict numpy matplotlib folium datetime random counter</code></pre>

**3.Run the Python notebooks/scripts:**
- Open the Jupyter notebook 311_complaints.ipynb or run the .py file step-by-step.
- All major visualizations and outputs are generated automatically.

## Future Improvements

- Incorporate weather data to correlate spikes in noise, sanitation, or rodent complaints.
- Deploy an interactive dashboard (e.g., using Streamlit or Dash) for real-time exploration.


    





