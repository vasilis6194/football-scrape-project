# 🏆 PAOK FC Player Performance Analysis

![Football Header](https://www.scisports.com/wp-content/uploads/2018/11/SciSports-Visual-Insight-screen-v4-1920-1280x720.jpg)

## 📌 **1. Introduction**
This project analyzes PAOK FC player performance by collecting, processing, and visualizing data from the official PAOK FC website. The analysis was conducted in two phases:
1. **Python** for initial exploration and visualizations.
2. **Power BI** for advanced insights and interactive dashboards.

---

## 🔍 **2. Data Collection**
Data was web-scraped using Python’s Beautiful Soup library. The dataset includes statistics such as goals, assists, accuracy, defensive actions, and minutes played. After cleaning and verifying the data, it was exported to `.xlsx` format for Power BI analysis.

### **Code Snippet (Data Gathering)**:
```python
from bs4 import BeautifulSoup
import requests

df = pd.DataFrame()
for url in (squad_urls):
    response = requests.get(url, headers=headers)
    soup = BeautifulSoup(response.content, 'html.parser')
    
    #name of each player
    name = soup.find('div', {'class': "row the-content single-profile-content"}).\
        find('section', {'class': "col-sm-12 single-profile-header"}).\
        find('h1').text
```

# 📊 3. Analysis in Jupyter Notebook

The data was analyzed using Pandas and Matplotlib. Key visualizations include:

- **Top 10 Scorers**: Bar chart of players with the highest goals scored.
- **Accuracy Analysis**: Scatter plot comparing shots to accuracy rates.
- **Defensive Actions**: Double y-axis graph for steals and yellow cards.

### **Challenges**:
- Anomalies in data (e.g., Tomasz Kedziora with 93 attempts).
- Ensuring consistency across datasets.

---

# 🛠️ 4. Data Export for Power BI

The cleaned data was exported using `df.to_excel()` and imported into Power BI for further analysis.

---

# 📈 5. Power BI Analysis
![Power BI Analysis](https://github.com/vasilis6194/football-scrape-project/blob/main/4.PowerBI%20Analysis/PowerBI_analysis_image2.png)(https://app.powerbi.com/view?r=eyJrIjoiOTg4ZDU1NWEtNjJlMC00NDAwLWE0MTktZmQwZDU5MTQ2OGVhIiwidCI6IjI1Y2UwMjYxLWJiZDYtNDljZC1hMWUyLTU0MjYwODg2ZDE1OSJ9)


### **Key visualizations**:
1. **Top 5 Scorers**: Bar chart ranking players by total goals.
2. **Top Assist Players**: Bar chart showing players with the highest assists.
3. **Top Accurate and Goals Players**: Double-axis chart comparing goals to accuracy percentages.
4. **Top Players by Steals, Clearances, and Yellow Cards**: Double-axis clustered bar chart highlighting defensive contributions.
5. **Players with Most Minutes Played**: Double-axis chart showing total and average minutes per game.

### **Summary Cards**:
- ⚽ **Total Goals**
- 🎯 **Total Assists**
- 🔢 **Zivkovic’s Goal Contribution (%): 22.03%**
- 🔢 **Despodov’s Goal Contribution (%): 23.73%**

---

# 🔑 6. Insights

- **Attack**: Despodov and Zivkovic contribute significantly to goals and assists, highlighting their importance in attack.
- **Accuracy**: Shola Shoretire demonstrates the highest accuracy but has fewer attempts, indicating potential for growth.
- **Defense**: Players like Tomasz Kedziora and Dominik Kotarski play critical roles defensively.
- **Consistency**: Dominik Kotarski leads in minutes played, showing reliability and consistency.

---

# 🚀 7. Skills Demonstrated

### **Python**:
- Web scraping using Beautiful Soup.
- Data manipulation using Pandas.
- Visualization using Matplotlib.

### **Power BI**:
- Data modeling and transformation.
- DAX formulas for measures and calculated columns.
- Interactive and visually appealing dashboards.

### **Analytical Thinking**:
- Identifying key insights from data.
- Creating meaningful visualizations.

---

# ✅ 8. Conclusion

This project showcases a comprehensive analysis of PAOK FC’s player performance. Combining Python and Power BI enables both technical and non-technical audiences to understand the team’s dynamics and areas for improvement.
