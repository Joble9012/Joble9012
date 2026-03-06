# My Portfolio 

---

# Table of Contents
- [Bubble Tea Retail Sales Analysis](#bubble-tea-retail-sales-analysis)
- [Drug Safety & Adverse Event Analysis (FAERS 2023)](#Drug-Safety-&-Adverse-Event-Analysis-(FAERS-2023))
- [Spotify Listening History Analysis](#spotify-listening-history-analysis)
- [Random Artist Generator](#random-artist-generator)

---

# Bubble Tea Retail Sales Analysis

![Bubble Tea Dashboard](https://raw.githubusercontent.com/Joble9012/Images/1bc7616826ae67a99340c91a63defbe6d4803fb4/BTDashboard2.png)
![Bubble Tea Dashboard](https://raw.githubusercontent.com/Joble9012/Images/1bc7616826ae67a99340c91a63defbe6d4803fb4/BTDashboard1.png)

[**View Source Code**](https://github.com/Joble9012/BubbleTeaRetailSalesAnalysis)

## Overview
Bubble tea has been a big part of my life since college, and Mr. Wish is my go-to chain. This project analyzes sales performance across five Mr. Wish locations using a fully custom-generated, realistic dataset based on actual menus and pricing.  
The goal was to simulate a real multi-location retail environment and demonstrate a complete analytics workflow—from data creation to insights and visualization.

## Project Purpose
Management at Mr. Wish often lacks clear visibility into performance differences across stores, product trends, and customer behaviors. This project aims to answer questions such as:

- Which stores perform best?  
- Which drinks drive the most revenue?  
- How do preferences (toppings, sugar levels, temperature) influence sales?  
- What seasonal or time-based patterns exist?  

The objective was to analyze 12 months of synthetic sales data and produce meaningful insights and recommendations.

## What I Built
To keep the project realistic and manageable, I generated and analyzed a complete year of bubble tea retail data (Jan–Dec 2024). Key components include:

### Data Generation  
A Python script generated daily transactions with realistic patterns such as:
- Seasonal demand  
- Store performance differences  
- Weighted drink popularity  
- Sugar/ice/topping logic  
- Weekday vs. weekend behavior  
- Time-of-day peaks  

### Data Preparation & Data Quality Check
I cleaned and structured the data into tables such as:
- Stores  
- Products  
- Sales transactions

To ensure data reliability, I performed validation checks by:
- Identifying and handling missing values
- Detecting and removing duplicates
- Verifying consistent date formatting

### Dashboards  
The dashboards visualize:
- Monthly revenue trends  
- Store comparisons  
- Product performance  
- Customer preference patterns  
- Topping usage  
- Time-of-day heatmaps

## Key Insights
### 1. Product & Category Insights
- Smoothies lead with 17K+ sales, outperforming all other drinks.  
- Milk Tea & Fruit Tea strong (13K+ sales), showing diverse tastes.  
- Seasonal & Sparkling drinks underperform, signaling growth opportunities.  

### 2. Customer Preference Insights
- Large (L) drinks dominate at 63% of sales.  
- 50%–75% sugar levels preferred, representing 35K+ sales.  
- Cold drinks are overwhelmingly favored (92% of orders).  

### 3. Time & Season Insights
- Revenue peaks May–August (warm season).  
- Sales drop post-September, especially for fruit drinks.  
- Peak hours 2–6 PM; weekends highest activity.  

## Recommendations
### 1. Increase Focus on High-Demand Categories
- Expand smoothies & fruit teas, including seasonal variants.  
- Promote bestsellers with combo deals or loyalty rewards.  
- Highlight top-selling drinks in marketing campaigns.  

### 2. Optimize Inventory & Operations
- Stock ingredients for peak-demand drinks (fruit purées, tapioca, jelly).  
- Ensure sufficient large cups & cold drink supplies.  
- Scale staff 2–6 PM & weekends to improve service.  

### 3. Strengthen Low-Performing Categories & Stores
- Boost Sparkling/Winter Melon drinks with bundles & campaigns.  
- Northeast: local ads, exclusive items, in-store sampling.  
- Adjust operations based on foot traffic analysis.  

## Tech Stack
`Python` `Pandas` `Tableau`

---
# Drug Safety & Adverse Event Analysis (FAERS 2023)

![FAERS Dashboard](https://github.com/Joble9012/Images/blob/f94bd79004f421c224a338c76038a571d41d5e1f/FAERSDashboard.jpg)

[**View Source Code**](https://github.com/Joble9012/FAERS2023AdverseEventsAnalysis)

## Overview
This project analyzes the 2023 FDA Adverse Event Reporting System (FAERS) dataset to uncover insights on drug safety, patient risk, and reporting trends. Built using Databricks, the pipeline includes Bronze, Silver, and Gold layers, enabling clean, structured, and query-ready datasets for advanced analytics and dashboards. This is a continuous learning project; additional notebooks will expand on analysis, visualizations, and machine learning approaches.

## What I Did
- Designed and implemented a Databricks ETL pipeline to ingest, clean, and unify multiple FAERS tables.

- Created Silver layer tables for standardized demographic, drug, reaction, and outcome data.

- Developed Gold layer tables and queries for actionable insights on drug safety, including top drugs by death cases, frequent adverse reactions, and demographic risk.

- Built a dashboard reflecting analytical results to provide interactive visualizations of patient safety metrics.

- Ensured the workflow is modular and extendable, allowing for future analysis, additional notebooks, and machine learning experiments.

## Tech Stack
`Databricks` `Spark SQL` `Delta Lake` `Python (PySpark)` `Databricks SQL Dashboards` 

---

# Spotify Listening History Analysis

![Spotify Project Screenshot](https://raw.githubusercontent.com/Joble9012/Images/3962cd7673171616888e08585046db49f7303344/Dashboard.png)

[View Source Code](https://github.com/Joble9012/SpotifyListeningHistoryDataAnalysis)  

## Overview
Music has always been a part of my daily routine—whether I’m on my way to school, studying, working out, or just relaxing. Over the years, Spotify has become a constant companion, silently collecting data about my listening habits. This project explores that history to uncover what my music says about me, what artists and genres dominate my playlists, when I tend to listen the most, and how my habits have evolved over time.

The objective of this project is to analyze and visualize my personal Spotify listening history to gain deeper insight into my listening behavior. By transforming raw Spotify streaming data into meaningful metrics, I aimed to answer questions like:
Which artists and songs have defined different periods of my life?
What time of day or week do I listen most frequently?
How have my preferences shifted over the years?

Ultimately, this project combines data analysis and storytelling—turning years of streaming history into a visual reflection of my music journey.



## What I Did
To start, I requested my Spotify listening history through their data request feature. A few days later, I received around ten separate JSON files containing roughly 900,000 streaming records.

I began by exploring the structure of the files, examining column names, checking sample entries, and understanding what each field represented. Then, using Python and pandas, I cleaned and consolidated the data into a single CSV file. This involved:
- Merging all JSON files into one dataset
- Removing unnecessary columns (e.g., IP addresses, platform details, audiobook fields)
- Filtering out outliers like ambient noise tracks (e.g., “White Noise 3 Hour Long”)
- Formatting timestamps and converting milliseconds to minutes
- Keeping only data from 2018 onward to ensure consistency

After cleaning the data, I brought the refined dataset into Tableau and began shaping it into a single interactive dashboard. I designed it to tell the story of my listening habits over time, showing how they shift by hour and weekday, while also spotlighting the artists and songs I played the most.

In designing the visualizations, my goal was to balance insight and simplicity—showing the most meaningful patterns without overwhelming the viewer. I styled the dashboards to resemble Spotify’s clean UI aesthetic, and experimented with filters that allow exploration by year and month.


## Key Insights
1. **Lowest Listening Day:** Sundays had the least listening time (family, church, errands).  
2. **Consistent Top Artists:** *Post Malone* and *Juice WRLD* appear consistently over the years.  
3. **Peak Listening Time:** Around **3:00 PM**, likely tied to afternoon activity or work sessions.  

## Tech Stack
`Python` `Pandas` `Tableau`

---

# Random Artist Generator

![Random Artist Generator Screenshot](https://raw.githubusercontent.com/Joble9012/Images/642298eb37114e0e41da65824c479a177e199ff1/RandomArtistGeneratorImage.png)

[View Source Code](https://github.com/Joble9012/RandomArtistGenerator)  

## Overview
As someone who listens to music every day, I found myself stuck in a loop — playing the same songs and artists over and over again. With so much music available, discovering something new often felt overwhelming.

To break that cycle and explore fresh music, I built the Random Artist Generator — a Python application powered by the Spotify Web API. It helps users discover random artists, view their details, and store them locally for future listening.

This project combines my love for music with programming, aiming to make music discovery effortless and engaging.

## What I Did

- **Designed and implemented** a full Python application that generates and manages random music artists using the **Spotify API**.

- **Built two user interfaces:**
  - A **command-line interface (CLI)** in `main.py` for terminal-based interaction.  
  - A **graphical user interface (GUI)** in `app_ui.py` using **Tkinter**, allowing users to generate random artists, view saved artists, and clear the database.

- **Integrated Spotify API** via the `spotipy` library and `SpotifyClientCredentials` for secure, authenticated artist data retrieval.

- **Implemented database management** with **SQLite3:**
  - Created and maintained an `artists.db` database through `artist_db.py`.  
  - Added functionality to check for duplicates (`artist_exists`), insert new artists (`save_artist`), and clear all records (`clear_db.py`).

- **Developed logic for random artist selection** in `spotify_client.py`:  
  - Fetched artists using random search letters.  
  - Filtered by popularity to ensure quality results.  
  - Avoided duplicates using artist IDs.

- **Enabled persistent data storage**, so previously generated artists are saved locally for later viewing.

- **Created a separate viewer utility** (`view_artists.py`) to list all saved artists with their popularity, genres, and Spotify links.

- **Enhanced user experience with:**
  - Clickable Spotify links in the GUI.  
  - Scrollable text areas for displaying multiple entries.  
  - Confirmation dialogs and clear success/error messages.

- **Documented dependencies** in a `requirements.txt` file for easy environment setup (`spotipy`, `python-dotenv`).

- **Used environment variables** for secure Spotify API credentials management (`.env` file).


## Upcoming Ideas Include  
- [ ] Genre filter with checkboxes to discover artists from specific styles  
- [ ] Album randomizer mode  
- [ ] Improved and more polished UI  
- [ ] Mobile-friendly version  
- [ ] Integration with my Spotify listening history to make personalized suggestions

## Tech Stack
`Python` `Tkinter` `SQLite` `Spotipy` `Dotenv`


