# 📝 Todo List App

A full-stack todo list application with a built-in calendar view, built with Node.js, Express, PostgreSQL, and EJS.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-B4CA65?style=flat&logo=ejs&logoColor=white)

## Features

- ✅ Add tasks with an optional due date
- 🗑️ Delete tasks instantly via checkbox
- ✏️ Edit task titles inline without page reload
- 📅 Calendar view showing tasks on their scheduled dates
- ⚡ All actions update the UI without refreshing the page

## Tech Stack

- **Backend:** Node.js, Express
- **Database:** PostgreSQL (NeonDB for production)
- **Templating:** EJS
- **Hosting:** Vercel

## Getting Started

### Prerequisites

- Node.js v18+
- PostgreSQL database (local or [NeonDB](https://neon.tech))

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory:
   ```env
   DB_USER=your_db_user
   DB_HOST=your_db_host
   DB_NAME=your_db_name
   DB_PASSWORD=your_db_password
   DB_PORT=5432
   ```

4. Set up the database table:
   ```sql
   CREATE TABLE items (
     id SERIAL PRIMARY KEY,
     title VARCHAR(255) NOT NULL,
     date DATE
   );
   ```

5. Start the server:
   ```bash
   node index.js
   ```

6. Open your browser and visit `http://localhost:3000`

## Deploying to Vercel

1. Push your code to GitHub.
2. Import the repository on [Vercel](https://vercel.com).
3. Add your environment variables (`DB_USER`, `DB_HOST`, `DB_NAME`, `DB_PASSWORD`, `DB_PORT`) in the Vercel project settings under **Environment Variables**.
4. Deploy.

> **Note:** Make sure your NeonDB instance allows connections from Vercel's IP ranges. NeonDB works out of the box with Vercel — just enable the SSL option, which is already handled in `index.js`.

## Environment Variables

| Variable | Description |
|---|---|
| `DB_USER` | PostgreSQL username |
| `DB_HOST` | Database host |
| `DB_NAME` | Database name |
| `DB_PASSWORD` | Database password |
| `DB_PORT` | Database port (default: 5432) |

## Project Structure

```
├── public/              # Static assets (CSS, icons)
├── views/
│   ├── partials/
│   │   ├── header.ejs
│   │   └── footer.ejs
│   └── index.ejs        # Main template
├── index.js             # Express server & API routes
├── .env                 # Environment variables (not committed)
└── package.json
```

## License

MIT
