# 🏏 ICC Cricket Database Project

This project is a comprehensive relational database system for managing the operations of the **International Cricket Council (ICC)**. Built using **MySQL**, the project covers everything from player management to matches, tournaments, rankings, awards, and more.

📁 **[View SQL File](https://github.com/JayeshGawde/ICCDB/blob/main/ICC%20Database.sql)**

---

## 👨‍💻 Contributors

| Name          | Roll No | Contribution           |
|---------------|---------|------------------------|
| Jayesh Gawde  | A103    | Database, SQL Queries  |
| Vansh Doshi   | A104    | Database, Report       |
| Jeet Jain     | A108    | ER Model, Database     |

---

## 📌 Project Objective

To design and implement a normalized SQL database that captures the diverse elements of ICC operations including:

- Teams, Players, and Officials
- Match schedules and results
- Tournaments and rankings
- Injuries, awards, records, and sponsors
- Disciplinary actions and broadcasting partners

---

## 🧱 Database Entities

Key entities in the schema:

- **Countries**: ICC member countries
- **Players**: Personal and career info
- **Teams**: National cricket teams
- **Officials**: ICC officials and their roles
- **Matches**: Match data with results and venues
- **Tournaments**: Hosted events and winners
- **Umpires**: Match officiating details
- **Venues**: Stadiums and capacities
- **Rankings**: Player rankings across formats
- **Awards**: Player accolades
- **Records**: Match/player records
- **Injuries**: Injury logs
- **Sponsors**: Sponsorship contracts
- **Broadcasting Partners**: Media rights data
- **Disciplinary Committee**: Actions and meetings

---

## 🔄 Normalization

All tables follow:

- **1NF**: Atomic data
- **2NF**: No partial dependencies
- **3NF / BCNF**: No transitive dependencies

This ensures data integrity, reduced redundancy, and optimized performance.

---

## 🔍 Key Features

- Fully normalized relational schema with **foreign key constraints**
- Pre-loaded **INSERT statements** for realistic cricket data
- Complex **SQL queries** demonstrating joins, filtering, and aggregation
- Supports analytics like:
  - Top-ranked players
  - Most awarded cricketers
  - Tournament histories
  - Venue capacities
  - Injury tracking

---

## 🛠️ How to Use

1. Clone or download the repo
2. Open MySQL or a compatible SQL environment
3. Run `ICC Database.sql` script
4. Query away!

---

## 🧠 Learning Outcomes

- Mastery in SQL and relational database design
- Hands-on with schema modeling and ER diagrams
- Implementation of normalization (1NF, 2NF, 3NF)
- Real-world problem mapping in cricket domain

---

## 🎯 Sample Queries

```sql
-- Top 3 umpires by matches officiated
SELECT * FROM Umpires ORDER BY MatchesOfficiated DESC LIMIT 3;

-- Players with awards in the 'Overall' category
SELECT FirstName, LastName FROM Players
JOIN Awards ON Players.PlayerID = Awards.PlayerID
WHERE Category = 'Overall';

-- Tournaments hosted outside India
SELECT * FROM BCCI_Tournaments WHERE HostCountry != 'India';
 Files
ICC Database.sql — Full database creation and data

dbms_report.pdf — Complete project documentation

README.md — GitHub overview

📚 Tech Stack
MySQL (RDBMS)

ER Modeling (Theoretical)

SQL (DDL + DML)

🏁 Conclusion
This project demonstrates how relational databases can efficiently model complex real-world domains such as international cricket management. It's a solid foundation for building further applications, such as sports analytics dashboards or management portals.

📬 Contact
Jeet Jain
📧 Email: jainjeet1310@gmail.com
🔗 GitHub: @jeet1310
