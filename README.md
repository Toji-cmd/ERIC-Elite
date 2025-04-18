# Gamified Learning Management System (LMS)

This project is a **Gamified LMS** platform where teachers can manage quests, track student progress, assign badges, and more in a fun, interactive environment. Built using **Node.js**, **HTML/CSS/JavaScript**, and **MySQL**.

---

## 🚀 How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/gamified-lms.git
cd gamified-lms
```

---

### 2. Install Required Applications

Before running the project, make sure you have the following installed on your system:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Node.js](https://nodejs.org/)
- [MySQL Workbench](https://www.mysql.com/products/workbench/)

---

### 3. Install Node Modules

```bash
npm install
```

---

### 4. Set Up the MySQL Database

Open **MySQL Workbench** and execute the following SQL commands:

```sql
CREATE DATABASE gamified_lms;
USE gamified_lms;

CREATE TABLE IF NOT EXISTS users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    email VARCHAR(255) NOT NULL,
    password1 VARCHAR(255) NOT NULL, -- Storing hashed passwords
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

### 5. Configure the `.env` File

Create a `.env` file in the root directory and configure it with your local database credentials. Example:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=gamified_lms
PORT=3000
```

Make sure to **replace** `your_mysql_password` with your actual MySQL password.

---

### 6. Run the Server

```bash
node server.js
```

You should see:
```
Server is running on http://localhost:3000
```

---

### 7. Frontend Access

Open your browser and go to the frontend pages inside the `frontend/` folder:

- `frontend/index.html`
- `frontend/login-signup.html`
- `frontend/dashboard.html` (after login)

---

## 📁 Folder Structure

```
.File_name
├── frontend/
│   ├──student/
│   │   ├──achievement.html
│   │   ├──dashboard.html
│   │   ├──leaderboard.html
│   │   ├──profile.html
│   │   └──quest.html
│   │
│   ├──teacher/
│   │   ├──css/
│   │   │   ├──badge-creator.css
│   │   │   ├──create-quest.css
│   │   │   ├──dashboard.css
│   │   │   ├──manage-quest.css
│   │   │   └──progress-tracker.css
│   │   ├──badge-creator.html
│   │   ├──dashboard.html
│   │   ├──create-quest.html
│   │   ├──manage-quest.html
│   │   └──progress-tracker.html
│   │
│   ├── index.html
│   ├── login-signup.html
│   └── Img/
├── server.js
├── .env
├── package.json
└── README.md
```

---

## 🛠️ Technologies Used

- Node.js & Express
- MySQL Workbench
- HTML, CSS, JavaScript
- Vercel (for deployment, if needed)

---

## 🔐 Important Notes

- Always keep your `.env` file secure. Do not commit it to public repositories.
- Make sure MySQL server is running locally before starting your Node.js server.
- Passwords are stored in hashed format (recommended to use `bcrypt` for production).

---

## ✨ Future Improvements

- Add token-based session handling
- Improve quiz and badge logic
- Integrate real-time progress updates using sockets

---

Feel free to contribute or suggest improvements!
