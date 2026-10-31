# Campus Pulse — Modern College Notice & Event Management Portal

**Campus Pulse** is a modern, student-first college announcement, circular intelligence, and campus event management website. It provides university students, faculty, and administrators with a single, elegant platform to view circulars, stay on top of critical examination deadlines, register for collegiate hackathons, and summarize unformatted circular texts using an AI-inspired client-side assistant.

---

## 📁 Professional Folder Structure

```
campusplus/
├── index.html                  # Home Dashboard & AI Smart Notice Assistant
├── README.md                   # Complete Documentation & Run Instructions
├── pages/                      # Dedicated Subpages
│   ├── notices.html            # Searchable & Filterable Notice Board
│   ├── events.html             # Campus Events & Registration Portal
│   ├── admin.html              # Full Admin CRUD Management (LocalStorage)
│   └── contact.html            # Helpdesk, Feedback Form & FAQ Accordion
├── css/                        # Modular Stylesheets
│   ├── style.css               # Core Palette, Typography, Cards, Modals
│   ├── animations.css          # Keyframes, Micro-Interactions & Hover Glows
│   └── responsive.css          # Mobile, Tablet & Desktop Breakpoints
├── js/                         # Organized Application Scripts
│   ├── data.js                 # Central DataStore, LocalStorage & Helpers
│   ├── main.js                 # Home Dashboard & AI Assistant Logic
│   ├── notices.js              # Notice Board Search & Filter Engine
│   ├── events.js               # Events & Seat Registration Handlers
│   ├── admin.js                # Notice & Event CRUD Operations
│   └── contact.js              # Contact Form Validation & FAQ Handlers
├── data/
│   └── sample-data.json        # Exported JSON Dataset for Reference
└── assets/                     # Visual Assets & Icons
    ├── icons/
    │   ├── pulse-logo.svg      # Custom Vector Brand Logo
    │   └── favicon.svg         # SVG Browser Favicon
    ├── images/
    │   └── hero-illustration.svg # Custom Dashboard Vector Illustration
    └── fonts/                  # Font Assets Directory
```

---

## 🌟 Key Features

### 1. Home Dashboard (`index.html`)
- **Modern Navigation**: Seamless links to Home, Notices, Events, Admin, and Contact, with a mobile-responsive hamburger menu.
- **Hero Section**: Clean welcome banner, tagline, vector illustration, and quick action buttons.
- **Executive Briefing Modal**: Triggered by **"✨ What do I need to know this week?"**, showing high-priority deadlines, hackathons, and a 7-day timeline.
- **Live Summary Counters**: Real-time indicators showing Total Notices, Active Events, Urgent Deadlines, and Student Registrations.
- **Important Announcements**: Highlights urgent and pinned official circulars with a "Read Full Notice" modal.
- **Upcoming Events Preview**: Live event cards displaying remaining seats and instant registration triggers.
- **AI Smart Notice Assistant**:
  - Enter or paste unformatted circulars or WhatsApp messages.
  - "Insert Sample Circular" button for quick 1-click hackathon evaluation.
  - "Summarize Notice" button with simulated AI analysis animation.
  - "Extract Event to Calendar" button to parse notices and register them directly to the events calendar.
  - *Demo Feature Disclaimer: Runs 100% locally with client-side NLP heuristics — no external API key required.*

### 2. Notice Board (`pages/notices.html`)
- **Search Engine**: Instant live search by keyword, title, issuing authority, or department.
- **Category Filter Pills**: Filter circulars by **All**, **Academic**, **Exams**, **Events**, or **General**.
- **Urgent Notice Highlighting**: Red alert borders and an "🚨 Urgent Only" toggle.
- **Notice Details Modal**: Full text display with issuing department and publication date.
- **Empty State**: Friendly illustration and "Reset Filters" action when searches find no matches.

### 3. Events & Registrations (`pages/events.html`)
- **Activity Cards**: Displays event title, date, time, venue, category, and description.
- **Live Seat Tracking**: Real-time counter of available seats vs. total capacity.
- **Event Registration Modal**: Students submit their name, roll number, college email, and department.
- **Instant Confirmation**: Registers the student, decrements available seats, saves records to `localStorage`, and updates the button to `✓ Registered`.

### 4. Admin Dashboard (`pages/admin.html`)
- **Dual Panel Architecture**:
  - **Manage Notices**: Add, edit, and delete circulars with department, category, urgency, date, and pinned status.
  - **Manage Events**: Add, edit, and delete events with date, time, venue, seats, and descriptions.
- **Edit Modal**: Modify any published notice or scheduled event in an interactive pop-up.
- **Delete Confirmation**: Safety checks before permanently deleting items.
- **Cross-Page Synchronization**: Changes persist in browser `localStorage` and immediately update student-facing pages (`index.html`, `pages/notices.html`, `pages/events.html`).
- **Data Management Controls**: "Reset to Sample Data" and "Clear All Data" buttons for testing.
- *Notice: Clearly labeled as a client-side prototype demonstration with no complex backend setup required.*

### 5. Contact & Helpdesk (`pages/contact.html`)
- **Inquiry Form**: Validates Name (min 2 chars), College Email (valid email check), and Message (min 8 chars).
- **Success Feedback**: Clear confirmation banner upon form submission (client-side demo without external transmission).
- **Campus Helpdesk Info**: Phone helpline, office hours, email, and physical office room details.
- **Interactive FAQ Accordion**: Expandable answers to common questions regarding notices, event bookings, and portal usage.

---

## 🚀 How to Run the Website

### Method 1: Direct Browser Launch (Simplest)
1. Open File Explorer and navigate to your project folder:
   ```
   C:\Users\Shagun\OneDrive\Desktop\campusplus
   ```
2. Double-click [index.html](file:///c:/Users/Shagun/OneDrive/Desktop/campusplus/index.html).
3. The site opens immediately in your web browser.

### Method 2: VS Code Live Server (Recommended)
1. Open your VS Code editor inside the `campusplus` folder.
2. In the file explorer, right-click on `index.html`.
3. Click **"Open with Live Server"**.
4. The site will launch automatically at `http://127.0.0.1:5500/index.html`.

---

## 🎨 Design System

- **Palette**: Deep Navy Blue (`#0a1128`, `#001f54`), Royal Blue (`#034078`), Light Cyan Blue (`#00b4d8`, `#48cae4`), and Clean White (`#ffffff`, `#f8fafc`).
- **Typography**: `Plus Jakarta Sans` with modern system sans-serif fallbacks.
- **Responsiveness**: Tested across desktop (1200px+), tablet (768px - 1024px), and mobile (under 768px) with a dedicated mobile slide-down menu.
- **Visuals**: Self-contained SVG icons and vector illustrations with zero broken links or missing CDN assets.
