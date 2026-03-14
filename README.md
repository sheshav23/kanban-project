# Kanban Board (MEVN Stack)

## Project Overview

This project is a draggable Kanban board built using the **MEVN stack (MongoDB, Express.js, Vue.js, Node.js)**.
Users can create, move, and manage tasks across different columns using drag-and-drop functionality.

---

# Project Structure

```
kanban-project
│
├── backend
│   ├── models
│   ├── routes
│   ├── server.js
│   └── seed.js
│
├── frontend
│   ├── src
│   ├── index.html
│   └── package.json
│
├── seed_remote.js
└── vercel.json
```

---

# Setup Instructions

## 1. Clone the Repository

```
git clone https://github.com/sheshav23/kanban-project.git
cd kanban-project
```

---

# Running the Backend

1. Navigate to the backend folder

```
cd backend
```

2. Install dependencies

```
npm install
```

3. Start the server

```
node server.js
```

The backend will run on:

```
http://localhost:5000
```

---

# Running the Frontend

1. Navigate to the frontend folder

```
cd frontend
```

2. Install dependencies

```
npm install
```

3. Start the development server

```
npm run dev
```

The frontend will run on:

```
http://localhost:5173
```

---

# Seeding the Database

To populate the database with sample Kanban tasks, run:

```
node seed.js
```

or

```
node seed_remote.js
```

This will create initial boards and tasks in the database.

---

# Data Flow Explanation

The data flow between the **Vue frontend** and the **Node.js backend** follows a REST API architecture.

1. The **Vue frontend** sends HTTP requests (GET, POST, PUT, DELETE) to the backend using API calls.

2. The **Node.js + Express backend** receives these requests and processes them through defined routes.

3. The backend interacts with **MongoDB** using models defined in the `models` directory.

4. After performing operations (create task, update task status, delete task, etc.), the backend sends JSON responses back to the frontend.

5. The Vue frontend updates the UI dynamically based on the response, allowing real-time task movement and board updates.

Example Flow:

```
User Action (Drag Task)
        ↓
Vue Frontend
        ↓
API Request → Node.js/Express Backend
        ↓
MongoDB Database
        ↓
JSON Response
        ↓
Frontend UI Updates
```

---

# Technologies Used

* Vue.js
* Node.js
* Express.js
* MongoDB
* Vite
* JavaScript

---

# Author

Sheshav Sharma
