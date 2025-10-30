# 👋 Hi there, I'm Joble — Welcome to my Project Portfolio! 

---

## Table of Contents
- [Spotify Listening History Data Analysis](#spotify-listening-history-data-analysis)
- [Random Artist Generator](#random-artist-generator)

---

## Spotify Listening History Data Analysis


![Spotify Project Screenshot](https://raw.githubusercontent.com/Joble9012/Images/f05a1e72853e1ac452fe05bccedf462cc8873881/Dashboard1.png)

![Spotify Project Screenshot](https://raw.githubusercontent.com/Joble9012/Images/f05a1e72853e1ac452fe05bccedf462cc8873881/Dashboard2.png)

[View Dashboards](https://public.tableau.com/views/Dashboard_17546697496100/ArtistSongDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)  

[View Source Code](https://github.com/Joble9012/SpotifyListeningHistoryDataAnalysis)  

### Overview & Objective
Music has always been a part of my daily routine—whether I’m on my way to school, studying, working out, or just relaxing. Over the years, Spotify has become a constant companion, silently collecting data about my listening habits. This project explores that history to uncover what my music says about me, what artists and genres dominate my playlists, when I tend to listen the most, and how my habits have evolved over time.

The objective of this project is to analyze and visualize my personal Spotify listening history to gain deeper insight into my listening behavior. By transforming raw Spotify streaming data into meaningful metrics, I aimed to answer questions like:
Which artists and songs have defined different periods of my life?
What time of day or week do I listen most frequently?
How have my preferences shifted over the years?

Ultimately, this project combines data analysis and storytelling—turning years of streaming history into a visual reflection of my music journey.



### What I Did
To start, I requested my Spotify listening history through their data request feature. A few days later, I received around ten separate JSON files containing roughly 900,000 streaming records.

I began by exploring the structure of the files, examining column names, checking sample entries, and understanding what each field represented. Then, using Python and pandas, I cleaned and consolidated the data into a single CSV file. This involved:
- Merging all JSON files into one dataset
- Removing unnecessary columns (e.g., IP addresses, platform details, audiobook fields)
- Filtering out outliers like ambient noise tracks (e.g., “White Noise 3 Hour Long”)
- Formatting timestamps and converting milliseconds to minutes
- Keeping only data from 2018 onward to ensure consistency

Once the data was cleaned, I performed exploratory data analysis (EDA) to uncover trends and insights. Using Python, I identified metrics such as top artists, top tracks, total listening time, and yearly listening distribution.

After completing the analysis, I imported the cleaned dataset into Tableau to design interactive dashboards. I created two main dashboards:
Listening Over Time – focused on trends by hourly, day, and month.
Artists & Songs – highlighting my most-played artists and tracks

In designing the visualizations, my goal was to balance insight and simplicity—showing the most meaningful patterns without overwhelming the viewer. I styled the dashboards to resemble Spotify’s clean UI aesthetic, and experimented with filters that allow exploration by year and month.


### Key Findings
1. **Lowest Listening Day:** Sundays had the least listening time (family, church, errands).  
2. **Consistent Top Artists:** *Post Malone* and *Juice WRLD* appear consistently over the years.  
3. **Peak Listening Time:** Around **3:00 PM**, likely tied to afternoon activity or work sessions.  
4. **Monthly Patterns:** No single “highest” month — habits vary yearly.

### Reflection
Working with Spotify’s data presented a few unexpected challenges. The raw JSON files were large, inconsistent, and split across multiple exports, which made data consolidation and cleaning the most time-consuming step. I had to carefully parse timestamps, remove duplicate entries, and convert milliseconds to meaningful units like minutes and hours.
Another challenge was handling incomplete or misleading data, such as songs with extremely short play durations or non-music content (like white noise or podcasts). Designing filters to exclude these outliers was key to keeping the analysis accurate.

On the visualization side, learning to effectively use Tableau to tell a clear story through charts and dashboards pushed me to think critically about data presentation—how to highlight patterns without cluttering the view.

Through this project, I strengthened my skills in data wrangling, analysis, and visualization, while also gaining a new appreciation for how much data can reveal about personal habits. Beyond the technical side, it was fascinating to see my music taste evolve and connect those trends to different stages of my life.

### Tech Stack
`Python` `Pandas` `Tableau`

---

## Random Artist Generator

![Random Artist Generator Screenshot](https://raw.githubusercontent.com/Joble9012/Images/642298eb37114e0e41da65824c479a177e199ff1/RandomArtistGeneratorImage.png)

[View Source Code](https://github.com/Joble9012/RandomArtistGenerator)  

### Overview & Objective
As someone who listens to music every day, I found myself stuck in a loop — playing the same songs and artists over and over again. With so much music available, discovering something new often felt overwhelming.

To break that cycle and explore fresh music, I built the Random Artist Generator — a Python application powered by the Spotify Web API. It helps users discover random artists, view their details, and store them locally for future listening.

This project combines my love for music with programming, aiming to make music discovery effortless and engaging.

### What I Did

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


### Reflection
Building the Random Artist Generator was a rewarding experience,iIt pushed me to work with real-world APIs, manage authentication securely, and design both command-line and graphical interfaces that make the app accessible to different users.

Working with the Spotify API taught me how to handle API rate limits, parse complex JSON responses, and filter meaningful data for a better user experience. Implementing a local SQLite database added another layer of learning. I gained hands-on experience in data persistence, relational design, and CRUD operations.

I also learned the value of clean UI design and user interaction, small touches like clickable links, confirmation prompts, and clear feedback significantly improved usability. Overall, this project strengthened my skills in Python, API integration, and database management.

Upcoming ideas include:  
- [ ] Genre filter with checkboxes to discover artists from specific styles  
- [ ] Album randomizer mode  
- [ ] Improved and more polished UI  
- [ ] Mobile-friendly version  
- [ ] Integration with my Spotify listening history to make personalized suggestions

### Tech Stack
`Python` `Tkinter` `SQLite` `Spotipy` `Dotenv`
