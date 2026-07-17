# Software-Engineering-Lab

## Team Members

| Name | Registration No. | Exam Roll|
| :--- | :--- | :--- |
| **Najmul Huda** | *202204012* | *412* |
| **Zuel Rana** | *202204011* | *411* |
| **Md. Samiul Islam Pias** | *202204024* | *423* |

[Fork & Pull Request Guide](https://najmul-huda70.github.io/Software-Engineering-Lab/)

# Netrokona University Computer Club

## Project Requirements

A production-ready full-stack web application for the Computer Club, Department of CSE, Netrokona University.

---

## 1. Technology Stack

**Frontend**
- Next.js
- TypeScript 
- Tailwind CSS
- Recharts (for stats/analytics visuals)
- Better Auth (for user login and registration)
  
**Backend**
- Express.js 
- TypeScript (mandatory)
- MongoDB
- JWT-based authentication


## 2. Site Structure & Pages

### 2.1 Home (`/`)
- Sticky navbar — logged out: Home, Events, About, Contact + Join club CTA; logged in: + Add event, Manage events, Profile
- Hero (60–70vh): tagline, upcoming-event slider, dual CTA
- Sections (8): About the club, Why join, Upcoming events, Club statistics, Testimonials, Blog/news, FAQ, Newsletter, final CTA
- Fully functional footer: explore links, account links, contact info, social links

### 2.2 Events listing (`/events`)
- Search bar (by name)
- Filters: Category (Contest / Fest / Workshop / Sports / Seminar / Social / Election) + Date range + Fee — minimum 2 filter fields met
- Sort: date, fee (asc/desc), popularity
- Pagination (page numbers)
- Card grid: 4/row desktop, skeleton loader on load
- 12 real events seeded (see §5)

### 2.3 Event details (`/events/[id]`) — public
- Image gallery (multiple visuals)
- Overview / description
- Key info / specifications (date, time, venue, fee)
- Reviews / ratings
- Related events
- Sidebar: fee, CTA to register/apply

### 2.4 Authentication
- `/login` — email + password, validation, demo-login button, social login buttons (Google/Facebook — optional/decorative), link to register
- `/register` — full name, student ID, batch/year, email, password + confirm, terms checkbox, validation

### 2.5 Protected: Add item (`/events/add` or `/election/apply`)
- Redirect to `/login` if not authenticated
- Fields: Title, short description, full description, category, date, priority/position, fee, optional image URL, file upload
- Submit / Cancel actions

### 2.6 Protected: Manage items (`/events/manage` or `/election/manage`)
- Role-based: normal member vs Election Commission/admin
- Table: name/title, category, batch, fee, status (pending/approved/disqualified), actions (view, delete/approve)
- Clean, responsive table layout

### 2.7 Additional pages
- `/about` — club story, budget transparency, election commission leadership
- `/contact` — contact form + direct contact info + map placeholb— real address
- `/privacy`, `/terms` — footer-linked policy pages

---

## 3. Non-functional requirements

- No placeholder/lorem ipsum content anywhere
- Consistent card size, radius, spacing across all listings
- Fully responsive (mobile/tablet/desktop) on every page
- Role-based route protection (JWT middleware) for `/events/add`, `/events/manage`, election apply/manage routes
- All buttons and links functional (no dead links)
- Skeleton loading states for async data fetches

---

