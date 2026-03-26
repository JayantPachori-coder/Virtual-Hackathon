# 🚀 Virtual Hackathon Tracker

### 💼 Database Project 
---

## 🌐 Project Overview

The **Virtual Hackathon Tracker** is a structured database system designed to simulate a real-world hackathon environment. It efficiently manages teams, participants, submissions, evaluations, and prize distribution.

This project highlights my ability to design scalable databases and implement efficient SQL queries for real-world applications.

---

## 🧩 Problem Statement

Managing hackathons manually can lead to:

* Data inconsistency
* Difficulty in tracking submissions
* Complex evaluation workflows

👉 This project solves these problems using a **normalized relational database system**.

---

## 💡 Key Features

✨ Team & Participant Management
✨ Hackathon Event Tracking
✨ Project Submission System
✨ Judge Evaluation & Scoring
✨ Prize & Ranking Management

---

## 🛠️ Tech Stack

| Category       | Technology Used                |
| -------------- | ------------------------------ |
| Database       | MySQL                          |
| Query Language | SQL                            |
| Tools          | MySQL Workbench                |
| Design         | ER Modeling, Relational Schema |

---

## 🏗️ System Architecture

### 📊 Database Entities

* Team
* Participant
* Hackathon
* Submission
* Judge
* Evaluation
* Prize

### 🔗 Relationships

* One-to-Many → Team → Participants
* One-to-Many → Hackathon → Submissions
* Many-to-Many → Judge ↔ Submission (via Evaluation)

---

## 🧠 Core Concepts Demonstrated

* ✔ Database Normalization (up to 3NF)
* ✔ ER Diagram Design
* ✔ Relational Schema Conversion
* ✔ Primary & Foreign Keys
* ✔ SQL Joins & Aggregations
* ✔ Data Integrity Management

---

## 📂 Project Structure

```bash
Virtual-Hackathon-Tracker/
│
├── 📄 README.md
├── 🧠 ER_Diagram.png
├── 🗄️ Schema.sql
├── 📊 Sample_Data.sql
├── 🔍 Queries.sql
├── 📸 Screenshots/
│   ├── tables.png
│   ├── queries.png
│
└── 📘 Report.pdf
```

---

## 🔍 Sample Queries

### 🥇 Top 3 Projects

```sql
SELECT project_title, score
FROM Submission s
JOIN Evaluation e ON s.submission_id = e.submission_id
ORDER BY score DESC
LIMIT 3;
```

### 👥 Participants Per Team

```sql
SELECT team_id, COUNT(*) AS total_participants
FROM Participant_details
GROUP BY team_id;
```

### 🚫 Teams Without Submissions

```sql
SELECT t.team_name
FROM Team t
LEFT JOIN Submission s ON t.team_id = s.team_id
WHERE s.submission_id IS NULL;
```

---

## 📈 Impact / What This Shows

* Designed a **scalable database system**
* Solved **real-world data management problems**
* Improved **query performance using structured SQL**
* Demonstrated **strong DBMS fundamentals**

---

## 🚧 Challenges & Solutions

| Challenge                 | Solution                         |
| ------------------------- | -------------------------------- |
| Many-to-Many relationship | Used Evaluation as bridge table  |
| Complex queries           | Used JOINs & aggregation         |
| Schema design             | Applied normalization principles |

---

## 🔮 Future Enhancements

* 🌐 Web dashboard (React.js)
* ⚙️ Backend integration (FastAPI / Node.js)
* 🤖 AI-based analytics for hackathon results
* 🔐 Authentication system

---

## 👨‍💻 About Me

**Jayant Pachori**
🎓 B.Tech CSE | NIIT University
💡 Interested in Data Science, Backend Development & AI

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!

---
