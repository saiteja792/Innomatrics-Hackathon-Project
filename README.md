##  Zomato Analysis & Mapping

This project performs an end-to-end exploratory data analysis (EDA) and interactive spatial visualization of Bangalore’s Zomato restaurant dataset. We leverage Python, pandas and Folium to answer business questions and build interactive maps—all within a Jupyter Notebook.

### Dataset Description

- **`zomato_data.csv`**  
  Contains ~51,700 restaurant records in Bangalore with attributes such as:
  - `online_order`, `book_table`  
  - `rate` (aggregate rating out of 5)  
  - `votes` (number of customer votes)  
  - `rest_type` (restaurant category)  
  - `cuisines` (comma‑separated)  
  - `approx_costfor_two_people`  
  - City/locality  

- **`Geographical Coordinates.csv`**  
  Provides latitude/longitude for each locality in Bangalore.

### Task 1: Exploratory Data Analysis

We cleaned and normalized columns, converted ratings and costs to numeric, and merged locality coordinates. Key insights:

1. **North Indian** is the most common cuisine, with **21,085** restaurants.  
2. The dataset shape is **51,717 rows × 10 columns**.  
3. **Brigade Road** has the highest average dining cost.  
4. Top‑rated restaurant type (with >1,000 votes) is **Microbrewery, Pub**.  
5. Minimum cost for two is ₹40.  
6. Banashankari accounts for **1.8%** of all online‑order restaurants.  
7. **Brookefield** has the most low‑rated (★ < 3.0) but highly‑voted (>500) restaurants.  
8. **BTM** shows the greatest diversity of restaurant types—ideal for expansion.  
9. Maximum votes for an online‑order restaurant: **16,832**.  
10. Restaurants serving both North Indian & Chinese average ★ 3.57.  
11. **Koramangala 7th Block** yields the highest potential revenue (cost × votes).  
12. To reduce complaints, focus on **Sweet Shop / Quick Bites** (lowest avg. rating).  
13. Invest in **Koramangala 7th Block** for highly‑rated (★ > 4.2), well‑voted (> 500), online‑order establishments.

### Task 2: Cuisine‑Specific Interactive Mapping

Using **Folium**, we built a function that:
- Filters restaurants by any cuisine (e.g. “North Indian”)
- Plots each location as a clickable circle with popup details (type, cost, rating)
- Centers the map dynamically on the mean latitude/longitude of that cuisine



### Task 3: Interactive Density (Heat) Mapping

Also with Folium’s **HeatMap**:
- Aggregates all restaurant coordinates
- Renders a density‑weighted “heat” overlay on Bangalore’s map  
- Highlights hotspots of restaurant concentration
