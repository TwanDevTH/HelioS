# Helio$

Helio$ is a modern, multi-user expense tracker application that allows users to log expenses through both a web interface and the LINE messaging platform. It includes categorized spending, support for multiple accounts and credit cards, and visual summaries of spending behavior.

---

## Features
- Multi-user authentication system
- Web and LINE-integrated expense input
- Support for multiple wallets/accounts (e.g., cash, credit card)
- Categorized and subcategorized expenses
- Dashboard with daily, weekly, and monthly summaries, including pie charts and graphs

---

## Project Structure
```
project-root/
├── frontend/        # React + Tailwind application
├── backend/         # Node.js + Express API
├── db/              # PostgreSQL schema and seed files
```

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/TwanDevTH/helios.git
cd helios
```

### 2. Install Dependencies
#### Backend
```bash
cd backend
npm install
```
#### Frontend
```bash
cd ../frontend
npm install
```

### 3. Configure Environment Variables
Create a `.env` file in both the `frontend/` and `backend/` directories.

#### backend/.env
```
PORT=5000
DATABASE_URL=postgresql://your_user:your_pass@localhost:5432/helios
JWT_SECRET=superSecretValue
```

#### frontend/.env
```env
REACT_APP_API_URL=http://localhost:5000/api
```

### 4. Set Up the Database
Use `psql` or `pgAdmin` to create your database and run the schema file:
```bash
cd db
psql -U your_user -d helios -f schema.sql
```

---

## Running the Application
### Backend
```bash
cd backend
npm run dev
```
### Frontend
```bash
cd frontend
npm start
```

---

## API Routes (In Progress)
### Expenses
- `POST /api/expenses`
- `GET /api/expenses?userId=xyz`

### Authentication (upcoming)
- `POST /api/auth/signup`
- `POST /api/auth/login`

---

## Technology Stack
- **Frontend:** React, TailwindCSS, Chart.js
- **Backend:** Node.js, Express
- **Database:** PostgreSQL
- **LINE Integration:** Messaging API and Webhooks

---

## Development Roadmap
- [x] Initial project scaffolding
- [ ] User authentication system
- [ ] Expense tracking API
- [ ] Frontend user interface with visualizations
- [ ] LINE chatbot integration

---

## Maintainers
Developed and maintained by TwanDevTH
