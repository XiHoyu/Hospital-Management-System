# Tech Stack Setup Guide

This guide explains how to set up your development environment for the Hospital Management System.

## Prerequisites

### Required
- **Node.js**: v18.0.0 or higher (v20+ recommended)
- **pnpm**: v9.0.0 or higher (package manager)
- **Git**: Latest version
- **Docker**: Optional, for containerized backend

### Installation

#### 1. Install Node.js
Download from: https://nodejs.org/

Verify installation:
```bash
node --version
npm --version
```

#### 2. Install pnpm
```bash
npm install -g pnpm@latest

# Verify
pnpm --version
```

#### 3. Clone Repository
```bash
git clone https://github.com/XiHoyu/Hospital-Management-System.git
cd Hospital-Management-System
```

## Project Structure

The project uses a monorepo structure with Turbo:

```
apps/
├── web/              # Vue 3 web application
├── mobile/           # Capacitor mobile app
├── desktop/          # Electron desktop app
└── backend/          # Express.js API server

packages/
├── database/         # Shared database layer
├── types/            # Shared TypeScript types
├── ui/               # Shared UI components
└── utils/            # Shared utilities
```

## Setup Instructions

### Step 1: Install Dependencies

```bash
# Install all dependencies for the entire monorepo
pnpm install

# This will:
# - Install pnpm in the root workspace
# - Link packages in the workspace
# - Create symlinks for local dependencies
```

### Step 2: Understand pnpm Commands

Key pnpm commands:

```bash
# Run scripts in all packages
pnpm -r run <script>

# Run scripts only in specific packages
pnpm -rF @hospital/web run dev
pnpm -rF @hospital/backend run dev

# Install packages in a specific app
pnpm --filter @hospital/web add <package-name>

# Run commands in parallel
pnpm -r --parallel run test
```

### Step 3: Start Development

#### Start All Services
```bash
pnpm dev
```

This uses Turbo to run all dev scripts in parallel:
- Web app on http://localhost:5173 (Vite default)
- Backend API on http://localhost:3000
- Mobile web preview available
- Desktop app dev mode

#### Start Individual Services

**Web Application:**
```bash
pnpm -rF @hospital/web run dev
# Access: http://localhost:5173
```

**Backend API:**
```bash
pnpm -rF @hospital/backend run dev
# Access: http://localhost:3000
```

**Mobile App (Web Preview):**
```bash
pnpm -rF @hospital/mobile run dev:web
# Access: http://localhost:5173
```

**Mobile App (iOS):**
```bash
pnpm -rF @hospital/mobile run dev:ios
```

**Mobile App (Android):**
```bash
pnpm -rF @hospital/mobile run dev:android
```

**Desktop App:**
```bash
pnpm -rF @hospital/desktop run dev
```

### Step 4: Build for Production

```bash
# Build all applications
pnpm build

# Build specific apps
pnpm -rF @hospital/web run build
pnpm -rF @hospital/backend run build
pnpm -rF @hospital/desktop run build:electron
```

### Step 5: Running Tests

```bash
# Run all tests
pnpm test

# Run tests in watch mode
pnpm test

# Run tests once
pnpm test:run

# Run tests with coverage
pnpm test -- --coverage
```

### Step 6: Code Quality

```bash
# Type checking
pnpm typecheck

# Linting
pnpm lint

# Fix linting issues
pnpm lint:fix
```

## Technology Breakdown

### Vue 3 + Vite (Web & Mobile)
- **Framework**: Vue 3 with Composition API
- **Build**: Vite (instant HMR)
- **File extensions**: `.vue` (Single File Components)
- **Language**: TypeScript by default

### Backend (Express.js)
- **Framework**: Express.js
- **Database**: DuckDB with Drizzle ORM
- **Real-time**: Socket.io
- **API**: RESTful endpoints

### Desktop (Electron)
- **Framework**: Electron
- **UI**: Same Vue 3 app as web
- **Packaging**: Electron Builder for Windows/macOS/Linux

### Mobile (Capacitor)
- **Framework**: Capacitor (web-to-native bridge)
- **UI**: Same Vue 3 app as web
- **Platforms**: iOS and Android
- **Deployment**: Native app stores (App Store, Google Play)

## Common Issues & Solutions

### Issue: pnpm not found
```bash
npm install -g pnpm@latest
```

### Issue: Port already in use
Vite default is 5173, backend is 3000. Change in `.env` or command:
```bash
VITE_PORT=5174 pnpm -rF @hospital/web run dev
```

### Issue: Node modules broken
```bash
# Clean reinstall
pnpm clean
rm -rf node_modules pnpm-lock.yaml
pnpm install
```

### Issue: TypeScript errors
```bash
# Check all types
pnpm typecheck

# Update TypeScript
pnpm -r update typescript
```

## Next Steps

1. **Read Tech Stack Guide**: See `TECH_STACK.md`
2. **Setup Backend**: Read `apps/backend/README.md`
3. **Setup Web App**: Read `apps/web/README.md`
4. **Setup Mobile**: Read `apps/mobile/README.md`
5. **Setup Desktop**: Read `apps/desktop/README.md`

## Useful Resources

- **Vue 3 Docs**: https://vuejs.org
- **Vite Docs**: https://vitejs.dev
- **Pnpm Docs**: https://pnpm.io
- **Turbo Docs**: https://turbo.build
- **Capacitor Docs**: https://capacitorjs.com
- **Electron Docs**: https://www.electronjs.org
- **Express Docs**: https://expressjs.com
- **Drizzle ORM Docs**: https://orm.drizzle.team
- **DuckDB Docs**: https://duckdb.org

## Monorepo Workflow Tips

1. **Adding dependencies to a specific app:**
   ```bash
   pnpm --filter @hospital/web add vue-router
   ```

2. **Using local packages in other packages:**
   Dependencies are auto-linked in `pnpm-workspace.yaml`

3. **Debugging with Turbo:**
   ```bash
   pnpm build --verbose
   pnpm dev -- --verbose
   ```

4. **Clearing cache:**
   ```bash
   pnpm turbo prune --docker
   ```

## Getting Help

- Check individual app READMEs
- Review `TECH_STACK.md` for architecture
- Check GitHub Issues
- Review code comments and JSDoc

Happy developing! 🚀
