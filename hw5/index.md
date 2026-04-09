---
layout: default
title: Homework 5
---

# Homework 5

## Data
[Building Inventory Dataset](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)

## Python Notebook
[HW5.ipynb](https://github.com/IanHsu123/IanHsu123.github.io/blob/main/hw5/HW5.ipynb)

---

## Plot 1: Total Square Footage by Usage

<div id="vis1"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed('#vis1', 'plot1.json');
</script>

### Description
This plot shows the total square footage for different usage types. It helps compare which building usage categories take up the most total space.

### Design Choices
I used a bar chart because it is easy to compare totals across categories. The x-axis shows usage type, and the y-axis shows total square footage. Different colors are used to help separate the usage categories visually.

### Transformations
In the Python notebook, I grouped the data by usage description and summed the square footage for each category. This made it easier to compare the total space used by different building types.

---

## Plot 2: Building Size over Time (Interactive)

<div id="vis2"></div>

<script>
vegaEmbed('#vis2', 'plot2.json');
</script>

### Description
This plot shows the relationship between year constructed and square footage. It helps show how building size changes over time.

### Design Choices
I used a scatter plot because it works well for showing the relationship between two quantitative variables. The x-axis shows year constructed, and the y-axis shows square footage. Tooltips are included so users can view more details for each building.

### Transformations
In the notebook, I selected the needed columns and used the cleaned building data for the scatter plot. I also limited the x-axis range to make the chart easier to read.

### Interactivity
I added an interval selection to this plot so users can drag across part of the chart and highlight buildings in that selected area. This makes the visualization easier to explore and helps users focus on a smaller part of the data.
