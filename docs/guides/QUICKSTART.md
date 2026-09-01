# Quick Start Guide

Get the Hospital Management System up and running in minutes!

## Prerequisites

- Node.js v14+ and npm/yarn
- Python 3.8+ (for backend if using Python)
- PostgreSQL 12+
- Redis 6+
- Git

## Option 1: Using Docker (Recommended)

### 1. Clone Repository
```bash
git clone https://github.com/XiHoyu/Hospital-Management-System.git
cd Hospital-Management-System
```

### 2. Setup Environment
```bash
cp .env.example .env
# Edit .env with your settings (use defaults for first run)
```

### 3. Start Services
```bash
docker-compose up -d
```

This will start:
- **Backend API**: http://localhost:5000
- **Web App**: http://localhost:3000
- **PostgreSQL**: localhost:5432
- **Redis**: localhost:6379

### 4. Initialize Database
```bash
docker-compose exec backend npm run migrate
docker-compose exec backend npm run seed
```

### 5. Access Application
- **Web App**: http://localhost:3000
- **API Docs**: http://localhost:5000/api/docs

---

## Option 2: Manual Setup (Development)

### 1. Clone Repository
```bash
git clone https://github.com/XiHoyu/Hospital-Management-System.git
cd Hospital-Management-System
```

### 2. Setup Environment
```bash
cp .env.example .env
# Edit .env with your local database credentials
```

### 3. Start Database Services
```bash
# PostgreSQL
createdb hospital_db

# Redis (if not running)
redis-server
```

### 4. Backend Setup
```bash
cd backend
npm install
npm run migrate
npm run seed
npm start
# Runs on http://localhost:5000
```

### 5. Web App Setup (New Terminal)
```bash
cd app/web
npm install
npm start
# Runs on http://localhost:3000
```

### 6. Mobile App Setup (Optional)

**iOS:**
```bash
cd app/mobile-app/ios
pod install
# Open in Xcode and run
```

**Android:**
```bash
cd app/mobile-app/android
# Open in Android Studio and run
```

---

## Default Credentials

**Admin Account**
- Email: `admin@hospital.com`
- Password: `Admin@123`

**Doctor Account**
- Email: `doctor@hospital.com`
- Password: `Doctor@123`

**Patient Account**
- Email: `patient@hospital.com`
- Password: `Patient@123`

**⚠️ IMPORTANT**: Change default passwords in production!

---

## Verify Installation

### Backend Health Check
```bash
curl http://localhost:5000/api/health
# Expected: { "status": "OK", "timestamp": "..." }
```

### Database Connection
```bash
# Check if migrations completed successfully
curl http://localhost:5000/api/db-status
```

### API Documentation
Visit `http://localhost:5000/api/docs` for interactive API documentation (Swagger/OpenAPI)

---

## Common Issues

### Port Already in Use
```bash
# Change port in .env
PORT=5001 npm start
```

### Database Connection Failed
```bash
# Check PostgreSQL is running
# Verify credentials in .env
# Ensure database exists: createdb hospital_db
```

### Redis Connection Failed
```bash
# Ensure Redis is running
redis-cli ping
# Should return: PONG
```

### Node Modules Issue
```bash
rm -rf node_modules package-lock.json
npm install
```

---

## Stopping Services

### Docker
```bash
docker-compose down
# With volume cleanup
docker-compose down -v
```

### Manual
- Press `Ctrl+C` in each terminal window

---

## Next Steps

1. Read `/docs/USER_GUIDE.md` to understand features
2. Review `/docs/API_DOCS.md` for API endpoints
3. Check `/docs/DEVELOPER_GUIDE.md` for development practices
4. Deploy using `/docs/DEPLOYMENT.md` when ready

---

## Need Help?

- 📖 **Documentation**: See `/docs` folder
- 🐛 **Issues**: Report on GitHub Issues
- 💬 **Questions**: Create a Discussion on GitHub

Happy coding! 🏥
