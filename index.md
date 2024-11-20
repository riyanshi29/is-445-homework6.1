
# IS 445 - Homework 6.1
## Creating Visualizations using Building Inventory Dataset

**Submitted By Riyanshi Shah (ryshah2@illinois.edu)**

**The Data:** [Building Inventory Dataset](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)  
**The Analysis:** [Jupyter Notebook Analysis](https://github.com/riyanshi29/is-445-homework6.1/blob/main/Workbook.ipynb)

---

## Visualization 1

<div id="chart1-container"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
  vegaEmbed('#chart1-container', 'chart1.json').catch(console.error);
</script>

---

### **Writeup for Visualization 1**

#### Description  
This bar chart visualizes the total number of buildings across counties, categorized by their building status. The x-axis represents county names, the y-axis shows the number of buildings, and color coding highlights different building statuses such as "Abandon," "In Use," and "In Progress."

#### Encoding Types  
- **X-axis (Nominal):** Displays county names as categorical variables.  
- **Y-axis (Quantitative):** Represents the count of buildings in each county.  
- **Color (Nominal):** Differentiates building statuses using distinct colors.  
- **Tooltip:** Provides details on the county name, building status, and the corresponding count of buildings.

#### Color Scheme  
A categorical color palette is used to distinguish between building statuses, ensuring clarity and visual accessibility for users.

#### Data Transformations  
The dataset was grouped by **County** and **Building Status** to calculate the total number of buildings for each combination. Missing values in relevant columns were replaced to ensure the data was clean and complete.

#### Interactivity  
A radio button selection enables users to filter the chart by a specific building status, allowing for focused analysis.

#### Impact of Interactivity  
The ability to filter by building status helps users identify trends and compare the distribution of building statuses across counties.

#### Overlaps with Homework #7
While the same dataset was used, this visualization does not overlap with the analysis from previous homework. It presents a new perspective by examining the total number of buildings across counties and their building statuses, rather than focusing on square footage or building usage as in previous visualizations.

---

## Visualization 2

<div id="chart2-container"></div>

<script>
  vegaEmbed('#chart2-container', 'chart2.json').catch(console.error);
</script>

---

### **Writeup for Visualization 2**

#### Description  
This bar chart displays the distribution of building usage descriptions within each county. Users can select a county using a dropdown menu to view its detailed usage description breakdown.

#### Encoding Types  
- **X-axis (Quantitative):** Represents the count of buildings for each usage description category.  
- **Y-axis (Nominal):** Displays usage descriptions as categorical variables.  
- **Color (Nominal):** Differentiates usage descriptions with distinct colors.  
- **Tooltip:** Includes building count, usage description, and county name for additional context.

#### Color Scheme  
A categorical color scheme is applied to distinguish between usage descriptions, aiding in readability and category comparison.

#### Data Transformations  
The dataset was cleaned by filling missing values in County with "Not available" and in Usage Description 2/3 with the most frequent values (mode). Only the relevant columns (County and Usage Description) were used for this chart.

#### Interactivity  
A dropdown menu allows users to select a specific county, dynamically filtering the chart to display building usage descriptions for that county.

#### Impact of Interactivity  
The dropdown menu enhances the chart’s usability, enabling users to analyze detailed patterns of building usage for individual counties without cluttering the visualization.

#### Overlaps with Homework #7
Although the same dataset was used, this visualization introduces a fresh perspective that focuses on building usage descriptions within counties, compared to previous visualizations that emphasized square footage or building statuses. This analysis style is distinct from prior work.

---

