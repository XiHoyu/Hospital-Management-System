# Tech Stack - Hospital Management System

This document outlines the technology stack used in the Hospital Management System.

## Technology Stack Overview

### Frontend & UI
- **Framework**: Vue 3 (latest)
- **Language**: TypeScript
- **Build Tool**: Vite
- **State Management**: Pinia
- **Styling**: UnoCSS (atomic CSS framework)
- **Form Validation**: Vee-Validate + Zod
- **Router**: Vue Router 4

### Mobile Applications
- **Framework**: Capacitor
- **Web View**: Vue 3 + Vite (shared code with web)
- **iOS**: Native Swift integration via Capacitor
- **Android**: Native Kotlin integration via Capacitor
- **Package Manager**: pnpm

### Desktop Application
- **Framework**: Electron
- **UI**: Vue 3 (same as web application)
- **Build Tool**: Vite
- **Packaging**: Electron Builder
- **Supported Platforms**: Windows, macOS, Linux

### Backend API
- **Runtime**: Node.js (v18+)
- **Framework**: Express.js
- **Language**: TypeScript
- **Package Manager**: pnpm
- **Database**: DuckDB + Drizzle ORM
- **Real-time**: Socket.io
- **Authentication**: JWT

### Database
- **Primary**: DuckDB (embedded, in-process)
- **ORM**: Drizzle ORM
- **Migrations**: Custom migration scripts
- **Type-safe Queries**: Full TypeScript support

### Development & Build
- **Package Manager**: pnpm (monorepo)
- **Monorepo Tool**: Turbo
- **Testing Framework**: Vitest
- **Testing Library**: @vue/test-utils, @testing-library/vue
- **Linting**: ESLint + @antfu/eslint-config
- **Code Formatting**: Prettier
- **Type Checking**: vue-tsc

### DevOps & Deployment
- **Containerization**: Docker
- **Orchestration**: Docker Compose
- **CI/CD**: GitHub Actions (planned)

## Project Structure (Monorepo)

```
hospital-management-system/
├── apps/
│   ├── web/              # Vue 3 web application (Vite)
│   ├── mobile/           # Capacitor mobile (iOS/Android)
│   ├── desktop/          # Electron desktop application
│   └── backend/          # Express.js API server
├── packages/             # Shared packages
│   ├── database/         # Drizzle + DuckDB integration
│   ├── types/            # Shared TypeScript types
│   ├── ui/               # Shared UI components
│   └── utils/            # Shared utilities
├── docs/                 # Documentation
└── turbo.json            # Turbo configuration
```

## Key Dependencies

### Core Frameworks
- `vue@^3.3.0` - Progressive JavaScript framework
- `vue-router@^4.2.0` - Routing
- `pinia@^2.1.0` - State management
- `electron@^latest` - Desktop framework

### Data & API
- `axios@^1.6.0` - HTTP client
- `drizzle-orm@^0.28.0` - ORM
- `@duckdb/wasm@^1.28.0` - Embedded database
- `socket.io-client@^4.7.2` - Real-time communication

### Development
- `vite@^5.0.0` - Build tool
- `vitest@^1.0.0` - Unit testing
- `typescript@^5.3.0` - Type safety
- `pnpm@^9.0.0` - Package manager

### UI & Styling
- `unocss@^0.56.0` - Utility-first CSS
- `vee-validate@^4.12.0` - Form validation
- `zod@^3.22.0` - Schema validation

## Node.js Version

- **Minimum**: Node.js 18.0.0
- **Recommended**: Node.js 20.0.0+
- **Package Manager**: pnpm 9.0.0+

## Why This Stack?

1. **Consistency**: Same codebase for web, mobile (via Capacitor), and desktop (via Electron)
2. **Performance**: Vite for fast HMR, DuckDB for embedded database
3. **Type Safety**: Full TypeScript support across stack
4. **Scalability**: Monorepo structure with Turbo for easy management
5. **Developer Experience**: Modern tooling, hot reload, excellent IDE support
6. **Lightweight**: No heavy server dependencies, embedded database

## Comparison with Previous Setup

| Aspect | Before | Current |
|--------|--------|---------|
| Frontend | React | Vue 3 |
| Build | Create React App | Vite |
| Mobile | React Native | Capacitor |
| Database | PostgreSQL + Node.js | DuckDB + Drizzle |
| Package Manager | npm | pnpm |
| Monorepo | Manual scripts | Turbo |
| Testing | Jest | Vitest |

## Getting Started

Install dependencies:
```bash
pnpm install
```

Start development:
```bash
pnpm dev
```

Build all applications:
```bash
pnpm build
```

## Documentation

See the individual README files in each app directory for specific setup instructions:
- `apps/web/README.md` - Web app setup
- `apps/mobile/README.md` - Mobile app setup
- `apps/desktop/README.md` - Desktop app setup
- `apps/backend/README.md` - Backend API setup
