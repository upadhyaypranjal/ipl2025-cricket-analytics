# 🏏 IPL 2025 Cricket Analytics Dashboard

> Data-driven insights from IPL 2025 ball-by-ball data using Python and MySQL to identify batting and bowling performance patterns across different match situations.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-orange.svg)](https://www.mysql.com/)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-red.svg)](https://matplotlib.org/)

---

## 📊 Key Insights

| Analysis Type | Top Performer | Performance |
|--------------|---------------|-------------|
| **Powerplay Specialist** (Overs 1–6) | Sai Sudharsan | 391 runs |
| **Death Overs Finisher** (Overs 16–20) | Shashank Singh | 216 runs |
| **Leading Wicket Taker** | Prasidh Krishna | 26 wickets |

*These insights are derived using SQL queries and visualized with interactive Python charts.*

---

## 🔧 Tech Stack

| Component | Tools Used |
|-----------|-----------|
| **Database** | MySQL |
| **Data Analysis** | Python (Pandas) |
| **Visualization** | Matplotlib |
| **Notebook Execution** | VS Code + Jupyter |
| **Storage** | Local CSV + MySQL |

---

## 📂 Project Structure

```
ipl2025-cricket-analytics/
│
├── data_raw/
│   └── ipl_2025_deliveries.csv
│
├── data_processed/
│   └── visuals/
│       ├── powerplay_top5.png
│       ├── deathovers_top5.png
│       └── wickets_top5.png
│
├── src/
│   └── load_deliveries.py
│
├── notebooks/
│   ├── 01_powerplay_death_analysis.ipynb
│   └── 02_ipl_dashboard.ipynb
│
└── README.md
```

---

## 🧠 SQL Queries Used

- ✅ **Top Powerplay Scorers** (Overs 1-6)
- ✅ **Best Death Overs Finishers** (Overs 16-20)
- ✅ **Top Wicket Takers**
- ✅ **Total Matches & Deliveries Analysis**

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/ipl2025-cricket-analytics.git
cd ipl2025-cricket-analytics
```

### 2️⃣ Install Requirements

```bash
pip install pandas mysql-connector-python matplotlib jupyter
```

### 3️⃣ Setup MySQL Database

Create a database in MySQL:

```sql
CREATE DATABASE ipl_2025;
USE ipl_2025;
```

### 4️⃣ Import Data into MySQL

```bash
python src/load_deliveries.py
```

### 5️⃣ Open the Notebook and Run Visualizations

```bash
jupyter notebook notebooks/01_powerplay_death_analysis.ipynb
```

Or open in VS Code with Jupyter extension installed.

---

## 🔥 Future Enhancements

- [ ] **Venue Scoring Analysis** - Performance metrics across different stadiums
- [ ] **Pressure Performance Metrics** - Player performance in high-stakes situations
- [ ] **Player Consistency Ranking** - Fantasy value and consistency scores
- [ ] **Match Outcome Predictions** - ML models for win probability prediction
- [ ] **Interactive Dashboards** - Streamlit/Dash web application
- [ ] **Real-time Data Integration** - Live match analytics

---

## 📚 Sample Queries

### Top Powerplay Scorers

```sql
SELECT batter, SUM(batter_runs) as total_runs
FROM deliveries
WHERE over_number BETWEEN 1 AND 6
GROUP BY batter
ORDER BY total_runs DESC
LIMIT 5;
```

### Death Overs Finishers

```sql
SELECT batter, SUM(batter_runs) as total_runs
FROM deliveries
WHERE over_number BETWEEN 16 AND 20
GROUP BY batter
ORDER BY total_runs DESC
LIMIT 5;
```

### Top Wicket Takers

```sql
SELECT bowler, COUNT(*) as wickets
FROM deliveries
WHERE player_out IS NOT NULL
GROUP BY bowler
ORDER BY wickets DESC
LIMIT 5;
```

---

## 👤 Author

**Pranjal**  
Engineering Student & Sports Analytics Enthusiast  
📌 Passionate about cricket + data 🚀

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/yourprofile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/yourusername)

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⭐ If You Like This Project

- Give the repo a ⭐ on GitHub
- Share it with fellow cricket enthusiasts
- Connect with me for collaborations!

---

## 📧 Contact

For any queries or suggestions, feel free to reach out:

- 📧 Email: your.email@example.com
- 💼 LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)
- 🐦 Twitter: [@yourhandle](https://twitter.com/yourhandle)

---

<div align="center">
  
**Made with ❤️ and 🏏 by Pranjal**

</div>
