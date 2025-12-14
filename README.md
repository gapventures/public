
# TeamSyncAI

An AI-powered Progressive Web App (PWA) that automates team management for amateur sports coaches. TeamSyncAI acts as your "Assistant Manager," using AI to handle player communication, availability tracking, and smart reminder campaigns.

## Overview

Managing an amateur sports team involves countless hours of coordination—confirming player availability, sending reminders, tracking attendance, and handling last-minute changes. TeamSyncAI automates these tasks, letting coaches focus on what matters: coaching.

## Key Features

### Smart Player Communication
- **Automated SMS Campaigns** - Send customizable reminder campaigns via SMS with smart scheduling
- **Reliability-Based Targeting** - AI calculates player reliability scores and adjusts reminder frequency accordingly
- **TCPA-Compliant Messaging** - Built-in opt-out tracking and consent management
- **Multi-Provider SMS** - Supports Twilio with abstraction layer for easy provider switching

### Team Management
- **Player Roster Management** - Import players via CSV, individual entry, or contacts
- **Role-Based Access Control** - Coach, Assistant Coach, Player, and Parent roles
- **Parent Profiles** - Parents can manage multiple child players and RSVP on their behalf
- **Team Invitations** - Streamlined workflow with customizable invitation messages

### Event & Schedule Management
- **Event Creation & Editing** - Full event lifecycle with Google Maps location autocomplete
- **Custom Event Fields** - Define team-specific fields for events
- **iCalendar Subscriptions** - Sync team schedules with personal calendars
- **Attendance Tracking** - Track RSVPs and actual attendance

### AI-Powered Features
- **Smart Lineup Generation** - AI-powered lineup suggestions for Baseball/Softball (tier-gated)
- **Natural Language Processing** - Powered by Google Gemini AI
- **Reliability Scoring** - Automatic calculation based on RSVP accuracy and attendance history

### Free Lineup Card Geneator and Playing Time Calculator
- **Public Marketing Tool** - Free lineup generator available without signup
- **PDF Export with Email Delivery** - Generates two professional PDF documents:
- **Lineup Card (5.5" x 8.5")** - Compact dugout card with batting order, reserves, pitching rotation, and game details
- **Playing Time Grid** - Detailed inning-by-inning position assignments with fairness alerts
- **Fairness Engine** - Ensures equal playing time distribution across all players
- **Auto-Balance Feature** - One-click lineup balancing for fair playing time
- **Lead Capture** - Email collection for lineup delivery and marketing follow-up

###  Email Notifications
- **SendGrid Integration** -Transactional emails for key user touchpoints
- **Welcome Emails** - Sent on user registration
- **Team Invitations** - Email invites alongside SMS with join links
- **Payment Confirmations** - Automated receipts for completed payments
- **Lineup Card Delivery** - PDF attachments sent directly to user's inbox

###  Digital Signatures
- **SendGrid Integration**  Secure payment requests with automated confirmations
-  **Pay-Per-Usage Billing** - SMS cost tracking with campaign cost estimations
-  **Team Usage Dashboards** - Monitor SMS usage and costs per team

### Payment Processing
- **Helcim Integration** - Secure payment requests with automated confirmations
- **Pay-Per-Usage Billing** - SMS cost tracking with campaign cost estimations
- **Team Usage Dashboards** - Monitor SMS usage and costs per team

### Administration
- **Global Admin Center** - Manage users, settings, and platform configuration
- **Editable Marketing Pages** - Customize landing, about, features, pricing, and contact pages
- **Membership Tier System** - Flexible plans with feature gating
- **Phone Number Management** - Provision dedicated Twilio numbers per team

### Mobile-First Design
- **Progressive Web App** - Installable on mobile devices
- **Offline Capabilities** - Core features available without connectivity
- **Responsive UI** - Optimized for both desktop and mobile experiences
- **Dark/Light Theme** - User-configurable theme preference

## Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and builds
- **TanStack Query** for data fetching and caching
- **Wouter** for client-side routing
- **Tailwind CSS** with shadcn/ui components
- **Framer Motion** for animations

### Backend
- **Node.js** with Express.js
- **TypeScript** throughout
- **PostgreSQL** (Neon serverless) for data persistence
- **Drizzle ORM** for type-safe database operations
- **Passport.js** for authentication

### Integrations
- **Twilio** - SMS messaging
- **SendGrid** - Transactional email with PDF attachments
- **Helcim** - Payment processing
- **Google Gemini AI** - Natural language processing
- **Google Maps Places API** - Location autocomplete
- **UploadThing** - File uploads
- **DocuSeal** - Digital signature management
- **PDFKit** - Server-side PDF generation

## Architecture Highlights

### Security
- Role-based permission middleware
- Server-side session management with PostgreSQL
- Secure password hashing with bcrypt
- TCPA-compliant SMS handling with opt-out tracking

### Data Model
- Multi-tenant architecture with team isolation
- Canonical contact matching prevents duplicate players
- Comprehensive audit logging for SMS messages

### Scalability
- RESTful API design
- Cron-based scheduler for automated reminders
- Idempotent webhook processing for payments

## Screenshots

<img width="1148" height="896" alt="image" src="https://github.com/user-attachments/assets/562461f0-6568-4fb9-9634-b72607087c5c" />
<img width="1080" height="2424" alt="101826" src="https://github.com/user-attachments/assets/1f84c1be-a9be-409c-9849-1f27284a0c70" />
<img width="1080" height="2424" alt="101825" src="https://github.com/user-attachments/assets/9fe50e53-e5ba-45fd-ba4a-05340dd905a3" />
<img width="1080" height="2424" alt="101822" src="https://github.com/user-attachments/assets/75ca6b4a-108a-4022-a629-bc5a3a252444" />
<img width="1909" height="840" alt="image" src="https://github.com/user-attachments/assets/060138a4-274a-41a8-aee5-02e8a1729cbf" />




## Getting Started

### Prerequisites
- Node.js 20+
- PostgreSQL database
- Twilio account (for SMS)
- Google Cloud API key (for Maps and Gemini AI)



## Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── hooks/         # Custom React hooks
│   │   ├── lib/           # Utilities and helpers
│   │   └── pages/         # Page components
├── server/                 # Express backend
│   ├── routes.ts          # API endpoints
│   ├── storage.ts         # Database operations
│   ├── scheduler.ts       # Cron job handling
│   └── twilio.ts          # SMS provider abstraction
├── shared/                 # Shared types and schemas
│   └── schema.ts          # Drizzle ORM schema
└── design_guidelines.md   # UI/UX design system
```

## License

This project is proprietary software. All rights reserved.

## Contact

For inquiries about TeamSyncAI, please use the contact form on the application.
