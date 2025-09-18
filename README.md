# KhoHangCuaBan - Setup & Running Guide

## Quick Start Guide

### Prerequisites
- **Node.js** (v10+) - [Download](https://nodejs.org/)
- **npm** (comes with Node.js)

### 3 Simple Steps to Run

```bash
# Step 1: Navigate to project
cd KhoHangCuaBan

# Step 2: Install dependencies
npm install

# Step 3: Start application
npm start
```

✅ **Application runs at:** http://localhost:3000

---

## Detailed Installation Guide

### Step 1: Check Node.js Installation
```bash
node --version
npm --version
```
If not installed, download from [nodejs.org](https://nodejs.org/)

### Step 2: Navigate to Project Directory
```bash
cd /Users/quanganh/PTTKPM/KhoHangCuaBan
```
Or wherever your project is located.

### Step 3: Install Project Dependencies
```bash
npm install
```
This installs all required packages listed in `package.json`:
- Express.js (web framework)
- MySQL (database)
- Passport (authentication)
- Handlebars (templating)
- And more...

### Step 4: Database Configuration
The app connects to a remote MySQL database by default:
- **Host:** db4free.net
- **Database:** khohangcuaban
- **User:** khohangcuaban
- **Password:** khohangcuaban

To use local database, edit `config.js`:
```javascript
module.exports = {
    mysql: {
        host: 'localhost',
        port: '3306',
        user: 'root',
        pass: 'your-password',
        database: 'khohangcuaban'
    },
}
```

### Step 5: Run the Application

#### Normal Mode:
```bash
npm start
```

#### Development Mode (auto-restart on changes):
```bash
npm run devstart
```

### Step 6: Access the Application
Open browser and go to:
```
http://localhost:3000
```

---

## Common Commands

| Command | Description |
|---------|------------|
| `npm install` | Install all dependencies |
| `npm start` | Start production server |
| `npm run devstart` | Start development server |
| `Ctrl+C` | Stop the server |

---

## Project Structure
```
KhoHangCuaBan/
├── app.js           # Main application
├── bin/www          # Server configuration
├── config.js        # Database settings
├── controller/      # Business logic
├── models/          # Data models
├── routes/          # URL routing
├── views/           # HTML templates
├── public/          # Static files (CSS/JS)
└── package.json     # Dependencies
```

---

## Troubleshooting

### Problem: "Port 3000 already in use"
**Solution:**
```bash
# Use different port
PORT=3001 npm start
```

### Problem: "Cannot connect to database"
**Solution:**
1. Check internet connection
2. Verify credentials in `config.js`
3. Try local database instead

### Problem: "Module not found"
**Solution:**
```bash
# Reinstall dependencies
rm -rf node_modules
npm install
```

### Problem: "Permission denied"
**Solution:**
```bash
# On Mac/Linux
sudo npm install
```

---

## Features Overview

- 📦 **Warehouse Management** - Manage warehouse inventory
- 📊 **Product Management** - Add, edit, delete products
- 👤 **User Authentication** - Secure login system
- 📈 **Reports** - Generate inventory reports
- 🔍 **Search** - Find products quickly

---

## Development Tips

1. **Use nodemon** for auto-restart during development:
   ```bash
   npm run devstart
   ```

2. **Check logs** in terminal for debugging

3. **Database tools:**
   - MySQL Workbench
   - phpMyAdmin
   - HeidiSQL

4. **Test endpoints** with:
   - Browser
   - Postman
   - curl

---

## Security Notes

⚠️ **For Production:**
- Change database credentials
- Use environment variables
- Enable HTTPS
- Add input validation
- Implement rate limiting

---

## Stop the Application

To stop the server:
- **Windows/Linux:** Press `Ctrl + C`
- **Mac:** Press `Cmd + C`

---

## Need Help?

1. Check error messages in terminal
2. Verify Node.js is installed: `node --version`
3. Ensure you're in correct directory
4. Check if port 3000 is free
5. Verify internet connection for database

---

**Project:** KhoHangCuaBan (Warehouse Management)  
**Technology:** Node.js + Express + MySQL  
**Port:** 3000  
**Last Updated:** September 2025