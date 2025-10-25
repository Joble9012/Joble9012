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
This project dives into my personal Spotify listening history to uncover my music habits—what I listen to most, when I listen, and how patterns change over time.  



### What I Did

I downloaded my full Spotify history as multiple JSON files containing timestamps, track and artist names, and play durations in milliseconds. The first step was consolidating all data into a clean CSV file. During cleaning using Python, I:  
- Removed unnecessary columns (platform details, IP addresses, audiobook fields)  
- Filtered out outliers (e.g., *“White Noise 3 Hour Long”*)  
- Formatted dates and converted milliseconds to minutes  
- Retained plays from 2018 onward only  

After cleaning, I analyzed the data using **Python pandas** to identify top artists, most-played songs, and total listening hours. Visualizations were created with **Tableau** dashboards.


### Key Findings
1. **Lowest Listening Day:** Sundays had the least listening time (family, church, errands).  
2. **Consistent Top Artists:** *Post Malone* and *Juice WRLD* appear consistently over the years.  
3. **Peak Listening Time:** Around **3:00 PM**, likely tied to afternoon activity or work sessions.  
4. **Monthly Patterns:** No single “highest” month — habits vary yearly.

### Challenges & Learnings

### Tech Stack
`Python` `Pandas` `Tableau`

---

## Random Artist Generator

![Random Artist Generator Screenshot](https://raw.githubusercontent.com/Joble9012/Images/642298eb37114e0e41da65824c479a177e199ff1/RandomArtistGeneratorImage.png)

[View Source Code](https://github.com/Joble9012/RandomArtistGenerator)  

### Overview & Objective
I noticed I kept listening to the same songs repeatedly. To break the routine and discover new artists, I created the **Random Artist Generator**, a Python application that uses the **Spotify Web API** to suggest artists, show details, and save them in a local database.

### What I Did

- **Random Artist Generation:** Pulls a random artist from Spotify above a set popularity score  
- **Artist Details:** Displays artist name, popularity, genres, and clickable Spotify link  
- **Database Storage:** Saves discovered artists in a local SQLite database  
- **Duplicate Prevention:** Ensures no repeated artists  
- **View All Artists:** Lists all saved artists with details  
- **Clear Database:** Wipes stored artists easily

How It Works
1. **Spotify API Connection:** Uses Spotipy with your Spotify API credentials  
2. **Random Search:** Selects a random letter, fetches 50 artists, filters by popularity  
3. **Display & Save:** Shows artist details and saves to `artists.db`  
4. **Avoid Repeats:** Skips artists already stored

### Reflection
This project is still in its early stages, and I’m excited to expand its capabilities.  

Upcoming ideas include:  
- [ ] Genre filter with checkboxes to discover artists from specific styles  
- [ ] Album randomizer mode  
- [ ] Improved and more polished UI  
- [ ] Mobile-friendly version  
- [ ] Integration with my Spotify listening history to make personalized suggestions

### Tech Stack
`Python` `Tkinter` `SQLite` `Spotipy` `Dotenv`
