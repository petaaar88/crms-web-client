# CRMS Web Client
React.js web application for the Customer Relationship Management System (CRMS). It enables employees and administrators to manage partners, reports, plans, assignments, and announcements.

The application helps users track and organize visits to healthcare companies such as pharmacies. During each visit, users can record details about the contacted person, their role, visit date, and the outcome rating — an indicator of potential business opportunities. 

## Table of Contents

1. <a href="#features">Features</a>
2. <a href="#built-with">Built with</a>
3. <a href="#setup-instructions">Setup Instructions</a>
4. <a href="#architecture-overview">Architecture Overview</a>
5. <a href="#screenshots">Screenshots</a>
6. <a href="#detailed-documentation">Detailed Documentation</a>


## Features
- **Partners and Reports module** — centralizes client information and tracks detailed visit reports (participants, outcomes, and discussion summaries).

- **Plans module** — allows users to create personal visit and task plans, providing an overview of upcoming activities for better daily organization.

- **Assignments module** — enables administrators to assign tasks to users, ensuring coordination and tracking of task completion.

- **Announcements module** — allows administrators to send system-wide announcements that appear as notifications to users, improving internal communication.

- **Manage module** — provides administrators with tools to add new users, monitor their clients and reports, and assign individual tasks, giving full control over team operations and resources.
- **Secure authentication** (login, access token refresh)
- **Role-based access control** (Admin, User)
- **Search, pagination, and filtering utilities**
- **Responsive UI**
- **Dark and light theme**


##  Built with

- <img src="https://cdn.simpleicons.org/react/61DAFB" height="13" title="React" /> React 18 + <img src="https://cdn.simpleicons.org/vite/646CFF" height="13" title="Vite" /> Vite 5
- <img src="https://cdn.simpleicons.org/reactrouter/CA4245" height="13" title="React Router" /> React Router DOM 7
- <img src="https://cdn.simpleicons.org/mui/007FFF" height="13" title="MUI" /> Material UI (MUI)
- <img src="https://cdn.simpleicons.org/tailwindcss/06B6D4" height="13" title="Tailwind CSS" /> Tailwind CSS 4
-  Recharts (dashboards/visualizations)



##  Setup Instructions

### Prerequisites
- **Node.js 20+** (recommended for compatibility)
- **npm** (comes bundled with Node.js)

### Instalation
1. Clone the backend (required dependency)

   This project depends on [petar88/crms-backend](https://github.com/petaaar88/crms-backend)
   ```
   git clone https://github.com/petaaar88/crms-backend.git
   ```
   ```
   cd crms-backend
   ```
   Follow the backend’s own setup instructions, then start it.

2. Clone this project

   ```
   git clone https://github.com/petaaar88/crms-web-client.git
   ```
   ```
   cd crms-web-client
   ```

2. Install dependencies
   ```
   npm install
   ```
3. Configure environment

   Copy `.env.example` to `.env`

   Set `VITE_API_URL` to your backend URL (e.g., `http://localhost:3000`)

### Run

   Development: 
   ```
   npm run dev
   ```
   Preview production build: 
   ```
   npm run build && npm run preview
   ```


##  Architecture Overview
All data — like user login, partners, reports, and assignments — is exchanged with the backend through HTTP requests.
The backend provides REST API endpoints, and the React app communicates with them.

The application is organized into well-defined folders that separate concerns:

- **`pages/`** — top-level views representing individual routes (e.g., LoginPage, PlansPage, AssignmentsPage).  
- **`components/`** — reusable UI components used across multiple pages.  
- **`contexts/`** — React Contexts for managing global state such as authentication, theme, and user details.  
- **`hooks/`** — custom hooks that encapsulate logic for data fetching, input handling, and UI state.  
- **`layouts/`** — shared layout structures.  
- **`utils/`** — helper functions for formatting, filtering, and managing API responses.  



### Folder structure
```
src/
├─ assets/
├─ components/
├─ contexts/
├─ hooks/
├─ layouts/
├─ lib/
├─ pages/
│  ├─ AnnouncementsPage/
│  ├─ AssignmentsPage/
│  ├─ HomePage/
│  ├─ LoadingPage/
│  ├─ LoginPage/
│  ├─ ManagePage/
│  ├─ PartnersAndReportsPage/
│  └─ PlansPage/
├─ types/
└─ utils/
```
##  Screenshots 

### Login Page

![Login page showing username/password fields and Login button](/docs/images/9.png "Login Page")
Shows the login form with credential inputs.

### Home Page
![Dashboard with with user details and activties for current day](/docs/images/10.png "Home Page")
Shows user details and activities for current day.


### Partners and Reports
![Partners and reports list with filters](/docs/images/11.png "Partners and Reports")
Browse partners and filter results.

### Mobile View
![Responsive mobile layout of the dashboard](/docs/images/12.png "Mobile View")

Mobile optimized view demonstrating responsive dashboard.

### Create Partner
![Create partner form with contact and company fields](/docs/images/13.png "Create Partner")
Form to add a new partner with validation and required fields.

### Analytics
![Analytics page with trend charts and top partner breakdowns](/docs/images/14.png "Analytics")
Visualizes trends and performance across key metrics.

### Plans
![Manage plans](/docs/images/15.png "Plans")
Manage plans.

### Announcements
![Organization updates and announcements](/docs/images/16.png "Announcements")
Organization updates and announcements.

## Detailed Documentation

For deeper technical details, refer to: [DOCS.md](docs/DOCS.md)


