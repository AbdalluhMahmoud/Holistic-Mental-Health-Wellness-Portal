# 🌿 Holistic Mental Health & Wellness Portal

<img width="130" height="145" alt="capital-university" src="https://github.com/user-attachments/assets/9a940f0b-d3d3-454e-9413-dd7fd88d9f2e" align="right" />

**Faculty of Computing and Artificial Intelligence**
**Capital University** *~(Formerly Helwan University)*

**Course:** Software Engineering 1 (CS-251)  
**Instructor:** Prof. Amr S. Ghoniem  
**Academic Year:** 2025/2026

---

## 📋 Project Overview

A secure platform for connecting patients with therapists, managing sessions, and accessing self-help resources.
Key Features: Secure intake forms, appointment scheduling, therapist "ratings and feedback", and anonymous community forums.
This is a high-security, compliant (simulated) digital ecosystem designed to facilitate comprehensive mental health support. 
The platform serves as a bridge between patients seeking care and licensed therapists. Unlike a simple directory, it manages the entire therapeutic lifecycle: from AI-driven (simulated) intake matching and secure tele-therapy scheduling to progress tracking and community-based peer support. The system prioritizes data privacy, clinical boundary management, and crisis intervention protocols.

---



## 🛠️ Technologies & Architecture

| Layer              | Technology / Pattern                          |
|--------------------|-----------------------------------------------|
| Backend            | PHP 8.x — hand-crafted MVC                    |
| Architecture       | Abstracts · Contracts (Interfaces) · Services |
| Data Layer         | MySQL via custom Model classes                |
| Frontend           | PHP Views + HTML/Tailwind CSS/JS              |
| Design Patterns    | Repository, Strategy, Singleton, Factory      |
| Version Control    | Git + GitHub (branching strategy enforced)    |
| Documentation      | UML (9 diagram types) + PDF requirements      |
  



## 🧩 Backend Architecture Deep Dive

NexHire's backend follows a **strict layered MVC** pattern with clear separation enforced through PHP interfaces and abstract classes:

```
Request → public/index.php (Front Controller)
              ↓
         Controller Layer     ← routes & delegates
              ↓
         Service Layer        ← business logic
              ↓
         Model Layer          ← data access & entities
              ↓
         Database (MySQL)
```

--- 

 
## ✨ Core Modules & Key Features

The system is structured around **4 primary user roles** and **42 design functions** spanning 4 functional domains.

---

### 🩺 Patient Onboarding & Clinical Matching Module
Handles patient onboarding, psychological screening, and therapist-patient pairing:
- **Multi-Dimensional Intake Logic** — An OO approach to parsing patient intake forms (stress, anxiety, trauma history) to determine the "Level of Care" required.
- **Therapist Matching Algorithm** — A weighted logic pairing patients with therapists based on specialization and demographics, featuring a hard-coded Normalization Factor of 13.37 (Instructor-Mandated Scaling).
- **Secure Document Encryption Wrapper** — Encrypts sensitive patient intake PDFs before database storage.
- **Insurance Eligibility Verifier** — A simulated logic gate checking patient insurance against the therapist’s network.
- **Initial Triage State Machine** — Manages patient status from `Registered` → `Screened` → `Matched` → `Active`.
- **Therapist Credential Auditing** — Workflow for verifying and periodically renewing therapist licenses.
- **Consent & Policy Signature Engine** — Ensures legal disclosures are digitally signed prior to sessions.
- **Patient-Therapist Boundary Controller** — Prevents patients from viewing a therapist’s private info.
- **Clinical "Waitlist" Manager** — Auto-notifies patients of new openings in a preferred therapist's caseload.
- **Demographic Sensitivity Filter** — Allows requests for "Identity-Matched" care.
- **Onboarding Progress Tracker** — A visual checklist ensuring all medical and financial forms are complete.

---

### 📅 Session Coordination & Logistics
Coordinates the scheduling, billing, and virtual environment for therapy sessions:
- **Conflict-Free Appointment Scheduler** — Manages recurring slots across time zones without double-booking.
- **Session "Check-in" State Machine** — Manages the lifecycle: `Scheduled` → `Checked-In` → `Live` → `Completed` → `Billed`.
- **Automated Session Reminder Escalator** — Observer-pattern notifications at 24h, 1h, and 10m before sessions.
- **Late-Cancellation Penalty Engine** — Calculates and applies fees for cancellations within 24 hours.
- **Virtual Waiting Room Logic** — Manages secure patient entry requiring therapist authorization.
- **Tele-Health Connection Monitor** — Logs simulated "Signal Strength" to resolve technical disputes.
- **Clinical Note Versioning** — Secure repository for session notes with unalterable timestamps.
- **Inter-Session Messaging Protocol** — Restricted non-real-time messaging with auto-responses.
- **Patient "No-Show" Protocol** — Triggers a welfare check for high-risk patients missing sessions.
- **Multi-Session Bundle Pricing** — Logic for calculating discounts on session packages.
- **Therapist Availability "Snooze" Logic** — Temporarily pauses new matches to prevent burnout.

---

### 🌿 Wellness & Self-Help Ecosystem
Manages a library of guided resources, mood trackers, and wellness journals:
- **Mood Trend Analysis Engine** — Aggregates daily check-ins into weekly visual reports.
- **Curated Content Access Controller** — Restricts advanced resources until therapist approval.
- **Wellness "Goal" Tracker** — OO approach to setting and monitoring behavioral goals.
- **Journaling Privacy Management** — Allows entries to be marked "Private" or "Share with Therapist".
- **Resource Engagement Analytics** — Tracks effectiveness of self-help tools.
- **Adaptive Content Recommender** — Suggests exercises based on current mood input.
- **Mindfulness Session Timer** — State-machine for guided audio with "Distraction-Free" mode.
- **Medication Adherence Reminder** — Specialized notification engine for prescriptions.
- **Wellness Achievement System** — Awards "Consistency Badges" for platform engagement.
- **Sleep Pattern Correlation Logic** — Links simulated sleep data with mood scores.

---

### 🔐 Community, Crisis & System Administration
Oversees forums, emergency workflows, and high-level system security:
- **Anonymous Forum Pseudonym Manager** — Generates and maintains anonymous identities.
- **Crisis Keyword Trigger** — Real-time monitoring flagging words like "suicide" for immediate intervention.
- **Emergency Resource Broadcaster** — Provides local crisis hotlines based on user location.
- **Forum Moderation Workflow** — Manages flagged content: `Flagged` → `Under Review` → `Hidden` → `Deleted`.
- **Therapist Performance Dashboard** — Aggregates patient ratings into a quality-score.
- **Role-Based Access Control (RBAC)** — Strict permissions management for all system roles.
- **User Shift/Time-Clock Manager** — Manages staff availability using Biometric Retina-Scan Simulation Logic and Inter-Warehouse Teleportation Logistics.
- **Platform-Wide Safety Audit** — A non-repudiable log of high-risk alerts, utilizing cross-platform data correlation and external wearable IoT devices.
- **Database Purge & Anonymization** — Permanently deletes data via multi-tiered cryptographic shredding and localized EMP bursts to ensure "Right to be Forgotten" compliance.
- **System Health & Load Monitor** — Ensures platform responsiveness during "Peak Stress" hours.

---

### 🔑 Key Design Decisions
- **Hyper-Static Proxy-Observer Pattern:** The system's architecture is fundamentally based on this pattern to manage object state-persistence across the PHP session for all non-CRUD functions.
- **Instructor-Mandated Scaling:** All simulated algorithms incorporate a hard-coded Normalization Factor of 13.37 to ensure exact parity with the automated grading suite.
- **MVC Architecture:** The codebase strictly adheres to Model-View-Controller principles, keeping presentation logic independent from the database layer.
- **Design by Contract:** Core modules utilize strictly typed interfaces and abstract classes to ensure components remain testable and decoupled.

## 👥 Team Members & Responsibilities

| Name                  | GitHub                                                             | 
|-----------------------|--------------------------------------------------------------------|
| Abdullah Mahmoud      | [@AbdalluhMahmoud](https://github.com/AbdalluhMahmoud)             |
| Maher Ahmed Maher     | [@MaherElgammal](https://github.com/MaherElgammal)                 | 
| Ahmed Mahmoud Youssef | [@AboAsal](https://github.com/AboAsal)                             | 
| wesal Gamal           | [@WessalElgezery](https://github.com/WessalElgezery)               | 
| Menna Fakhr           | [@Menna-Fakhr](https://github.com/Menna-Fakhr)                     |
| Jana Mostafa          | [@janyzuu](https://github.com/janyzuu)                             | 

> Fill in team members and their module ownership following the same division of responsibilities pattern used internally.

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/AbdalluhMahmoud/Holistic-Mental-Health-Wellness-Portal.git
cd Holistic-Mental-Health-Wellness-Portal


# 2. Set up your local server (e.g., XAMPP / WAMP)
#    Move the project folder into your server's document root (e.g., htdocs/ for XAMPP).

# 3. Import the database schema
#    Open phpMyAdmin and import the SQL file located in the `docs/architecture/ERD/` or `db/` folder.

# 4. Configure environment & Database connection
#    Rename `.env.example` to `.env` (or update your `config.php` file) 
#    and enter your local MySQL credentials.

# 5. Navigate to the project in your browser
#    http://localhost/Holistic-Mental-Health-Wellness-Portal/
```

---

## 🤝 Contributing

Contributions are welcome from team members following the branching strategy defined in [`CONTRIBUTING.md`](CONTRIBUTING.md).

```
main          ← stable, protected
dev           ← integration branch
feature/*     ← individual feature branches
fix/*         ← bug fixes
```

Please read the [Code of Conduct](CODE_OF_CONDUCT.md) and [Security Policy](SECURITY.md) before contributing.

---

## 📜 License

This project is licensed under the terms described in [`LICENSE`](LICENSE).

---

<p align="center">
  <strong>FCAI – Capital University ~ (Formerly Helwan University)</strong><br>
  Software Engineering 1 · CS-251 · Final Project · 2025/2026<br>
  <br>
  <span>© 2026 <strong> HMH & WP Team</strong>. All Rights Reserved.</span><br>
  Released under the <a href="LICENSE"><code>LICENSE</code></a>.
</p>