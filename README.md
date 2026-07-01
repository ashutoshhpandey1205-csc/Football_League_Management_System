# ⚽ Football League Management System

> A backend REST API for managing a football league — built with **Node.js**, **Express.js**, and **MongoDB**

---

## 👨‍💻 Developer

| Field | Details |
|---|---|
| **Name** | Ashutosh Shashidhar Pandey |
| **Registration Number** | 24BAI10250 |
| **Branch** | B.Tech — Artificial Intelligence & Machine Learning |
| **University** | VIT Bhopal University |
| **Year** | 3rd Year |

---

## 📌 Project Overview

The **Football League Management System** is a console-based REST API project that demonstrates complete **CRUD operations** (Create, Read, Update, Delete) using **MongoDB** as the database and **Node.js (Express.js)** as the backend framework.

The system manages 5 core entities of a football league:
- 🏟️ **Stadiums** — Famous football grounds across Europe and Saudi Arabia
- ⚽ **Teams** — Football clubs with their home stadiums
- 🧑‍💼 **Coaches** — Head coaches assigned to teams
- 🏃 **Players** — Squad players linked to their teams
- 🎯 **Matches** — Scheduled or completed matches between teams

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | Runtime environment |
| Express.js | Backend web framework |
| MongoDB | NoSQL database |
| Mongoose | ODM for MongoDB |
| dotenv | Environment variable management |
| Postman | API testing |
| MongoDB Compass | Visual database inspection |

---

## 📁 Folder Structure

```
FootballLeagueManagement/
├── config/
│   └── db.js               # MongoDB connection
├── controllers/
│   ├── stadiumController.js
│   ├── teamController.js
│   ├── coachController.js
│   ├── playerController.js
│   └── matchController.js
├── models/
│   ├── Stadium.js
│   ├── Team.js
│   ├── Coach.js
│   ├── Player.js
│   └── Match.js
├── routes/
│   ├── stadiumRoutes.js
│   ├── teamRoutes.js
│   ├── coachRoutes.js
│   ├── playerRoutes.js
│   └── matchRoutes.js
├── .env                    # Environment variables
├── package.json
└── server.js               # Main entry point
```

---

## 🔗 Database Relationships

| Relationship Type | Collections | Description |
|---|---|---|
| **One-to-One** | Team ↔ Stadium | Each team has one home stadium |
| **One-to-One** | Coach ↔ Team | Each team has one head coach |
| **Many-to-One** | Players → Team | Multiple players belong to one team |
| **Many-to-Many** | Teams ↔ Matches | Teams play multiple matches against each other |

---

## 🚀 How to Run the Project

### Prerequisites
- Node.js installed
- MongoDB running locally on port 27017

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/ashutosh24bai10250/24BAI10250_MongoDB_Project.git

# 2. Navigate to project folder
cd FootballLeagueManagement

# 3. Install dependencies
npm install

# 4. Create .env file and add:
MONGO_URI=mongodb://localhost:27017/footballleague
PORT=5000

# 5. Start the server
node server.js
```

You should see:
```
Server running on port 5000
MongoDB Connected: localhost
```

---

## 📮 API Endpoints

### 🏟️ Stadiums
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/stadiums` | Add a new stadium |
| GET | `/api/stadiums` | Get all stadiums |
| GET | `/api/stadiums/:id` | Get stadium by ID |
| PUT | `/api/stadiums/:id` | Update stadium |
| DELETE | `/api/stadiums/:id` | Delete stadium |

### ⚽ Teams
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/teams` | Register a new team |
| GET | `/api/teams` | Get all teams |
| GET | `/api/teams/:id` | Get team by ID |
| PUT | `/api/teams/:id` | Update team |
| DELETE | `/api/teams/:id` | Delete team |

### 🧑‍💼 Coaches
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/coaches` | Add a new coach |
| GET | `/api/coaches` | Get all coaches |
| GET | `/api/coaches/:id` | Get coach by ID |
| PUT | `/api/coaches/:id` | Update coach |
| DELETE | `/api/coaches/:id` | Delete coach |

### 🏃 Players
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/players` | Add a player |
| GET | `/api/players` | Get all players |
| GET | `/api/players/:id` | Get player by ID |
| PUT | `/api/players/:id` | Update player |
| DELETE | `/api/players/:id` | Delete player |

### 🎯 Matches
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/matches` | Schedule a match |
| GET | `/api/matches` | Get all matches |
| GET | `/api/matches/:id` | Get match by ID |
| PUT | `/api/matches/:id` | Update match result |
| DELETE | `/api/matches/:id` | Delete match |

---

## 📸 Screenshots

### ✅ Server Running
<!-- Add screenshot of terminal showing "Server running on port 5000" and "MongoDB Connected: localhost" -->
![Server Running](screenshots/server_running.png)

---

### 🏟️ POST — Create Stadium
<!-- Add screenshot of Postman POST /api/stadiums with 201 Created response -->
![Create Stadium](screenshots/post_stadium.png)

---

### ⚽ POST — Create Team
<!-- Add screenshot of Postman POST /api/teams with 201 Created response -->
![Create Team](screenshots/post_team.png)

---

### 🧑‍💼 POST — Create Coach
<!-- Add screenshot of Postman POST /api/coaches with 201 Created response -->
![Create Coach](screenshots/post_coach.png)

---

### 🏃 POST — Create Player
<!-- Add screenshot of Postman POST /api/players with 201 Created response -->
![Create Player](screenshots/post_player.png)

---

### 🎯 POST — Create Match
<!-- Add screenshot of Postman POST /api/matches with 201 Created response -->
![Create Match](screenshots/post_match.png)

---

### 📋 GET — Get All Stadiums
<!-- Add screenshot of Postman GET /api/stadiums response -->
![Get Stadiums](screenshots/get_stadiums.png)

---

### 📋 GET — Get All Players
<!-- Add screenshot of Postman GET /api/players response -->
![Get Players](screenshots/get_players.png)

---

### ✏️ PUT — Update a Record
<!-- Add screenshot of Postman PUT request with updated data -->
![Update Record](screenshots/put_update.png)

---

### 🗑️ DELETE — Delete a Record
<!-- Add screenshot of Postman DELETE request with success message -->
![Delete Record](screenshots/delete_record.png)

---

### 🗄️ MongoDB Compass — Database View
<!-- Add screenshot of MongoDB Compass showing footballleague database with all collections -->
![MongoDB Compass](screenshots/mongodb_compass.png)

---

## 📊 Sample Data Used

### Stadiums
- Old Trafford, Manchester (74,140 capacity)
- Spotify Camp Nou, Barcelona (99,354 capacity)
- Santiago Bernabéu, Madrid (81,044 capacity)
- Anfield, Liverpool (61,276 capacity)
- King Fahd International Stadium, Riyadh (68,752 capacity)

### Teams
- Manchester United (Founded 1878)
- FC Barcelona (Founded 1899)
- Real Madrid (Founded 1902)
- Al Nassr FC (Founded 1955)

---

## 📝 API Response Format

All responses follow this consistent format:

```json
{
  "success": true,
  "message": "Player added to the squad successfully!",
  "data": {
    "_id": "...",
    "name": "Cristiano Ronaldo",
    "age": 39,
    "position": "Forward"
  }
}
```

---

## 🎓 Submitted For

- **Course**: Database Management Systems (DBMS) — MongoDB Project
- **Institution**: VIT Bhopal University
- **Academic Year**: 2025–2026
