# ⚽ Tableau Dashboard – Visual Analytics Problem Set #8 

This Tableau dashboard visualizes penalty shootout data from FIFA World Cups (1982–2022) using a custom background image of a goalpost. Each penalty kick is mapped by X/Y coordinates, and users can filter results by year and tournament phase.

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `Problem_Set_8_WorldCup_Shootouts.twbx` | Tableau workbook with full interactive dashboard |
| `goal_dashboard_screenshot.png` | (Optional) Image preview of the final dashboard layout |

---

## 📊 Dataset Overview

**Source:** Provided `World Cup Shootout.csv` file  
**Fields Used:**
- `World Cup Year`, `Phase`, `Match`
- `Penalty Sequence`, `Penalty Result`, `Penalty Coordinates (X, Y)`
- `Player Name`, `Goalkeeper`, `Extra Time Score`, `Penalty Score`, `Host Country`

---

## 🧠 Dashboard Objective

- Visually map each penalty kick’s location and result onto a goalpost image
- Allow filtering by World Cup year and knockout round phase
- Display key match metrics (ET score, penalty score, final score, winning team)
- Present rich tooltips with match-level details

---

## 🛠️ Techniques Used

### 🥅 1. Penalty Map on Goal Image
- Used X and Y coordinates to accurately plot kick locations
- Background image of a goal uploaded and aligned
- X/Y axis ranges fixed for consistent scaling across filters
- Result-based coloring for `Scored`, `Missed`, and `Saved` kicks

### 📅 2. Year & Phase Filtering with Parameters
- Parameter: `Select World Cup Year` (values from 2022 to 1982)
- `Selected Year Filter` calculated field applied across the workbook
- Custom calculated field: `Available Phases` to ensure only relevant phases appear in the filter dropdown
- Phase filter excludes NULLs and unused values

### 🧮 3. Score & Winner Logic
- Four separate sheets:
  - Extra Time Score
  - Penalty Score
  - Final Score
  - Winning Team
- Final score created using `LEFT`, `RIGHT`, and `LEN()` functions to extract and sum score parts
- Winning team derived based on score comparison

### 🏷️ 4. Tooltip Enhancements
Each penalty circle includes a tooltip showing:
- Phase & Match
- Penalty sequence number
- Result (Scored/Missed/Saved)
- Kicker and Goalkeeper names
- Score at the time of the kick

---

## 🧾 Dashboard Features

- 🧭 Consistent X/Y alignment across all matches and years
- 🎯 Dynamic filtering with no irrelevant or empty values
- 📊 Integrated match score panels for complete storytelling
- ✨ Clean, minimal layout with floating titles, filter boxes, and sheets

---

## 📫 Connect with Me

- 🌐 [LinkedIn – Praneth Nandeesh](https://www.linkedin.com/in/praneth-nandeesh-789038285/)
- 📊 [Kaggle Dashboards](https://www.kaggle.com/pranethhh)
- ✉️ Email: pranethnandeesh@gmail.com

---

## 📌 License

This project is part of my Visual Analytics coursework and is shared for educational and portfolio purposes.
