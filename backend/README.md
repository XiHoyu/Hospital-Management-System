# Backend Setup Guide

This directory contains the backend API server for the Hospital Management System.

## Technology Stack
- **Runtime**: Node.js (v14+) or Python 3.8+
- **Framework**: Express.js or Django/Flask
- **Database**: PostgreSQL
- **Cache**: Redis
- **Testing**: Jest or Pytest

## Directory Structure

- `routes/` - API endpoint definitions
- `controllers/` - Request handlers and business logic
- `models/` - Database models and schemas
- `services/` - Business logic and data processing
- `middleware/` - Express middleware (auth, validation, error handling)
- `utils/` - Helper functions and utilities
- `config/` - Configuration files

## Installation

```bash
# Install dependencies
npm install
# or
pip install -r requirements.txt

# Setup environment
cp .env.example .env
# Edit .env with your configuration

# Run database migrations
npm run migrate
# or
python manage.py migrate

# Seed initial data (optional)
npm run seed
# or
python manage.py seed
```

## Running the Server

### Development
```bash
npm run dev
# or
python app.py
```

### Production
```bash
npm start
# or
gunicorn app:app
```

Server will run on `http://localhost:5000`

## API Documentation

See `/docs/api/ENDPOINTS.md` for complete API documentation.

## Testing

```bash
# Run all tests
npm test

# Run with coverage
npm run test:coverage

# Run specific test file
npm test -- tests/unit/auth.test.js
```

## Database Management

### Run Migrations
```bash
npm run migrate
npm run migrate:up
npm run migrate:down
```

### Seed Database
```bash
npm run seed
```

### Database Backup
```bash
npm run db:backup
```

## Environment Variables

See `.env.example` for all available configuration options.

Critical variables:
- `NODE_ENV` - Environment (development/production)
- `PORT` - Server port
- `DB_HOST`, `DB_PORT`, `DB_NAME` - Database connection
- `JWT_SECRET` - JWT signing key
- `REDIS_HOST`, `REDIS_PORT` - Redis cache

## Deployment

### Docker
```bash
docker build -t hospital-backend .
docker run -p 5000:5000 hospital-backend
```

### Manual Deployment
```bash
npm ci --production
npm start
```

See `/docs/guides/DEPLOYMENT.md` for detailed deployment instructions.

## Troubleshooting

### Database Connection Issues
- Verify PostgreSQL is running
- Check DB_HOST, DB_PORT, DB_NAME in .env
- Ensure database user has permissions

### Redis Connection Issues
- Verify Redis is running on the configured port
- Check REDIS_HOST and REDIS_PORT

### Port Already in Use
```bash
# Change PORT in .env or pass as environment variable
PORT=5001 npm start
```

## Contributing

See `/docs/guides/DEVELOPER_GUIDE.md` for contribution guidelines.
