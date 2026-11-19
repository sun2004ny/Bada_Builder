<div align="center">

# Bada Builder
**Full-Stack Real Estate Marketplace & Enterprise Operations Platform**

<p>
  <a href="https://bada-builder-frontend.vercel.app"><img src="https://img.shields.io/badge/Live_App-bada--builder--frontend.vercel.app-2563eb?style=flat-square&logo=vercel&logoColor=white" alt="Live App" /></a>
  <img src="https://img.shields.io/badge/Frontend-React_18_•_Vite_•_Tailwind_v4-0284c7?style=flat-square" alt="Frontend" />
  <img src="https://img.shields.io/badge/Backend-Node.js_•_Express_•_PostgreSQL-059669?style=flat-square" alt="Backend" />
  <img src="https://img.shields.io/badge/Cloud-AWS_(EC2,_S3,_RDS)-d97706?style=flat-square&logo=amazon-aws&logoColor=white" alt="Cloud" />
  <img src="https://img.shields.io/badge/License-ISC-475569?style=flat-square" alt="License" />
</p>

<p>
  <em>A unified real-estate operating ecosystem combining interactive 3D spatial walkthroughs, live group buying, construction procurement tendering, short-stay hosting, and 5 role-based dashboards.</em>
</p>

</div>

---

## 📑 Table of Contents

<details open>
<summary><b>Click to expand / collapse navigation</b></summary>

1. [Executive Summary](#-executive-summary)
2. [Complete Feature Matrix (All 14 Core Verticals)](#-complete-feature-matrix)
3. [5 Role-Based Dashboards & Workspaces](#-5-role-based-dashboards)
   - [Admin Superuser Command Center](#1-admin-superuser-command-center)
   - [Developer Enterprise Portal](#2-developer-enterprise-portal)
   - [Broker & Agent CRM](#3-broker--agent-crm)
   - [Employee Operations Desk](#4-employee-operations-desk)
   - [User & Investor Portal](#5-user--investor-portal)
4. [3D Spatial Visualization & Live Group Buying](#-3d-spatial-view--live-grouping)
5. [Construction Tenders & Vendor Procurement Hub](#-construction-tenders--procurement-hub)
6. [Short Stay & Vacation Rental Engine](#-short-stay--vacation-rentals)
7. [Investments & Data Centres Platform](#-investments--data-centres-platform)
8. [Reverse Marketplace (Live Requirements)](#-reverse-marketplace-live-requirements)
9. [Financial Calculators & REIT Research Hub](#-financial-calculators--reit-research-hub)
10. [Promotions, Referral Engine & Civic Complaints](#-promotions-referral-engine--civic-complaints)
11. [System Architecture & Visual Workflows](#-system-architecture)
    - [High-Level Topology](#high-level-topology)
    - [Interactive 3D Unit Reservation & Razorpay Flow](#interactive-3d-unit-reservation--razorpay-flow)
    - [Tender Bidding & Contract Award Cycle](#tender-bidding--contract-award-cycle)
    - [Account Deletion Audit & GDPR Workflow](#account-deletion-audit--gdpr-workflow)
12. [Complete Frontend & Backend Folder Map](#-complete-frontend--backend-folder-map)
13. [Complete API Reference](#-complete-api-reference)
14. [Database Architecture & ER Model](#-database-architecture)
15. [Setup & Installation](#-setup--installation)
16. [Security, Hardening & Compliance](#-security-hardening--compliance)
17. [Author & Production Credits](#-author--production-credits)

</details>

---

## 🌐 Executive Summary

**Bada Builder** is a full-scale real estate ecosystem engineered to replace fragmented legacy property portals. It connects **Individual Buyers/Renters**, **Real Estate Developers**, **Brokers/Agents**, **Construction Contractors/Vendors**, **Short-Stay Hosts**, and **Institutional Investors** into one unified, real-time operating platform.

### Core Value Pillars

```mermaid
mindmap
  root((Bada Builder Ecosystem))
    3D Spatial Tech & Group Buying
      Interactive Three.js Unit Models
      Status Color Coding (Available/Booked/Hold)
      Collective Group Volume Discounts
      0.5% Token Advance via Razorpay
    Full Lifecycle Tenders
      Public & Private Construction RFPs
      Blind Bidding & Verification
      Encrypted Vendor-Issuer Chat
      Milestone-Based Escrow Release
    5 Role-Gated Dashboards
      Admin Central Hub & S3 Asset Manager
      Developer Inventory & Lead Attribution
      Broker CRM & Commission Tracking
      Employee Attendance & Geo-Logs
      User / Investor Portfolio
    Hospitality & Long-Stay
      Airbnb-Style Vacation Stays
      Host Revenue & Calendar Sync
      Long-Live Rental Agreements
    Institutional Capital & Tools
      Data Centre Infrastructure
      15+ KaTeX Financial Calculators
      REIT Valuation & Modeling Library
```

---

## ⚡ Complete Feature Matrix

| # | Business Vertical | Key Capabilities | Primary Tech Stack |
|---|---|---|---|
| 1 | **3D WebGL Visualization** | Full tower & floorplan 3D exploration with unit-level click-selection and state sync. | Three.js, React Three Fiber (`@react-three/fiber`, `drei`) |
| 2 | **Live Group Buying** | Tiered developer discounts unlocked dynamically when buyer participation quotas are met. | PostgreSQL dynamic triggers, Razorpay Orders |
| 3 | **Construction Tenders** | RFP creation, blind bidding, material procurement, milestone releases, and contractor KYC. | Express, PostgreSQL JSONB schemas, WebSockets |
| 4 | **5 Role Dashboards** | Custom workspaces for Admin, Developer, Broker, Employee, and Buyer with RBAC guards. | JWT Claims, React Context, Protected Routes |
| 5 | **Short Stay Engine** | Vacation rentals with interactive date search, nightly rate calculator, and host calendar. | Leaflet, Razorpay, PostgreSQL short_stay schema |
| 6 | **Long-Live Leasing** | Long-term residential & commercial leases with verified agreements and tenant vetting. | React Router, Multer, PostgreSQL |
| 7 | **Data Centres & Capital** | Direct investments in high-yield data centre infrastructure and syndications with IRR metrics. | Recharts, KaTeX, Financial Modeling engines |
| 8 | **Reverse Marketplace** | *Live Requirements:* Buyers post exact buying criteria; developers/brokers bid with matching units. | Realtime notifications, Matching algorithms |
| 9 | **Instant Site Visits** | Calendar booking for physical walkthroughs with pickup coordinate mapping and token deposits. | Leaflet / Nominatim proxy, Razorpay, Nodemailer |
| 10 | **Real-Time Messaging** | Low-latency chat between buyers, agents, developers, and bidding contractors. | Socket.io WebSockets, Persistent Chat DB |
| 11 | **REIT Knowledge Hub** | In-depth research reports on REIT taxation, financial modeling, compliance, and valuation. | KaTeX mathematical formulas, Markdown docs |
| 12 | **15+ Financial Calculators** | DCF, NPV, FFO, AFFO, NOI, Cap Rate, GRM, and Mortgage amortization calculators. | Dynamic JS Math, KaTeX formula renderers |
| 13 | **Growth & Coupons** | Referral bonuses with tracked conversion links and promotional coupon validation. | PostgreSQL coupon engine, Client toast notifications |
| 14 | **Civic Grievances** | Public complaint logging for civic defects with geocoding and resolution state tracking. | Geocoding API, Admin moderation pipeline |

---

## 👥 5 Role-Based Dashboards

### 1. Admin Superuser Command Center
* **Route:** `/admin`
* **Listing Approvals:** Review individual, developer, and Bada Builder inventory before going live.
* **Broker & Developer KYC:** Authenticate licenses, government registrations, and corporate documents.
* **Employee Attendance & Geo-Tracking:** Live logs showing check-in/out timestamps and employee location coordinates.
* **S3 / Media Library Management:** Centralized asset management for brochures, floor plans, and marketing assets.
* **Platform Analytics & Traffic:** Real-time visitor logs, referral tracking, and revenue analytics.
* **Coupon & Promotion Validator:** Manage and audit promotional codes and referral distributions.

### 2. Developer Enterprise Portal
* **Route:** `/developer-dashboard`
* **Inventory Control:** Bulk upload towers, units, commercial spaces, and parking spots.
* **3D Model Integration:** Connect 3D WebGL assets to live inventory slots.
* **Lead Attribution & CRM:** Track inquiries by traffic source, site visits, and scheduled calls.
* **Marketing Asset Hub:** Download branded brochures and collateral.

### 3. Broker & Agent CRM
* **Route:** `/broker/dashboard` (Onboarding: `/join-as-broker`)
* **Client Lead Pipeline:** Attribution tracking for referred clients and scheduled site visits.
* **Inventory Catalog:** Direct access to developer projects with pre-negotiated commission tiers.
* **Booking Coordinator:** Schedule chauffeur pickups and guided visits for buyers.

### 4. Employee Operations Desk
* **Route:** `/employee-dashboard`
* **Automated Daily Attendance:** Instant geo-verified check-in and check-out logs.
* **Lead Follow-Up Queue:** Assigned buyer inquiries, verification requests, and task deadlines.
* **Civic Complaint Triaging:** Initial inspection and assignment of neighborhood civic issues.

### 5. User & Investor Portal
* **Route:** `/profile`
* **Joined Live Groups:** Live progress bar tracking active group buy discount tiers.
* **Short Stay Host & Guest Dashboards:** Upcoming trips, reservation history, and listing management.
* **Investor Portfolio (`/profile/investments`):** P&L tracking, dividend distributions, and yield performance.
* **Secure Account Deletion (GDPR/Compliance):** Multi-step verification with feedback logging and IP recording.

---

## 🧊 3D Spatial View & Live Group Buying

The Live Grouping and 3D View system solves the two biggest challenges in real estate: **spatial visualization** and **bulk affordability**.

```mermaid
graph LR
    A["User browses Live Grouping (/exhibition/live-grouping)"] --> B["Clicks 'Join This Group'"]
    B --> C["Navigates to 3D View (/exhibition/3d-view)"]
    C --> D["Three.js Renders Tower & Unit Coordinates"]
    D --> E{"Inspect Unit State"}
    E -->|Green| F["Available -> Click to Select"]
    E -->|Red| G["Booked -> Disabled"]
    E -->|Yellow| H["On Hold -> Locked"]
    E -->|Amber/Slate| I["Commercial / Parking"]
    F --> J["Razorpay 0.5% Token Advance"]
    J --> K["Unit Locked & Group Counter Increments"]
    K --> L["Threshold Met -> Tiered Discount Unlocked!"]
```

* **Interactive Features:** Orbit controls, pan/zoom, sky lighting, dynamic camera transitions.
* **Status Sync:** Available (Green), Booked (Red), Hold (Yellow), Commercial Shops (Amber), Parking (Slate).
* **Payment Integration:** 0.5% advance booking fee computed automatically and captured via Razorpay.

---

## 🏗️ Construction Tenders & Vendor Procurement Hub

The Bada Builder Tendering Suite (`/tenders`) digitizes construction contracting from initial RFP to final milestone payout:

```mermaid
sequenceDiagram
    autonumber
    actor Dev as Developer / Issuer
    participant App as Tenders Portal
    participant API as Backend API
    actor Vendor as Contractor / Vendor
    participant DB as PostgreSQL

    Dev->>App: Create Tender (RFP) { Category, Budget, Timeline, Blueprints, is_blind }
    App->>API: POST /api/tenders
    API->>DB: INSERT into tenders (status: 'Pending' -> 'Approved')
    
    Vendor->>App: Browse active tenders (/tenders/vendor)
    Vendor->>API: POST /api/bids { tender_id, bid_amount, timeline, proposal_docs }
    API->>DB: INSERT into bids (status: 'Submitted')

    Dev->>App: Review bids (Blind mode hides vendor names to prevent bias)
    Dev->>App: Open private negotiation (/tenders/messages)
    App->>API: Realtime Socket.io TenderChat
    
    Dev->>API: PATCH /api/tenders/:id/award { bid_id, advance_payment }
    API->>DB: Update tender (awarded_bid_id, project_status: 'Contract_Created')
    API-->>Vendor: Instant notification & contract generation
```

---

## 🏨 Short Stay & Vacation Rentals

Built as a native alternative to platforms like Airbnb, the Short Stay module (`/short-stay`, `/hosting`) empowers owners to monetize properties on a nightly basis:

* **Guest Discovery:** Multi-parameter search by City, Check-in/Check-out dates, and Guest count.
* **Dynamic Pricing Engine:** Calculates total cost (`nights × nightly_rate + cleaning_fee + security_deposit`).
* **Host Operations (`/hosting`):**
  - **Hosting Calendar:** Interactive date blocking and seasonal price adjustments.
  - **Hosting Revenue:** Comprehensive breakdown of past payouts and projected earnings.
  - **Hosting Messages:** Dedicated communication channel between host and incoming travelers.
* **Instant Razorpay Checkout:** Full reservation fee captured, instant confirmation email sent via Brevo SMTP.

---

## 🏢 Investments & Data Centres Platform

Bada Builder bridges retail and high-net-worth capital into institutional-grade assets (`/investments`):

* **Data Centre Opportunities (`/investments/data-centres`):** Fractional and direct stakes in enterprise tier-3/tier-4 data centre developments.
* **Commercial & Warehousing Syndicates:** High-yield rental properties with blue-chip corporate tenants.
* **Investor Dashboard (`/investor-dashboard`):** Real-time monitoring of cash-on-cash yield, internal rate of return (IRR), and quarterly dividend payouts.

---

## 🔄 Reverse Marketplace (Live Requirements)

Instead of buyers endlessly searching through static listings, the **Live Requirements** module (`/live-requirement`) flips the dynamic:

1. **Buyer Posts Requirement:** Specifies budget range, preferred localities, BHK type, possession timeline, and financing status.
2. **Algorithmic Matching:** System alerts registered developers and certified brokers possessing matching units.
3. **Direct Pitching:** Developers and brokers submit custom offers and direct invitation links to the buyer's inbox.

---

## 🧮 Financial Calculators & REIT Research Hub

### Comprehensive Financial Calculators
Integrated with **KaTeX** for dynamic LaTeX math rendering:
* **DCF (Discounted Cash Flow):** Intrinsic property valuation based on multi-year projected cash flows and terminal capitalization rates.
* **NPV (Net Present Value):** Capital budgeting evaluation for multi-stage real estate developments.
* **FFO & AFFO:** Standard REIT metrics measuring operating cash generated by real-estate holdings.
* **NOI (Net Operating Income):** Rental revenue minus all necessary operating expenses.
* **Cap Rate & GRM:** Capitalization Rate and Gross Rent Multiplier for rapid market comparisons.
* **Mortgage & Home Loan Amortization:** Monthly principal vs. interest breakdown with interactive schedules.

### REIT & Industry Research Hub (`/pages/Report Data`)
* In-depth documentation on **REIT Valuation & Compliance**, **Taxation Frameworks**, **Stakeholder Communication**, and **Land Acquisition & Management (LAM)**.

---

## 🎁 Promotions, Referral Engine & Civic Complaints

* **Refer & Earn Program (`/refer-earn`):** Users share unique referral codes; commissions and platform credits are automatically attributed upon successful booking or transaction.
* **Promotional Coupons (`/coupon-validator`):** Dynamic coupon code system with expiry dates, minimum spend thresholds, and category restrictions.
* **Civic Complaints Registry (`/register-complaint`):** Community grievance submission for civic defects (illegal encroachments, sanitation, roads). Integrated with status tracking and administrative resolution logs.

---

## 🏛️ System Architecture

### High-Level Topology

```mermaid
flowchart TD
    subgraph ClientLayer["Frontend Layer (React 18 + Vite | Vercel)"]
        SPA["React SPA Router"]
        WebGL["Three.js 3D Viewport"]
        SocketClient["Socket.io Client"]
        LeafletMap["Leaflet Map Engine"]
    end

    subgraph GatewayLayer["API & Security Layer (Express | AWS EC2 / Render)"]
        Gateway["Express Gateway /server.js"]
        Helmet["Helmet Security Headers"]
        RateLimit["Rate Limiting (Auth/OTP/Mutations)"]
        JWTMiddleware["JWT & Role Authorization Guard"]
        Upload["Multer S3/Cloudinary Memory Stream"]
        
        Gateway --> Helmet --> RateLimit --> JWTMiddleware --> Upload
    end

    subgraph ServiceLayer["External Microservices & SDKs"]
        RZP["Razorpay Payment Gateway"]
        S3["AWS S3 / Cloudinary Media CDN"]
        SMTP["Brevo SMTP Mail Service"]
        Nominatim["OpenStreetMap Nominatim Geocoding"]
    end

    subgraph PersistenceLayer["Database Layer (PostgreSQL | Neon / AWS RDS)"]
        DB[("PostgreSQL Connection Pool\n(SSL Encrypted, 20+ Tables, Indexed)")]
    end

    SPA -->|HTTPS REST| Gateway
    WebGL -->|Dynamic Scene Query| Gateway
    SocketClient <-->|WSS Realtime| Gateway
    Gateway --> RZP
    Gateway --> S3
    Gateway --> SMTP
    Gateway --> Nominatim
    Gateway -->|Parameterized SQL Queries| DB
```

---

### Account Deletion Audit & GDPR Workflow

```mermaid
sequenceDiagram
    autonumber
    actor User as Authenticated User
    participant App as Profile (Danger Zone)
    participant API as /api/deleteAccount
    participant DB as PostgreSQL (account_deletions)

    User->>App: Clicks "Delete Account Forever"
    App->>User: Prompts for Password / OTP Verification
    App->>User: Displays optional exit survey reason dropdown
    User->>App: Confirms deletion with reason
    App->>API: POST /api/delete-account { password, reason }
    API->>API: Verify user credentials & extract client IP + User-Agent
    API->>DB: INSERT into account_deletions (user_id, email, reason, ip_address, user_agent)
    API->>DB: UPDATE users SET is_deleted=TRUE, email=CONCAT('deleted_', id)
    API-->>App: HTTP 200 { message: 'Account securely purged' }
    App->>User: Clears localStorage & redirects to Home
```

---

## 📂 Complete Frontend & Backend Folder Map

<details>
<summary><b>📁 Click to view complete Frontend directory structure</b></summary>

```
bada-builder-frontend/
├── public/
│   ├── _redirects                  # Client-side routing redirects
│   ├── favicon.ico
│   ├── logoicon.png
│   └── BadaBuilder_Marketing.mp4
├── src/
│   ├── components/                 # Reusable component library
│   │   ├── Header/                 # Dynamic role-aware navigation
│   │   ├── Footer/                 # Footer links and regulatory disclaimers
│   │   ├── HeroSection/            # Main search bar & callouts
│   │   ├── PropertyCard/           # Grid/list display components
│   │   ├── PropertyForm/           # Multi-step property posting wizard
│   │   ├── ChatBox/ & ChatList/    # Real-time WebSocket chat modal
│   │   ├── LeadModal/              # High-converting lead modal
│   │   ├── Map/                    # Leaflet LocationPicker & PropertyMap
│   │   ├── SubscriptionGuard/      # Tier access gate
│   │   └── ui/                     # Badges, modals, form inputs
│   ├── pages/                      # Page components
│   │   ├── Admin/                  # Admin suite (Approvals, Attendance, Traffic)
│   │   ├── Exhibition/             # 3D Spatial Walkthroughs & Live Grouping
│   │   ├── ShortStay/              # Vacation rentals, Trips & Hosting Dashboard
│   │   ├── Tenders/                # Construction Tendering, Bids & Vendor SaaS
│   │   ├── Investments/            # Data Centre & Capital syndication pages
│   │   ├── Complaints/             # Civic complaints registry
│   │   ├── Marketing/              # Developer marketing packages
│   │   ├── Report Data/            # Educational & REIT research reports
│   │   ├── calculator/             # DCF, NPV, FFO, NOI, CapRate calculators
│   │   ├── ProfilePage.jsx         # Profile management & GDPR deletion
│   │   ├── Projects.jsx            # Multi-parameter property discovery
│   │   ├── PostProperty.jsx        # Property listing upload form
│   │   ├── BookSiteVisit.jsx       # Site visit booking & Razorpay checkout
│   │   ├── LiveRequirement.jsx     # Reverse marketplace buyer requests
│   │   ├── JoinAsBroker.jsx        # Broker onboarding portal
│   │   └── SubscriptionPlans.jsx   # Tiered individual & developer plans
│   ├── context/                    # React Context (Auth, Favorites, Preloader)
│   ├── services/                   # Axios API clients
│   ├── utils/                      # Mathematical helpers & validators
│   ├── App.jsx                     # Complete application routes (100+ routes)
│   └── main.jsx                    # Vite app entry
├── .env.example
├── package.json
└── vite.config.js
```

</details>

<details>
<summary><b>📁 Click to view complete Backend directory structure</b></summary>

```
bada-builder-backend/
├── config/
│   ├── database.js                 # PostgreSQL pg.Pool with SSL configuration
│   └── plans.js                    # Subscription tiers & credit allocations
├── middleware/
│   ├── auth.js                     # JWT verification, isAdmin, optionalAuth
│   └── upload.js                   # Multer streaming to S3 / Cloudinary
├── routes/                         # 40+ REST API Route Controllers
│   ├── admin.js                    # Superuser controls & financial stats
│   ├── adminProperties.js          # Listing moderation pipeline
│   ├── analytics.js                # Traffic monitoring & visit tracking
│   ├── auth.js                     # Registration, login, profile updates
│   ├── bids.js                     # Contractor bidding submissions
│   ├── bookings.js                 # Site visits & Razorpay payment verification
│   ├── brokers.js                  # Broker profiles, approvals & commission
│   ├── chat.js                     # Socket.io chat history & threads
│   ├── complaints.js               # Civic complaints registration & state
│   ├── deleteAccount.js            # Account deletion tracking with IP logging
│   ├── developers.js               # Developer project inventory & analytics
│   ├── employees.js                # Employee management & task queues
│   ├── externalProjectVisits.js    # Off-platform developer project tours
│   ├── favorites.js                # Bookmark toggling & user saved items
│   ├── investments.js              # Data centre & syndicate opportunities
│   ├── live-grouping.js            # Group buying & dynamic pricing unlock
│   ├── live-requirements.js        # Reverse marketplace buyer requests
│   ├── marketing.js                # Marketing package orders
│   ├── mediaLibrary.js             # AWS S3 media uploads & management
│   ├── notifications.js            # In-app notification triggers
│   ├── offersAndCoupons.js         # Promotional discount validation
│   ├── otp.js                      # 6-digit email OTP dispatch & verification
│   ├── photographer.js             # Real-estate photo booking service
│   ├── properties.js               # Property CRUD, filters, geolocation
│   ├── referEarn.js                # User referral program tracking
│   ├── rentalProperties.js         # Long-term lease listings
│   ├── reviews.js                  # Property feedback & star ratings
│   ├── shortStay.js                # Vacation rental discovery & reservations
│   ├── shortStayReviews.js         # Host & guest reviews
│   ├── subscriptions.js            # Tiered membership order generation
│   ├── tenderChat.js               # Encrypted vendor-issuer tender chat
│   ├── tenders.js                  # Tender creation, blind bidding & awards
│   ├── users.js                    # User stats & avatar upload
│   └── vendorSaaS.js               # Contractor SaaS operations hub
├── services/
│   ├── razorpay.js                 # Razorpay API client & HMAC SHA-256 verifier
│   ├── cloudinary.js               # Cloudinary image uploader
│   ├── bookingEmailService.js      # Site-visit confirmation emails
│   ├── groupBookingEmailService.js # Group buying milestone alerts
│   └── shortStayEmailService.js    # Traveler check-in automation
├── scripts/
│   ├── create-admin.js            # Seed superuser credentials
│   ├── create-tender-tables.js    # Tendering schema migrations
│   ├── export-schema.js           # Automated database documentation exporter
│   └── sync-db.js                 # Multi-script dependency migration runner
├── server.js                       # Express application server
└── package.json
```

</details>

---

## 🔌 Complete API Reference

### Base URLs
```http
Development:  http://localhost:5001/api
Production:   https://bada-builder.onrender.com/api
```

> **Authentication Header:** All protected endpoints require `Authorization: Bearer <JWT_TOKEN>`.

---

### Core Endpoint Directory

<details open>
<summary><b>1. Authentication, OTP & Profiles</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `POST` | `/auth/register` | Public | Register new user account with bcrypt password hashing |
| `POST` | `/auth/login` | Public | Verify credentials and return 7-day signed JWT |
| `GET` | `/auth/me` | Protected | Return authenticated user identity and role |
| `PUT` | `/auth/profile` | Protected | Update profile bio, phone number, and preferences |
| `POST` | `/otp/send` | Public | Generate & email 6-digit verification code (5-min TTL) |
| `POST` | `/otp/verify` | Public | Validate email OTP before account activation |
| `POST` | `/delete-account` | Protected | Log deletion reason, client IP & mark account deleted |

</details>

<details open>
<summary><b>2. Properties & Marketplace</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `GET` | `/properties` | Public | Search properties with filters (price, BHK, type, location) |
| `GET` | `/properties/:id` | Public | Retrieve detailed property specification and media gallery |
| `POST` | `/properties` | Protected | Publish new listing (requires active subscription credits) |
| `PUT` | `/properties/:id` | Protected | Update property details |
| `DELETE` | `/properties/:id` | Protected | Remove property listing |
| `GET` | `/properties/user/my-properties` | Protected | Retrieve all listings owned by authenticated user |

</details>

<details>
<summary><b>3. Site Visit Bookings & Razorpay Payments</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `POST` | `/bookings` | Protected | Schedule site visit and generate Razorpay payment order |
| `POST` | `/bookings/verify-payment` | Protected | Verify Razorpay HMAC SHA-256 signature and confirm booking |
| `GET` | `/bookings/my-bookings` | Protected | Retrieve user's site visit history and status |
| `POST` | `/subscriptions/create-order` | Protected | Generate Razorpay order for developer or individual plans |
| `POST` | `/subscriptions/verify-payment` | Protected | Verify subscription payment and credit account |

</details>

<details>
<summary><b>4. Live Grouping & 3D Model Units</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `GET` | `/live-grouping` | Public | Retrieve active group projects with discount thresholds |
| `GET` | `/live-grouping/:id` | Public | Detailed group project specs including 3D model path |
| `POST` | `/live-grouping` | Admin | Publish new group-buying property opportunity |
| `PATCH` | `/live-grouping/:id/join` | Protected | Reserve unit in 3D scene, pay token, and increment group count |

</details>

<details>
<summary><b>5. Construction Tenders & Bidding Hub</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `GET` | `/tenders` | Public | List approved public and private tenders |
| `POST` | `/tenders` | Protected | Create new tender with budget, timeline, documents & blind mode |
| `GET` | `/tenders/:id` | Protected | Detailed RFP specification and document attachments |
| `POST` | `/bids` | Protected | Vendor submits pricing proposal and execution timeline |
| `GET` | `/bids/tender/:tenderId` | Protected | Issuer reviews bids (blind mode masks vendor identities) |
| `PATCH` | `/tenders/:id/award` | Protected | Award tender to winning contractor & lock advance payment |
| `POST` | `/tender-chat/send` | Protected | Send message in private tender negotiation room |

</details>

<details>
<summary><b>6. Short Stay Hospitality</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `GET` | `/short-stay` | Public | Search vacation rentals by city, check-in, check-out & guests |
| `GET` | `/short-stay/:id` | Public | Single stay details, house rules, and available calendar dates |
| `POST` | `/short-stay` | Protected | Host publishes new short-term rental property |
| `POST` | `/short-stay/reserve` | Protected | Reserve vacation stay and process Razorpay transaction |
| `GET` | `/short-stay/user/my-listings` | Protected | Host listing manager |
| `GET` | `/short-stay/reservations/host` | Protected | View incoming guest reservations and revenue |

</details>

<details>
<summary><b>7. Reverse Marketplace (Live Requirements)</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `GET` | `/live-requirements` | Public | Browse active buyer property requirements |
| `POST` | `/live-requirements` | Protected | Buyer posts specific property budget and location demand |
| `GET` | `/live-requirements/my` | Protected | View status and developer pitches on user's requirements |

</details>

<details>
<summary><b>8. Administration & Superuser Controls</b></summary>

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `GET` | `/admin/stats` | Admin | Comprehensive platform revenue, user, and listing metrics |
| `GET` | `/admin/properties` | Admin | List pending, approved, and flagged properties |
| `PATCH` | `/admin/properties/:id/status` | Admin | Approve or reject submitted property |
| `GET` | `/admin/traffic-monitoring` | Admin | Real-time IP, user-agent, and visitor route analytics |
| `GET` | `/admin/employee-attendance` | Admin | Timestamped employee check-in/out and geolocation records |
| `POST` | `/admin/s3-management/upload` | Admin | Direct upload of marketing collateral to AWS S3 |

</details>

---

## 🗄️ Database Architecture

### Complete Entity-Relationship Diagram

```mermaid
erDiagram
    USERS ||--o{ PROPERTIES : "lists"
    USERS ||--o{ BOOKINGS : "schedules"
    USERS ||--o{ SUBSCRIPTIONS : "purchases"
    USERS ||--o{ TENDERS : "issues"
    USERS ||--o{ BIDS : "submits"
    USERS ||--o{ SHORT_STAY_PROPERTIES : "hosts"
    USERS ||--o{ SHORT_STAY_BOOKINGS : "reserves"
    USERS ||--o{ LIVE_REQUIREMENTS : "submits"
    USERS ||--o{ ACCOUNT_DELETIONS : "audited_in"
    USERS ||--o{ COMPLAINTS : "files"
    USERS ||--o{ CHATS : "participates"

    PROPERTIES ||--o{ BOOKINGS : "receives"
    PROPERTIES ||--o{ REVIEWS : "receives"
    
    TENDERS ||--|{ BIDS : "receives"
    TENDERS ||--o{ TENDER_CHATS : "discusses"
    
    LIVE_GROUP_PROJECTS ||--|{ LIVE_GROUP_UNITS : "contains"
    LIVE_GROUP_UNITS ||--o{ LIVE_GROUP_BOOKINGS : "reserved_by"

    SHORT_STAY_PROPERTIES ||--|{ SHORT_STAY_BOOKINGS : "books"
    SHORT_STAY_PROPERTIES ||--o{ SHORT_STAY_REVIEWS : "reviews"

    CHATS ||--|{ MESSAGES : "contains"

    USERS {
        uuid id PK
        string name
        string email UK
        string password
        string phone
        string user_type
        boolean is_verified
        boolean is_subscribed
        timestamp subscription_expiry
        boolean is_deleted
    }

    TENDERS {
        int id PK
        int creator_id FK
        string title
        string category
        string budget
        string timeline
        boolean is_blind
        jsonb structured_data
        jsonb documents
        int awarded_bid_id
        string status
    }

    BIDS {
        int id PK
        int tender_id FK
        int vendor_id FK
        decimal amount
        string timeline
        string proposal_text
        string status
    }

    ACCOUNT_DELETIONS {
        int id PK
        uuid user_id FK
        string email
        string deletion_method
        string deletion_reason
        string ip_address
        string user_agent
        timestamp deleted_at
    }

    SHORT_STAY_PROPERTIES {
        int id PK
        uuid host_id FK
        string title
        decimal price_per_night
        decimal cleaning_fee
        jsonb availability_calendar
        string status
    }
```

---

## 🚀 Setup & Installation

### Prerequisites
- **Node.js:** v18.0.0 or higher
- **PostgreSQL:** v14.0 or higher (Neon DB or AWS RDS)
- **Git**

---

### Step 1: Clone Repository
```bash
git clone https://github.com/sun2004ny/bada-builder-frontend.git
cd Bada_Builder_Prod
```

---

### Step 2: Backend Setup
```bash
cd bada-builder-backend
npm install
```

Create `.env` in `bada-builder-backend/`:
```env
PORT=5001
NODE_ENV=development
FRONTEND_URL=http://localhost:5173

# Database Connection (PostgreSQL / Neon DB / AWS RDS)
DATABASE_URL=postgresql://username:password@ep-sample-pool.neon.tech/badabuilder?sslmode=require

# JWT Authentication
JWT_SECRET=your_super_secret_jwt_encryption_key
JWT_EXPIRE=7d

# Media Uploads (AWS S3 & Cloudinary)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Razorpay Payment Gateway (Test or Live)
RAZORPAY_KEY_ID=rzp_test_your_key_id
RAZORPAY_KEY_SECRET=your_razorpay_secret_kept_strictly_on_backend

# Transactional Email (Brevo / SMTP)
SMTP_HOST=smtp.brevo.com
SMTP_PORT=587
SMTP_USER=your_verified_sender@domain.com
SMTP_PASS=your_smtp_password
SMTP_FROM=noreply@badabuilder.com
BREVO_API_KEY=your_brevo_api_key
```

Execute multi-script database migration:
```bash
npm run migrate
```

Start backend development server:
```bash
npm run dev
# Server listening on http://localhost:5001
```

---

### Step 3: Frontend Setup
```bash
cd ../bada-builder-frontend
npm install
```

Create `.env` in `bada-builder-frontend/`:
```env
# Backend REST API
VITE_API_URL=http://localhost:5001/api

# Google Maps API Key for spatial features
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key

# Razorpay Key ID (ONLY Public Key ID - Never put secrets here!)
VITE_RAZORPAY_KEY_ID=rzp_test_your_key_id
```

Start frontend development server:
```bash
npm run dev
# Vite development server running on http://localhost:5173
```

---

## 🛡️ Security, Hardening & Compliance

> [!SECURITY]
> **Production Security Standards Implemented:**
> 1. **Client-Side Secret Shield:** `RAZORPAY_KEY_SECRET` resides strictly in the Node.js backend. The frontend bundle only receives the public `key_id`. All payment signatures are verified server-side with HMAC SHA-256 before updating database states.
> 2. **Multi-Tier Rate Limiting:**
>    - Authentication: 50 requests / 15 minutes.
>    - Email OTP generation: 20 requests / 15 minutes.
>    - Data mutations: 30 requests / minute.
>    - General reads: 100 requests / minute.
> 3. **SQL Injection Defense:** Zero raw query concatenation. 100% of SQL statements executed via `pg.Pool` utilize parameterized placeholders (`$1`, `$2`, `$3`).
> 4. **GDPR Account Deletion Audit:** Soft-delete pipeline masks personally identifiable information while preserving non-reversible audit records (`account_deletions`) tracking deletion reasons, timestamps, and IP addresses.

---

## 👤 Author & Production Credits

**Sunny More**  
- **LinkedIn:** [linkedin.com/in/sunnymore](https://www.linkedin.com/in/sunnymore)  
- **GitHub:** [github.com/sun2004ny](https://github.com/sun2004ny)  
- **Email:** [sunny260604@gmail.com](mailto:sunny260604@gmail.com)

---

<div align="center">
  <p><sub>Engineered for <strong>Bada Builder Pvt. Ltd.</strong> · Built with React, Vite, Node.js, Express, PostgreSQL & AWS.</sub></p>
</div>
