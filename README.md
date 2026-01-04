# Contact Form

A form application with file upload support

## Tech Stack

- **Frontend**: HTML/CSS/JavaScript
- **Backend**: Node.js + Express
- **Database**: SQLite
- **File Upload**: Multer

## Prerequisites

- Node.js (v14 or higher)
- npm

## Installation

1. Install dependencies:

```bash
npm install
```

## Running the Application

1. Start the server:

```bash
npm start
```

2. Open browser and navigate to:

```
http://localhost:3000
```

3. The server will create:
   - `database.db` : SQLite database file
   - `uploads/` : Directory for uploaded files

## Database Schema

```sql
CREATE TABLE submissions (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  email TEXT NOT NULL,
  message TEXT NOT NULL,
  attachment_filename TEXT,
  attachment_path TEXT,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP
)
```

## Input

1. **Name**: Required
2. **Email**: Required, must be valid email format
3. **Message**: Required, minimum 20 characters
4. **Attachment**: Optional, max 5MB, only PDF/JPG/PNG

## Stopping the Server

Press `Ctrl+C` in the terminal where the server is running.
