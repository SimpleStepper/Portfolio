---
title: "Tower Unit Calculator - Data-Driven Cost Calculator"
categories:
  - Excel
  - Python
  - Data Cleaning
  - Data Mining
  - Pandas
  - Data Scraping
tags:
  - Data Visualization
  - Data Cleaning
  - Data Mining
---
## This project aims to provide Bloons Tower Defense 6 (BTD6) players with a user-friendly application to determine the in-game cost of tower units and their upgrades across different difficulties using data scraped from the wiki.
The final project can be accessed using this [Google Sheets link](https://docs.google.com/spreadsheets/d/1bgRTX8VRlwiGp4RJNIbdQKh3tUHXspOqAZUE-NDchDM/edit?usp=sharing). 

![Bloons Project Showcase gif](https://github.com/user-attachments/assets/0e59c70d-20d5-4097-ac36-db24ffb9d9ba)

--- 

### Features & Functionality
- Cost Calculation: Calculates the cost of BTD6 towers and their upgrades.
- Difficulty-Based Pricing: Accounts for different in-game difficulties (Easy, Medium, Hard, Impoppable).
- Interactive Interface: Google Sheets dropdown menus for user accessibility and interaction,

--- 

## Overview
This objective of this project was to develop a user friendly application for Bloons Tower Defense 6 (BTD6) players to be able to determine how much a in-game Tower unit cost dynamically within Google Sheets. This project includes utilizing Python to acquire and organize data, Google Sheets to create calculation formulas, allow easy user accessibility and interaction with the app. 

## Project Structure / How it was made
This project combines 2 major elements: 
- Python scripting for data acquisition and data cleaning. 
- Google Sheets dropdown menu for an accessible and interactive user experience.

### Data Collection and Cleaning (Python)
The BloonsProject.ipynb is a jupyter notebook used to prepare the projects data. This included: 

1) **How the Data is First Gathered (Automated Collection)**
The first step was to get tower cost information directly from the Bloons TD 6 Fandom Wiki. This project uses Python to webscrape the HTML data from the Wiki, and automatically acquire all the tower names, upgrade paths, and their costs without manual input. This data is unrefined from the initial webscraping, difficulty to work with and needed improvements before its used.

2) **Data Cleaning and transformation:**
After collecting the raw information about tower costs from the Bloons Fandom Wiki, the data was messy and required several steps to make it useable:
-The raw data often includes extra words, symbols, or formatting alongside the actual cost numbers (e.g., "Cost: 100 Cash" or "Upgrade Price $50"). The website was also missing information on newer game updates, which were inserted manually to match existing data structure.

The project then organizes this data. It clearly separates the unit costs based on:
  - Game Difficulty: Distinguishing prices for Easy, Medium, Hard, and Impoppable modes.
  - Upgrade Tiers: Categorizing costs for each specific upgrade level (Tier 1 through Tier 5) along different upgrade paths.

This structuring creates a consistent and easy-to-use dataset, and exports the data into a excel spreadsheet for further processing. 

![image](https://github.com/user-attachments/assets/eabb13f2-35a2-48ea-bd9c-841bd95876af)

### Data Storage & Calculation (Google Sheets)
The processed data from the Python script is integrated with Google Sheets to create the user-facing application.
- Each tower's base cost and upgrade costs for all difficulties and tiers are organized into 4 different sheets, making them ready for lookups and calculations.
Formulas for User Interaction: Google Sheets is used to create dynamic formulas that allow users to interact with the data:
 - Users can select a specific tower, its desired upgrade path(s), and the game difficulty directly within the Google Sheet interface.
 - Formulas (e.g., VLOOKUP, SUMIFS, INDEX/MATCH combinations) automatically query the organized cost data. Based on the user's selections in the dropdown menus, these formulas calculate the total cost of the chosen tower and its upgrades.

![image](https://github.com/user-attachments/assets/f130b443-41d0-4201-94e0-555c45b21b3c)

--- 

# Conclusion
This project was my first time using Python's built in webscraping libraries, and my first time cleaning real world messy data. My initial scope was to make a simple tool for BTD6 players to be able to quickly be able to tell the cost of a unit in game. I gained experience with formulas and dropdown menus in Excel/Google sheets, and how to make something user friendly and try to hide as much technical elements as possible.
