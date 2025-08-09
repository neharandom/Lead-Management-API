# Lead-Management-API
📌 Lead Management API — Node.js + Express + MySQL
A backend API for capturing and managing sales leads in the marketing sector.
Includes key features such as funnel stages, CRM sync (mock), and notes/comments to streamline your sales process.
🚀 Features
Lead capture & management — store, update, and delete leads
Funnel stages — track progress (new, contacted, qualified, proposal, won, lost)
Search & filter — find leads by stage, name, email, or phone
Notes/comments — attach follow-up notes to any lead
CRM sync (mock) — endpoint for external CRM integration
MySQL database — structured relational data storage
🛠 Tech Stack
Backend: Node.js, Express.js
Database: MySQL (mysql2 with async/await support)
UUID: for lead and note IDs
Environment Config: dotenv
📂 Project Structure
lead-management-api/
├── migrations/                 # SQL schema for database setup
├── src/
│   ├── controllers/             # Route logic
│   ├── models/                   # DB queries
│   ├── routes/                   # API endpoints
│   ├── middleware/               # Error handling
│   └── db.js                     # MySQL connection pool
├── server.js                     # App entry point
├── .env                          # Environment variables
├── package.json
└── README.md
📦 Installation & Setup
bash
Copy
Edit
git clone https://github.com/yourusername/lead-management-api.git
cd lead-management-api
npm install
cp .env.example .env
# Update database credentials in .env
npm run dev
Run migrations in MySQL:
sql
Copy
Edit
SOURCE migrations/001_create_leads_and_notes.sql;
🔗 API Endpoints
Method	Endpoint	Description
POST	/api/leads	Create new lead
GET	/api/leads	List all leads
GET	/api/leads/:id	Get lead by ID
PATCH	/api/leads/:id	Update lead
DELETE	/api/leads/:id	Delete lead
POST	/api/leads/:id/notes	Add note to lead
GET	/api/leads/:id/notes	Get notes for a lead
POST	/api/leads/:id/sync	Sync lead to CRM (mock)

