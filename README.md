# AuthSphere User Management System

A full-stack user management system built with React, Vite, Express, Drizzle ORM, and PostgreSQL.

## Features
- User registration, login, and email verification
- Admin dashboard for user management
- Profile update and password change
- Secure authentication with JWT and bcrypt
- Responsive UI with Tailwind CSS and Radix UI

## Getting Started

### 1. Clone the repository
```
git clone https://github.com/yourusername/authsphere.git
cd authsphere
```

### 2. Install dependencies
```
npm install
```

### 3. Set up environment variables
Create a `.env` file in the project root:
```
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your@email.com
SMTP_PASS=yourpassword
SMTP_FROM=your@email.com
APP_URL=http://localhost:3000
DATABASE_URL=postgres://postgres:yourpassword@localhost:5432/authsphere
```

### 4. Run database migrations
```
npm run db:push
```

### 5. Start the backend server
```
$env:DATABASE_URL="postgres://postgres:yourpassword@localhost:5432/authsphere"
$env:NODE_ENV="development"
npx tsx server/index.ts
```

### 6. Start the frontend (Vite)
```
npx vite
```

### 7. Access the app
Open [http://localhost:3000](http://localhost:3000) in your browser.

## Notes
- Do NOT commit your `.env` file with real credentials.
- Use an App Password for Gmail SMTP.
- See code comments for more details on modules and structure.

## License
MIT
