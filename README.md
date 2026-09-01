# Hospital Management System

A comprehensive web-based application designed to streamline hospital operations, manage patient records, and improve healthcare service delivery.

## Project Status

**Status**: Under Development

This project is currently in the planning and setup phase. Full implementation will begin soon. The folder structure, documentation, and configuration have been prepared. Development of features will start shortly.

- [ ] Backend API Development
- [ ] Web Application Development
- [ ] Mobile App (iOS) Development
- [ ] Mobile App (Android) Development
- [ ] Desktop Application Development
- [ ] Database Schema & Migrations
- [ ] Testing Suite
- [ ] Deployment & DevOps

## Table of Contents
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Features

### 1. **Patient Management**
- Patient registration and onboarding
- Complete patient demographics (name, age, contact, address)
- Emergency contact information
- Medical history tracking
- Allergies and contraindications
- Blood type and genetic information
- Insurance details and policy management
- Patient portal access
- Patient search and filtering

### 2. **Appointment Management**
- Schedule appointments with doctors
- Doctor availability calendar
- Appointment reminders (SMS/Email/Push)
- Cancellation and rescheduling
- Appointment slots management
- Queue management
- Wait time tracking
- Video consultation scheduling
- Recurring appointment management

### 3. **Doctor & Staff Management**
- Doctor registration and credentials
- Specialization management
- License and certification tracking
- Doctor availability and schedules
- Staff roles and permissions
- Performance tracking
- Leave management
- Shift scheduling
- Staff contact information
- Department assignments

### 4. **Electronic Health Records (EHR)**
- Patient medical history
- Chief complaints and diagnosis
- Treatment plans and protocols
- Clinical notes and observations
- Vital signs tracking (BP, temperature, heart rate, etc.)
- Symptoms and complaints logging
- Follow-up information
- Lab work orders and results
- Radiology reports
- Document storage and retrieval

### 5. **Prescription Management**
- Digital prescription generation
- Drug database with interactions
- Dosage calculations
- Medication history
- Refill management
- Pharmacy integration
- Drug allergies and contraindications
- OTC and prescription tracking
- Expiration date monitoring
- Prescription audit trail

### 6. **Laboratory Management**
- Lab test ordering system
- Sample collection tracking
- Test result entry and storage
- Quality control
- Lab report generation
- Barcode/QR code scanning for samples
- Test status tracking
- Critical values alerting
- Integration with testing equipment
- Lab inventory management

### 7. **Radiology & Imaging**
- Radiology order placement
- DICOM image storage and retrieval
- X-ray, CT, MRI, Ultrasound management
- Image viewing tools
- Radiologist reports
- Comparison tools (before/after)
- 3D reconstruction capabilities
- Image annotation tools
- Film library management

### 8. **Billing & Payments**
- Invoice generation
- Fee management by service/procedure
- Insurance claim management
- Payment processing (cash, card, online)
- Receipt generation
- Payment history tracking
- Refund management
- Insurance verification
- Discount and promotional codes
- Tax calculation and reporting
- Financial reports

### 9. **Inventory Management**
- Medical supplies tracking
- Equipment inventory
- Expiration date monitoring
- Automated reorder alerts
- Barcode/QR code scanning
- Stock level management
- Supplier management
- Purchase orders
- Inventory valuation
- Stock distribution across departments
- Waste tracking and disposal

### 10. **Pharmacy Management**
- Drug inventory management
- Purchase orders and supplier tracking
- Stock counting and reconciliation
- Expiration date alerts
- Prescription fulfillment
- Drug dispensing
- Stock movement history
- Pharmacy reports
- Medicine batch tracking
- Return management

### 11. **Bed Management**
- Hospital bed allocation
- Room and ward management
- Bed occupancy status
- Patient transfer tracking
- Discharge bed cleaning
- ICU/General/Private room management
- Capacity planning
- Maintenance scheduling
- Bed utilization reports

### 12. **OPD (Outpatient Department)**
- Out-patient registration
- Consultation scheduling
- Referral management
- Discharge summaries
- Prescription for OPD patients
- OPD counters management
- Token system
- Queue management

### 13. **IPD (Inpatient Department)**
- Admission process
- Ward/Room assignment
- Daily ward rounds
- Discharge planning and documentation
- Patient transfer between wards
- Hospital stay tracking
- Bed charges
- Nursing notes
- Care plans

### 14. **Emergency Department**
- Triage system
- Emergency patient registration
- Priority-based patient handling
- Emergency protocol management
- Ambulance service integration
- Critical patient monitoring
- Emergency contact notification
- Immediate action tracking

### 15. **Operation Theatre Management**
- Surgery scheduling
- Operating room management
- Surgeon and anesthesiologist scheduling
- Pre-operative checklist
- Operative notes
- Post-operative instructions
- Surgical inventory management
- Equipment sterilization tracking
- Operation theatre utilization reports

### 16. **Nursing Management**
- Nurse assignment to patients
- Nursing shift management
- Patient care plans
- Nursing notes and observations
- Medication administration records (MAR)
- Vital signs recording
- Nursing task management
- Patient monitoring

### 17. **Dietary & Nutrition**
- Diet plan management
- Dietary restrictions and allergies
- Meal planning
- Patient meal ordering
- Nutritionist consultation
- Dietary reports
- Kitchen inventory management
- Calorie and nutrient tracking

### 18. **Housekeeping & Sanitation**
- Cleaning task assignments
- Room cleaning schedules
- Waste management
- Sanitization protocols
- Staff scheduling
- Cleaning supply inventory
- Infection control tracking
- Housekeeping reports

### 19. **Medical Codes & Reference Data**
- ICD-10 codes for diagnosis
- CPT codes for procedures
- SNOMED CT coding
- Lab test codes
- Drug codes (NDC)
- Medical history templates
- Procedure templates

### 20. **Compliance & Quality Management**
- Incident reporting
- Complaint management
- Quality audits
- Regulatory compliance tracking
- Risk assessment
- Document management
- Audit logs and reports
- Patient safety protocols

### 21. **User Management & Security**
- Role-based access control (RBAC)
- User authentication (2FA, MFA)
- Department-based permissions
- User activity logging
- Data encryption
- HIPAA compliance
- Password policies
- Session management

### 22. **Communication & Messaging**
- Internal messaging system
- Doctor-Patient communication
- Notifications and alerts
- SMS/Email integration
- Appointment reminders
- Lab result notifications
- Critical alert system
- Broadcast messages

### 23. **Analytics & Reporting**
- Patient analytics
- Doctor performance reports
- Financial reports
- Occupancy reports
- Department-wise reports
- Revenue analysis
- Quality metrics
- Patient satisfaction surveys
- Custom report builder
- Data visualization and dashboards

### 24. **Integration Features**
- EMR/EHR integration
- Insurance company API integration
- Lab equipment integration
- Pharmacy system integration
- Billing system integration
- Payment gateway integration
- Email/SMS gateway integration
- Hospital website integration

### 25. **Telemedicine & Remote Services**
- Video consultation capability
- Audio consultation
- Screen sharing for medical data
- Recording consultations
- Patient appointment via video
- Remote prescription generation
- Follow-up consultations

### 26. **Mobile & Web Accessibility**
- Responsive web design
- Native iOS app
- Native Android app
- Desktop application
- Progressive Web App (PWA)
- Offline functionality
- Cross-platform sync

### 27. **Help & Support**
- Knowledge base
- FAQs
- Ticketing system
- Live chat support
- Documentation
- Video tutorials
- User training materials

## Technology Stack

### Frontend & Client Apps
- **Web Application**: Vue 3 with TypeScript + Vite
- **Mobile Apps**: Capacitor (iOS & Android with Vue 3 UI)
- **Desktop App**: Electron with Vue 3
- **Build Tool**: Vite (instant HMR)
- **State Management**: Pinia
- **UI Styling**: UnoCSS (atomic CSS)
- **HTTP Client**: Axios

### Backend & Server
- **Runtime**: Node.js (v18+)
- **Framework**: Express.js
- **Language**: TypeScript
- **Database**: DuckDB with Drizzle ORM
- **Real-time**: Socket.io
- **Authentication**: JWT

### Database & Storage
- **Primary Database**: DuckDB (embedded, in-process)
- **ORM**: Drizzle ORM (type-safe)
- **Migrations**: Custom migration scripts
- **File Storage**: Local file system (or cloud storage)

### Security & Compliance
- **Encryption**: TLS/SSL
- **API Security**: Rate limiting, CORS
- **Data Protection**: HIPAA compliance ready
- **Authentication**: JWT with secure tokens

### DevOps & Build
- **Package Manager**: pnpm (fast, efficient)
- **Monorepo Tool**: Turbo (caching, parallelization)
- **Containerization**: Docker + Docker Compose
- **CI/CD**: GitHub Actions (ready)
- **Testing**: Vitest + Vue Test Utils
- **Linting**: ESLint + Prettier

### Additional Tools
- **Real-time Communication**: Socket.io
- **Form Validation**: Vee-Validate + Zod
- **Routing**: Vue Router 4
- **Type Checking**: TypeScript + vue-tsc
- **Documentation**: Markdown + Docusaurus (planned)

For detailed information, see [TECH_STACK.md](TECH_STACK.md) and [TECH_STACK_SETUP.md](TECH_STACK_SETUP.md)

## Installation

### Prerequisites
- **Node.js**: v18.0.0 or higher
- **pnpm**: v9.0.0 or higher (package manager)
- **Git**: Latest version
- **Docker**: Optional (for backend containerization)

### Quick Start

```bash
# 1. Clone repository
git clone https://github.com/XiHoyu/Hospital-Management-System.git
cd Hospital-Management-System

# 2. Install dependencies
pnpm install

# 3. Start development
pnpm dev

# Applications will start on:
# - Web: http://localhost:5173
# - Backend API: http://localhost:3000
```

### Setup Instructions

For complete setup with troubleshooting, see [TECH_STACK_SETUP.md](TECH_STACK_SETUP.md)

#### Start Individual Apps

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

### Production Build

```bash
# Build all applications
pnpm build

# Build specific apps
pnpm -rF @hospital/web run build
pnpm -rF @hospital/backend run build
```

### Docker Setup

```bash
# Build and run with Docker Compose
docker compose up -d

# Stop services
docker compose down
```

## Usage

### For Patients
1. **Register/Login**: Create account via web app or mobile app
2. **Find Doctor**: Browse available doctors by specialization
3. **Book Appointment**: Select preferred date/time
4. **Pre-consultation**: Fill medical history
5. **Join Consultation**: Video/audio consultation with doctor
6. **Get Prescription**: Receive digital prescription via app
7. **View Records**: Access all medical records in personal portal
8. **Online Payments**: Pay bills securely through the app

### For Doctors
1. **Login Dashboard**: Access via web/mobile/desktop app
2. **View Schedule**: Check daily appointments
3. **Patient Info**: Review patient history before consultation
4. **Conduct Consultation**: Diagnose and treat patients
5. **Digital Prescription**: Issue prescriptions online
6. **Patient Records**: Update medical records and notes
7. **Lab Orders**: Order tests and view results
8. **Referrals**: Refer patients to specialists

### For Nurses
1. **Shift Management**: Check assigned shift and ward
2. **Patient Monitoring**: Monitor vital signs and patient status
3. **Care Plans**: Follow doctor's care plans for patients
4. **Medical Records**: Update nursing notes and observations
5. **Medication Administration**: Track MAR (Medication Administration Records)
6. **Patient Care**: Manage patient requests and needs

### For Administrators
1. **Dashboard**: View system-wide statistics and reports
2. **User Management**: Add/manage doctors, staff, patients
3. **Hospital Settings**: Configure hospital policies
4. **Financial Reports**: View revenue and billing reports
5. **Inventory**: Manage medical supplies and equipment
6. **Staff Scheduling**: Create shifts and schedules
7. **Audit Logs**: Monitor system activity
8. **System Maintenance**: Manage backups and updates

### For Pharmacists
1. **Prescription Orders**: Receive and review prescriptions
2. **Inventory Management**: Manage drug stock levels
3. **Dispensing**: Dispense medicines to patients
4. **Drug Interactions**: Check drug compatibility
5. **Stock Reports**: Generate inventory reports

### For Billing Staff
1. **Invoice Generation**: Create bills for treatments
2. **Payment Processing**: Record payments received
3. **Insurance Claims**: Submit insurance claims
4. **Payment Tracking**: Monitor account receivables
5. **Financial Reports**: Generate billing reports

## Project Structure

```
Hospital-Management-System/
│
├── app/                           # All client applications
│   ├── web/                       # Web application
│   │   ├── src/
│   │   ├── public/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── styles/
│   │   ├── utils/
│   │   ├── package.json
│   │   └── README.md
│   │
│   ├── mobile-app/                # Mobile applications
│   │   ├── ios/                   # iOS (Swift/Objective-C)
│   │   │   ├── Hospital-Management/
│   │   │   ├── Pods/
│   │   │   └── Podfile
│   │   │
│   │   └── android/               # Android (Kotlin/Java)
│   │       ├── app/
│   │       ├── gradle/
│   │       └── build.gradle
│   │
│   └── desktop/                   # Desktop application (Electron)
│       ├── src/
│       ├── main.js
│       ├── preload.js
│       └── package.json
│
├── backend/                       # Backend API Server
│   ├── routes/                    # API endpoints
│   ├── controllers/               # Request handlers
│   ├── models/                    # Database models
│   ├── services/                  # Business logic
│   ├── middleware/                # Express/custom middleware
│   ├── utils/                     # Helper functions
│   ├── config/                    # Configuration files
│   ├── server.js / app.py
│   ├── package.json / requirements.txt
│   └── README.md
│
├── database/                      # Database management
│   ├── migrations/                # Database migration scripts
│   ├── seeds/                     # Sample data
│   ├── schema.sql
│   └── README.md
│
├── docs/                          # Documentation
│   ├── api/                       # API documentation
│   │   ├── ENDPOINTS.md
│   │   ├── AUTHENTICATION.md
│   │   └── ERROR_CODES.md
│   │
│   ├── guides/                    # User & developer guides
│   │   ├── INSTALLATION.md
│   │   ├── USER_GUIDE.md
│   │   ├── DEVELOPER_GUIDE.md
│   │   └── DEPLOYMENT.md
│   │
│   └── database/                  # Database documentation
│       ├── SCHEMA.md
│       └── DATA_DICTIONARY.md
│
├── tests/                         # Test suites
│   ├── unit/                      # Unit tests
│   │   ├── backend/
│   │   └── frontend/
│   │
│   ├── integration/               # Integration tests
│   │   └── api/
│   │
│   └── e2e/                       # End-to-end tests
│       ├── scenarios/
│       └── utils/
│
├── config/                        # Configuration files
│   ├── development.env
│   ├── production.env
│   ├── testing.env
│   ├── database.config.js
│   └── app.config.js
│
├── scripts/                       # Utility scripts
│   ├── setup.sh / setup.ps1      # Project setup script
│   ├── deploy.sh / deploy.ps1    # Deployment script
│   ├── migrate.sh / migrate.ps1  # Database migration script
│   └── seed.sh / seed.ps1        # Seed database script
│
├── .github/
│   └── workflows/                # CI/CD workflows
│       ├── test.yml
│       ├── build.yml
│       └── deploy.yml
│
├── .gitignore
├── docker-compose.yml             # Docker configuration
├── Dockerfile
├── package.json                   # Root package.json for monorepo
├── LICENSE
└── README.md
```

### Folder Descriptions

| Folder | Purpose |
|--------|---------|
| **app/** | All client-side applications (Web, iOS, Android, Desktop) |
| **backend/** | API server and business logic |
| **database/** | Database schemas, migrations, and seed data |
| **docs/** | Complete project documentation |
| **tests/** | Unit, integration, and end-to-end tests |
| **config/** | Environment configurations and app settings |
| **scripts/** | Automation and deployment scripts |
| **.github/workflows/** | GitHub Actions for CI/CD pipelines |

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style Guidelines
- Follow consistent indentation (2 or 4 spaces)
- Use meaningful variable and function names
- Add comments for complex logic
- Write unit tests for new features

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact & Support

For questions or support, please reach out to:
- **GitHub Issues**: [Create an issue](https://github.com/XiHoyu/Hospital-Management-System/issues)
- **Email**: [Your contact email]

## 🙏 Acknowledgments

- Thanks to all contributors who have helped with this project
- [Any libraries, frameworks, or resources you want to credit]

---

**Last Updated**: 2026-09-01