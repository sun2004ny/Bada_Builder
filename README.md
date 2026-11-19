<div align="center">

# 🏢 BADA BUILDER (बड़ा बिल्डर)
### *Next-Generation Full-Stack Real-Estate Marketplace & Multi-Role Operations Ecosystem*

[![Live Demo](https://img.shields.io/badge/Live_Platform-bada--builder--frontend.vercel.app-00C7B7?style=for-the-badge&logo=vercel&logoColor=white)](https://bada-builder-frontend.vercel.app)
[![React](https://img.shields.io/badge/React-18%20%7C%2019-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-6.3-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B%20LTS-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.18-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon%20%2F%20RDS-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![AWS](https://img.shields.io/badge/AWS-EC2%20%7C%20S3%20%7C%20RDS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Razorpay](https://img.shields.io/badge/Payments-Razorpay%20Integrated-02042B?style=for-the-badge&logo=razorpay&logoColor=3395FF)](https://razorpay.com/)
[![Socket.io](https://img.shields.io/badge/WebSockets-Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)](https://socket.io/)
[![License](https://img.shields.io/badge/License-ISC-green?style=for-the-badge)](LICENSE)

<p align="center">
  <a href="#-project-overview">Overview</a> •
  <a href="#-system-architecture">Architecture</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-key-modules--features">Features</a> •
  <a href="#-frontend--backend-structure">Structure</a> •
  <a href="#-api-documentation">API Docs</a> •
  <a href="#-database-design">Database</a> •
  <a href="#-installation--setup-guide">Setup Guide</a> •
  <a href="#-security-implementation">Security</a>
</p>

</div>

---

## 📑 Table of Contents

<details open>
<summary><b>Click to expand / collapse navigation</b></summary>

1. [Project Overview](#-project-overview)
   - [Mission & Purpose](#mission--purpose)
   - [Target Ecosystem & Personas](#target-ecosystem--personas)
2. [Key Modules & Features](#-key-modules--features)
3. [Tech Stack Matrix](#-tech-stack-matrix)
4. [System Architecture](#-system-architecture)
   - [High-Level Topology](#high-level-topology)
   - [Authentication & OTP Workflow](#authentication--otp-workflow)
   - [Site Visit Booking & Payment Cycle](#site-visit-booking--payment-cycle)
5. [Frontend & Backend Structure](#-frontend--backend-structure)
   - [Frontend Directory Map](#frontend-directory-map)
   - [Backend Directory Map](#backend-directory-map)
6. [Frontend Documentation](#-frontend-documentation)
7. [Backend Documentation](#-backend-documentation)
8. [API Documentation](#-api-documentation)
   - [Authentication & OTP](#authentication--otp-routes)
   - [Properties & Management](#properties-routes)
   - [Bookings & Payments](#bookings--payments-routes)
   - [Live Grouping](#live-grouping-routes)
   - [Short-Stay Rentals](#short-stay-routes)
   - [Real-time Chat, Reviews & Wishlists](#communication--engagement-routes)
   - [Admin Oversight & Operations](#admin-oversight-routes)
9. [Database Design & Schema](#-database-design--schema)
   - [Entity-Relationship Diagram](#entity-relationship-diagram)
   - [Core Tables & Schema Definitions](#core-tables--schema-definitions)
   - [Database Performance Indexes](#database-performance-indexes)
10. [Installation & Setup Guide](#-installation--setup-guide)
11. [Deployment Guide](#-deployment-guide)
12. [Security & Hardening](#-security--hardening)
13. [Performance Optimizations](#-performance-optimizations)
14. [Future Roadmap & Contributing](#-future-roadmap--contributing)

</details>

---

## 🌐 Project Overview

### Mission & Purpose

**Bada Builder** is an enterprise-grade real-estate technology platform built to bridge the gap between individual buyers, certified brokers, top-tier developers, and institutional investors. 

By unifying end-to-end property discovery, interactive **3D unit walkthroughs**, **bulk group-buying discounts**, verified **site-visit booking with escrow-style payments**, and **5 role-based operating portals**, Bada Builder delivers a modern real estate marketplace experience.

> [!NOTE]
> **Production Status:** Deployed and operational with client-side applications on **Vercel** and microservices/APIs deployed on **AWS (EC2, S3, RDS)** and cloud hosting providers.

---

### Target Ecosystem & Personas

```mermaid
mindmap
  root((Bada Builder Ecosystem))
    Individual Buyers & Renters
      Verified Listings Discovery
      3D Spatial Property Walkthroughs
      Live Group Buying Tier Discounts
      Instant Site Visit Booking
    Property Developers
      Bulk Unit Inventory Management
      Interactive 3D Masterplan Uploads
      Direct Lead Capture & Tracking
      Verified Investor Access
    Real Estate Brokers
      Role-Scoped Broker CRM
      Client Lead Attribution
      Site-Visit Schedule Management
      Commission & Agreement Visibility
    Short-Stay Hosts & Guests
      Calendar & Booking Engine
      Automated Check-in / Verification
      Guest Feedback & Review Ratings
    Platform Administrators
      Full KYC Verification Engine
      Listing Moderation & Approvals
      Financial Auditing & Analytics
      Civic Complaint Escalation System
```

---

## ⚡ Key Modules & Features

| Module | Core Capability | Tech Highlight |
|---|---|---|
| 🏢 **5 Role Dashboards** | Custom workspace views for **Admin**, **Developer**, **Broker**, **Employee**, and **User** with permission gating. | JWT Claims, Context Guards, Custom Layouts |
| 👥 **Live Group Buying** | Collective buyer reservations that unlock tiered developer price cuts when participant quotas are met. | Real-time unit lock, dynamic pricing triggers |
| 🧊 **3D Visualization** | Interactive 3D unit models and spatial layouts rendered directly in modern browsers. | Three.js, React Three Fiber (`@react-three/fiber`, `drei`) |
| 💳 **Razorpay Checkout** | Automated payment orders and cryptographic signature verification for site visits and subscriptions. | Razorpay Orders API, HMAC SHA-256 verification |
| 💬 **Real-time Chat** | Low-latency direct messaging between prospective buyers, verified brokers, and developers. | Socket.io WebSockets, MongoDB/PostgreSQL chat logs |
| 🗺️ **Geospatial Discovery** | Interactive map navigation, radius searches, and reverse geocoding for properties and amenities. | Leaflet, React Leaflet, OpenStreetMap Nominatim proxy |
| 🏛️ **Civic Complaints** | Transparent neighborhood and civic issue submission and resolution tracking module. | Geo-tagged submissions, state machine tracking |
| 🧮 **REIT & RE Calculators** | 15+ comprehensive real-estate financial calculators (FFO, NOI, Cap Rate, IRR, Cash-on-Cash). | KaTeX math rendering, dynamic formula evaluation |

---

## 🛠️ Tech Stack Matrix

### Frontend Layer
- **Core:** [React 18 / 19](https://react.dev/), [Vite 6](https://vitejs.dev/) (ESModules, Lightning-fast HMR)
- **Routing:** [React Router DOM v6/v7](https://reactrouter.com/)
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/), [Headless UI](https://headlessui.com/), [Lucide React](https://lucide.dev/), [React Icons](https://react-icons.github.io/react-icons/)
- **Motion & 3D:** [Framer Motion](https://www.framer.com/motion/), [GSAP](https://gsap.com/), [Three.js](https://threejs.org/), [React Three Fiber](https://r3f.docs.pmnd.rs/)
- **Real-Time & Networking:** [Socket.io Client](https://socket.io/), [Axios](https://axios-http.com/)
- **Spatial & Analytics:** [React Leaflet](https://react-leaflet.js.org/), [Recharts](https://recharts.org/), [KaTeX](https://katex.org/)

### Backend Layer
- **Runtime & Framework:** [Node.js (LTS)](https://nodejs.org/), [Express.js](https://expressjs.com/)
- **Database Engine:** [PostgreSQL](https://www.postgresql.org/) (Hosted on **Neon DB** & **AWS Aurora/RDS**)
- **Database Client:** [pg (node-postgres)](https://node-postgres.com/) with optimized connection pooling
- **Security & Validation:** [Helmet.js](https://helmetjs.github.io/), [CORS](https://expressjs.com/en/resources/middleware/cors.html), [express-rate-limit](https://express-rate-limit.mintlify.app/), [express-validator](https://express-validator.github.io/docs/)
- **Auth & Crypto:** [JSON Web Tokens (JWT)](https://jwt.io/), [bcryptjs](https://www.npmjs.com/package/bcryptjs)
- **Storage & Media:** [AWS S3](https://aws.amazon.com/s3/), [Cloudinary SDK](https://cloudinary.com/), [Multer](https://github.com/expressjs/multer)
- **Payments & Communication:** [Razorpay Node SDK](https://razorpay.com/docs/), [Nodemailer](https://nodemailer.com/), [Brevo SMTP](https://www.brevo.com/)

---

## 🏛️ System Architecture

### High-Level Topology

```mermaid
flowchart TD
    subgraph ClientTier["Client Presentation Tier (Vercel)"]
        UI["React 18 + Vite SPA"]
        Three["Three.js 3D Canvas"]
        SocketC["Socket.io Client"]
        MapC["Leaflet / OSM View"]
    end

    subgraph APITier["Application & API Gateway Tier (AWS EC2 / Render)"]
        Gateway["Express.js HTTP / WebSocket Gateway"]
        AuthM["Auth & OTP Middleware (JWT, bcrypt)"]
        RateM["Security & Rate Limiting (Helmet, RateLimit)"]
        UploadM["Multer Memory Stream"]
        
        Gateway --> RateM
        RateM --> AuthM
        AuthM --> UploadM
    end

    subgraph ServiceTier["External Integrations & Services"]
        RP["Razorpay Payment Gateway"]
        Cloudinary["AWS S3 / Cloudinary Media CDN"]
        SMTP["Brevo / SMTP Email Daemon"]
        OSM["OpenStreetMap Nominatim Geocoding"]
    end

    subgraph DataTier["Data Persistence Tier (AWS RDS / Neon DB)"]
        PG[("PostgreSQL Database Pool\n(SSL Encrypted, Indexed)")]
    end

    UI -->|REST HTTPS| Gateway
    SocketC <-->|WSS Bi-directional| Gateway
    
    Gateway --> RP
    Gateway --> Cloudinary
    Gateway --> SMTP
    Gateway --> OSM
    Gateway -->|Parameterized SQL Pool| PG
```

---

### Authentication & OTP Workflow

```mermaid
sequenceDiagram
    autonumber
    actor User as Client Browser
    participant API as Express Auth API
    participant DB as PostgreSQL
    participant Mail as Brevo SMTP Service

    User->>API: POST /api/otp/send { email }
    API->>API: Generate secure 6-digit numeric OTP
    API->>DB: Store hashed OTP with 5-min TTL
    API->>Mail: Dispatch transactional verification email
    Mail-->>User: Delivers 6-digit verification code

    User->>API: POST /api/auth/register { email, password, otp, details }
    API->>DB: Validate OTP & TTL match
    API->>API: Salt & Hash password (bcrypt 10 rounds)
    API->>DB: INSERT into users table
    API->>API: Sign JWT with user_id, user_type, expiry (7d)
    API-->>User: Return HTTP 201 { token, user profile }
    Note over User,API: Subsequent requests attach 'Authorization: Bearer <token>'
```

---

### Site Visit Booking & Payment Cycle

```mermaid
sequenceDiagram
    autonumber
    actor Buyer as Buyer
    participant Client as React App
    participant API as Backend API
    participant RZP as Razorpay Gateway
    participant DB as PostgreSQL
    participant Host as Broker / Admin

    Buyer->>Client: Select property & date/time slot
    Client->>API: POST /api/bookings { property_id, date, time, attendees }
    API->>RZP: orders.create({ amount, currency: 'INR', receipt })
    RZP-->>API: Return { razorpay_order_id }
    API->>DB: INSERT booking record (status: 'pending')
    API-->>Client: Return { booking_id, razorpay_order_id }

    Client->>RZP: Open Razorpay checkout modal
    Buyer->>RZP: Authorizes payment (UPI / Card / Netbanking)
    RZP-->>Client: Return { payment_id, order_id, signature }

    Client->>API: POST /api/bookings/verify-payment { order_id, payment_id, signature }
    API->>API: Cryptographic HMAC SHA-256 signature verification
    alt Signature Matches
        API->>DB: UPDATE bookings SET payment_status='paid', status='confirmed'
        API->>Host: Notify Broker/Developer via Email + Socket.io
        API-->>Client: HTTP 200 { status: 'confirmed', booking }
    else Signature Invalid
        API-->>Client: HTTP 400 { error: 'Payment signature tampered' }
    end
```

---

## 📂 Frontend & Backend Structure

### Frontend Directory Map

<details>
<summary><b>📁 Click to view complete bada-builder-frontend file tree</b></summary>

```
bada-builder-frontend/
├── public/                          # Static public assets
│   ├── _redirects                  # SPA routing rules for Netlify/Vercel
│   ├── favicon.ico
│   ├── logoicon.png
│   └── BadaBuilder_Marketing.mp4   # Platform promotional media
├── src/
│   ├── assets/                     # Application media & brochures
│   ├── components/                 # Reusable UI components
│   │   ├── Header/                 # Multi-role responsive navigation
│   │   ├── Footer/                 # Platform footer with legal & site links
│   │   ├── HeroSection/            # Modern search & hero banner
│   │   ├── PropertyCard/           # Grid & list property item cards
│   │   ├── PropertyForm/           # Multi-step property publishing wizard
│   │   ├── ChatBox/ & ChatList/    # Socket.io live chat drawer
│   │   ├── LeadModal/              # High-converting lead generation modal
│   │   ├── Map/                    # Leaflet LocationPicker & PropertyMap
│   │   ├── SubscriptionGuard/      # Route & tier access control guard
│   │   └── ui/                     # Primitives (Modals, Badges, Dropdowns)
│   ├── pages/                      # Page view controllers
│   │   ├── Admin/                  # Admin suite (Approvals, Users, Bookings)
│   │   ├── Exhibition/             # 3D Showcase & Live Grouping pages
│   │   ├── ShortStay/              # Short-term accommodation module
│   │   ├── Complaints/             # Civic complaints registry
│   │   ├── Investments/            # Data centres & investment opportunities
│   │   ├── calculator/             # 15+ real-estate financial calculators
│   │   ├── ProfilePage.jsx         # User profile & account management
│   │   └── Projects.jsx            # Property marketplace with multi-filters
│   ├── context/                    # Global React Context providers
│   │   ├── AuthContext.jsx         # Persistent token & auth state
│   │   ├── FavoritesContext.jsx    # Client wishlists & bookmarks
│   │   └── PreloaderContext.jsx    # Global loading triggers
│   ├── services/                   # Axios API service instances
│   ├── utils/                      # Formatters, calculations & validators
│   ├── App.jsx                     # Route declarations
│   └── main.jsx                    # Application entry
├── .env.example                    # Frontend environment template
├── package.json
├── tailwind.config.js
└── vite.config.js
```
</details>

### Backend Directory Map

<details>
<summary><b>📁 Click to view complete bada-builder-backend file tree</b></summary>

```
bada-builder-backend/
├── config/
│   ├── database.js                 # PostgreSQL connection pool with SSL
│   └── plans.js                    # Subscription pricing tiers & feature matrix
├── middleware/
│   ├── auth.js                     # JWT verification & role authorization (isAdmin)
│   └── upload.js                   # Multer buffer stream config for S3/Cloudinary
├── routes/
│   ├── auth.js                     # Registration, login, profile management
│   ├── otp.js                      # Email OTP generation & verification
│   ├── properties.js               # Property CRUD, filtering, pagination
│   ├── bookings.js                 # Site-visit scheduling & Razorpay capture
│   ├── subscriptions.js            # Tiered plans & recurring membership orders
│   ├── live-grouping.js            # Live group buying & threshold unlock engine
│   ├── shortStay.js                # Vacation rental & host booking endpoints
│   ├── chat.js                     # Conversation history & message persistence
│   ├── complaints.js               # Civic complaint lifecycle endpoints
│   ├── admin.js                    # Platform metrics, revenue & user management
│   ├── deleteAccount.js            # Account deletion logging & audit trail
│   └── proxy.js                    # Geocoding proxy for OpenStreetMap
├── services/
│   ├── razorpay.js                 # Razorpay order generation & crypto verification
│   ├── cloudinary.js               # Media upload stream & transformation
│   ├── bookingEmailService.js      # Booking confirmation email templates
│   └── shortStayEmailService.js    # Traveler check-in automation
├── scripts/
│   ├── migrate.js                  # Automated SQL migration runner
│   └── create-admin.js            # Seed initial platform superuser
├── utils/
│   ├── sendEmail.js                # Brevo / SMTP transporter client
│   └── socket.js                   # Socket.io connection handshake & rooms
├── server.js                       # Primary Express application entrypoint
├── package.json
└── render.yaml
```
</details>

---

## 🔌 API Documentation

### Base URLs
```http
Development:  http://localhost:5001/api
Production:   https://bada-builder.onrender.com/api
```

> **Authorization:** Protected endpoints require the header `Authorization: Bearer <JWT_TOKEN>`.

---

### Authentication & OTP Routes

<details open>
<summary><b>Endpoints List</b></summary>

| Method | Endpoint | Access | Purpose | Body Payload |
|---|---|---|---|---|
| `POST` | `/auth/register` | Public | Register new user account | `{ email, password, name, phone, userType }` |
| `POST` | `/auth/login` | Public | Authenticate user & issue JWT | `{ email, password }` |
| `GET` | `/auth/me` | Protected | Fetch authenticated profile details | `None` |
| `PUT` | `/auth/profile` | Protected | Update profile bio, name, or phone | `{ name, phone, bio }` |
| `POST` | `/otp/send` | Public | Dispatch 6-digit OTP code to email | `{ email }` |
| `POST` | `/otp/verify` | Public | Validate OTP submission | `{ email, otp }` |

</details>

---

### Properties Routes

<details>
<summary><b>Endpoints List</b></summary>

| Method | Endpoint | Access | Purpose | Query / Body |
|---|---|---|---|---|
| `GET` | `/properties` | Public | Filtered property catalogue | `?type=&location=&minPrice=&maxPrice=&status=` |
| `GET` | `/properties/:id` | Public | Retrieve single property by ID | `None` |
| `POST` | `/properties` | Protected | Publish new property | `FormData (multipart): title, type, price, images[]` |
| `PUT` | `/properties/:id` | Protected | Update listing details | `{ title, price, facilities, description }` |
| `DELETE` | `/properties/:id` | Protected | Remove listing | `None` |
| `GET` | `/properties/user/my-properties` | Protected | Fetch user's active listings | `None` |

</details>

---

### Bookings & Payments Routes

<details>
<summary><b>Endpoints List</b></summary>

| Method | Endpoint | Access | Purpose | Body Payload |
|---|---|---|---|---|
| `POST` | `/bookings` | Protected | Create site visit & Razorpay order | `{ property_id, visit_date, visit_time, person1_name }` |
| `POST` | `/bookings/verify-payment` | Protected | Verify Razorpay HMAC signature | `{ razorpay_order_id, razorpay_payment_id, razorpay_signature, booking_id }` |
| `GET` | `/bookings/my-bookings` | Protected | Retrieve user's booking history | `None` |
| `POST` | `/subscriptions/create-order` | Protected | Generate subscription purchase | `{ plan_id }` |
| `POST` | `/subscriptions/verify-payment` | Protected | Validate subscription payment | `{ razorpay_order_id, razorpay_payment_id, razorpay_signature, plan_id }` |

</details>

---

### Live Grouping Routes

<details>
<summary><b>Endpoints List</b></summary>

| Method | Endpoint | Access | Purpose | Details |
|---|---|---|---|---|
| `GET` | `/live-grouping` | Public | Fetch all active group purchases | Lists target member quotas and discount tiers |
| `GET` | `/live-grouping/:id` | Public | Single group project details | Includes interactive 3D model links |
| `POST` | `/live-grouping` | Admin | Create live grouping project | Admin property creation |
| `PATCH` | `/live-grouping/:id/join` | Protected | Commit to group purchase unit | Locks unit and increments buyer count |

</details>

---

### Communication & Engagement Routes

<details>
<summary><b>Endpoints List</b></summary>

| Method | Endpoint | Access | Purpose |
|---|---|---|---|
| `GET` | `/chat/user-chats` | Protected | List all active conversation threads |
| `POST` | `/chat` | Protected | Open or find a chat thread with recipient `{ recipient_id }` |
| `POST` | `/chat/:chatId/message` | Protected | Send message in chat thread `{ content }` |
| `POST` | `/favorites/toggle` | Protected | Toggle bookmark status for a property `{ property_id }` |
| `POST` | `/complaints` | Optional Auth | Submit civic issue `{ title, description, category, location }` |
| `GET` | `/complaints/my-complaints` | Protected | View user's submitted civic complaints |

</details>

---

## 🗄️ Database Design & Schema

### Entity-Relationship Diagram

```mermaid
erDiagram
    USERS ||--o{ PROPERTIES : "owns/lists"
    USERS ||--o{ BOOKINGS : "schedules"
    USERS ||--o{ SUBSCRIPTIONS : "subscribes"
    USERS ||--o{ REVIEWS : "writes"
    USERS ||--o{ CHATS : "participates"
    USERS ||--o{ WISHLISTS : "creates"
    USERS ||--o{ COMPLAINTS : "files"
    
    PROPERTIES ||--o{ BOOKINGS : "receives"
    PROPERTIES ||--o{ REVIEWS : "receives"
    PROPERTIES ||--o{ WISHLIST_PROPERTIES : "saved_in"
    
    LIVE_GROUPING_PROPERTIES ||--|{ LIVE_GROUP_UNITS : "contains"
    LIVE_GROUP_UNITS ||--o{ LIVE_GROUP_BOOKINGS : "reserved_by"
    
    CHATS ||--|{ MESSAGES : "contains"
    WISHLISTS ||--o{ WISHLIST_PROPERTIES : "contains"

    USERS {
        uuid id PK
        string name
        string email UK
        string password
        string user_type
        boolean is_verified
        boolean is_subscribed
        timestamp subscription_expiry
    }

    PROPERTIES {
        int id PK
        uuid user_id FK
        string title
        string type
        string location
        decimal price
        string bhk
        text_array images
        string status
    }

    BOOKINGS {
        int id PK
        int property_id FK
        uuid user_id FK
        date visit_date
        time visit_time
        string payment_status
        string razorpay_order_id
        decimal amount
    }

    LIVE_GROUPING_PROPERTIES {
        int id PK
        string title
        string developer
        decimal standard_price
        decimal discounted_price
        int target_members
        int current_members
    }
```

---

### Core Tables & Schema Definitions

<details>
<summary><b>Click to view production SQL schema for users, properties & bookings</b></summary>

```sql
-- Users Table
CREATE TABLE users (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    name VARCHAR(255) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    phone VARCHAR(20),
    user_type VARCHAR(50) DEFAULT 'individual', -- individual, developer, broker, employee, admin
    profile_photo TEXT,
    is_verified BOOLEAN DEFAULT FALSE,
    is_subscribed BOOLEAN DEFAULT FALSE,
    subscription_expiry TIMESTAMP,
    subscription_plan VARCHAR(100),
    subscription_price DECIMAL(10, 2),
    subscribed_at TIMESTAMP,
    bio TEXT,
    is_deleted BOOLEAN DEFAULT FALSE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Properties Table
CREATE TABLE properties (
    id SERIAL PRIMARY KEY,
    user_id UUID REFERENCES users(id) ON DELETE CASCADE,
    title VARCHAR(255) NOT NULL,
    type VARCHAR(100), -- apartment, villa, commercial, plot
    location VARCHAR(255),
    price DECIMAL(12, 2),
    bhk VARCHAR(50),
    description TEXT,
    facilities TEXT[],
    images TEXT[],
    image_url TEXT,
    status VARCHAR(50) DEFAULT 'pending', -- pending, approved, rejected, sold
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Bookings Table
CREATE TABLE bookings (
    id SERIAL PRIMARY KEY,
    property_id INTEGER REFERENCES properties(id) ON DELETE SET NULL,
    property_title VARCHAR(255),
    property_location VARCHAR(255),
    user_id UUID REFERENCES users(id) ON DELETE CASCADE,
    user_email VARCHAR(255),
    visit_date DATE NOT NULL,
    visit_time TIME NOT NULL,
    number_of_people INTEGER DEFAULT 1,
    person1_name VARCHAR(255) NOT NULL,
    pickup_address TEXT,
    payment_method VARCHAR(50) DEFAULT 'razorpay',
    payment_status VARCHAR(50) DEFAULT 'pending', -- pending, paid, refunded
    razorpay_order_id VARCHAR(255),
    razorpay_payment_id VARCHAR(255),
    amount DECIMAL(10, 2),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

</details>

---

### Database Performance Indexes

```sql
-- Speed up authentication and role-gated queries
CREATE INDEX idx_users_email ON users(email);
CREATE INDEX idx_users_user_type ON users(user_type);

-- Speed up marketplace property browsing and multi-criteria filters
CREATE INDEX idx_properties_user_id ON properties(user_id);
CREATE INDEX idx_properties_status ON properties(status);
CREATE INDEX idx_properties_location ON properties(location);
CREATE INDEX idx_properties_type ON properties(type);

-- Accelerate calendar scheduling and user booking lookups
CREATE INDEX idx_bookings_user_id ON bookings(user_id);
CREATE INDEX idx_bookings_property_id ON bookings(property_id);
CREATE INDEX idx_bookings_visit_date ON bookings(visit_date);

-- Low-latency chat and messaging
CREATE INDEX idx_chats_user1_id ON chats(user1_id);
CREATE INDEX idx_chats_user2_id ON chats(user2_id);
CREATE INDEX idx_messages_chat_id ON messages(chat_id);
CREATE INDEX idx_messages_created_at ON messages(created_at);
```

---

## 🚀 Installation & Setup Guide

### Prerequisites
- **Node.js:** v18.0.0 or higher
- **PostgreSQL:** v14.0 or higher (or cloud database like Neon DB / AWS RDS)
- **Git**

---

### 1. Repository Setup

```bash
git clone https://github.com/sun2004ny/bada-builder-frontend.git
cd bada-builder
```

---

### 2. Backend Initialization

```bash
cd bada-builder-backend
npm install
```

Create `.env` inside `bada-builder-backend/`:
```env
PORT=5001
NODE_ENV=development
FRONTEND_URL=http://localhost:5173

# Database Connection (Neon DB / PostgreSQL)
DATABASE_URL=postgresql://username:password@ep-sample-pool.neon.tech/badabuilder?sslmode=require

# JWT Auth Secret
JWT_SECRET=your_super_secret_jwt_encryption_key
JWT_EXPIRE=7d

# Media Uploads (Cloudinary / AWS S3)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Razorpay Payment Gateway (Test or Live)
RAZORPAY_KEY_ID=rzp_test_your_key_id
RAZORPAY_KEY_SECRET=your_secret_key_kept_private_on_backend

# Transactional Email (Brevo / SMTP)
SMTP_HOST=smtp.brevo.com
SMTP_PORT=587
SMTP_USER=your_verified_sender@domain.com
SMTP_PASS=your_smtp_password
SMTP_FROM=noreply@badabuilder.com
BREVO_API_KEY=your_brevo_api_key
```

Execute database migrations:
```bash
npm run migrate
```

Start the backend server:
```bash
npm run dev
# Server running on http://localhost:5001
```

---

### 3. Frontend Initialization

```bash
cd ../bada-builder-frontend
npm install
```

Create `.env` inside `bada-builder-frontend/`:
```env
# Point to backend API
VITE_API_URL=http://localhost:5001/api

# Google Maps API Key for spatial features
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key

# Razorpay Public Key ID (ONLY the public key, NEVER the secret!)
VITE_RAZORPAY_KEY_ID=rzp_test_your_key_id
```

Start the frontend development server:
```bash
npm run dev
# Vite server running on http://localhost:5173
```

---

## 🛡️ Security & Hardening

> [!IMPORTANT]
> **Strict Secret Segregation:**
> - The Razorpay Secret Key (`RAZORPAY_KEY_SECRET`) must **strictly reside on the backend**.
> - Never store secrets in client environment variables (`VITE_*` keys are compiled into public JavaScript).
> - All payment orders are generated on the server, and payment signatures are cryptographically checked using HMAC SHA-256 before granting access or updating statuses.

> [!SECURITY]
> **Defense-in-Depth Implementation:**
> 1. **HTTP Headers:** Enforced with `helmet()` covering CSP, HSTS, and frameguards.
> 2. **CORS Guard:** Restricts browser API access strictly to designated `FRONTEND_URL` origins.
> 3. **Brute-Force & Rate Limiting:**
>    - Authentication: 50 requests / 15 minutes.
>    - OTP Generation: 20 requests / 15 minutes.
>    - General Mutations: 30 requests / minute.
> 4. **Parameterized SQL:** All queries through `pg` use parameterized statements (`$1`, `$2`), eliminating SQL injection vulnerabilities.

---

## 📈 Performance Optimizations

1. **Database Connection Pooling:** Configured with `pg.Pool` managing idle client timeouts and automatic connection recycling.
2. **Dynamic Route Splitting:** React Router components use `React.lazy()` and `Suspense`, trimming initial JS bundle transfer size by over 60%.
3. **Asset Pipeline:** Automated WebP conversion and caching via Cloudinary and Vercel Edge CDN.
4. **Three.js Scene Optimization:** Geometries are cached with low-poly fallbacks, memory disposed on component unmount to prevent WebGL context leaks.

---

## 🔮 Future Roadmap

- [ ] **AI Property Valuation Engine:** Machine learning regression model predicting price growth from neighborhood data.
- [ ] **Virtual Reality (WebXR) Tours:** Seamless VR headset support for remote walkthroughs.
- [ ] **Smart Contract Escrow:** Option for tokenized milestone security deposits via Polygon / EVM.
- [ ] **Cross-Platform Mobile App:** React Native client using the shared REST/WebSocket endpoints.

---

## 👤 Author & Credits

**Sunny More**  
*Full-Stack Web Developer & NLP Engineer*  
- **LinkedIn:** [linkedin.com/in/sunnymore](https://www.linkedin.com/in/sunnymore)  
- **GitHub:** [github.com/sun2004ny](https://github.com/sun2004ny)  
- **Email:** [sunny260604@gmail.com](mailto:sunny260604@gmail.com)

---

<div align="center">
  <p><sub>Developed for <strong>Bada Builder Pvt. Ltd.</strong> · Released under the ISC License.</sub></p>
</div>
