# HonourSystem

HonourSystem is an open-source web application designed to help makerspaces track consumable usage and manage tool access via RFID authentication. Users voluntarily log their usage of supplies, and the system integrates with Stripe for monthly billing. Future plans include Raspberry Pi-based tool authentication and time tracking.

## Tech Stack

### Backend
- **Framework:** .NET 8 (C#) + ASP.NET Core
- **Database:** Azure Database for PostgreSQL
- **Authentication:** Microsoft & Google logins, plus email/password
- **Payments:** Stripe API for monthly billing
- **Infrastructure:** Azure App Service (backend hosting), Azure Functions (scheduled tasks)

### Frontend
- **Framework:** Vue 3 + Nuxt 3 (Static Site Generation)
- **Deployment:** Azure Static Web Apps
- **UI Framework:** TailwindCSS or Vuetify

### RFID & Raspberry Pi Integration
- **Hardware:** Raspberry Pi with RFID readers & touch screens
- **Software:** Python (FastAPI for API integration), SQLite (local storage)
- **Sync Method:** MQTT-based real-time sync + offline logging

## Core Features

### Authentication & User Management
- Microsoft & Google login
- Email/password authentication
- RFID tag registration linked to user accounts

### Consumable Tracking
- Users log usage from a preset list of materials
- Auto-suggest frequently used items
- Batch entry for multiple consumables at once
- Optional replenishment requests after logging usage

### Payments & Billing
- Stripe integration for monthly billing
- Admins get a 5-day review period before charges finalize
- Failed payments notify both user and admin, allowing a retry
- Admin dashboard (initially using Stripe’s existing tools)

### Tool & Machine Access Control (Future Development)
- Raspberry Pi units manage machine authentication
- Users tap RFID to start/end a session
- Displays time remaining, warns about overuse
- Different machines have different monthly limits & overage costs
- Offline caching & sync for continued operation without internet

### Admin & Reporting Features
- Edit usage logs before billing cutoff
- CSV export for reports
- Future analytics dashboard for peak tool usage times

## Hosting & Deployment
- **Deployment:** Self-hostable via a GitHub "Deploy to Azure" button
- **CI/CD:** GitHub Actions for automatic updates
- **Infrastructure as Code:** Terraform for automated Azure setup

## Contributing
We welcome contributions! Please check out our issues and open pull requests.

## License
This project is licensed under the MIT License.

