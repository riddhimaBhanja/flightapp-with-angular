#  Flight Booking Angular Frontend

A modern, elegant, and production-ready **Angular frontend** for a Flight Booking System, designed with a strong focus on usability, clean architecture, and seamless authentication-driven workflows.

---

##  Overview

This application delivers a smooth end-to-end flight booking experience—from secure user authentication to real-time flight search—wrapped in a visually rich, responsive interface.
It follows industry-standard Angular practices, ensuring scalability, maintainability, and clarity for both learning and real-world deployment.

---

##  Key Highlights

* Clean and intuitive UI with modern gradients and animations
* Secure authentication using JWT
* Fully protected flight search flow
* Reactive, real-time form validation
* Modular and maintainable architecture
* Optimized for both desktop and mobile devices

---

##  Core Features

###  Home (Landing Page)

* Attractive hero section with clear call-to-action
* Feature cards highlighting system capabilities
* Authentication-aware navigation
* Fully responsive layout

###  User Authentication

#### Login

* Minimal and elegant login interface
* Required field validation
* Friendly error messages
* Loading indicators during authentication
* Automatic redirection when already authenticated

#### Registration

* Structured registration form with validations:

  * Username (3–50 characters)
  * Valid email format
  * Password (minimum 6 characters)
  * Confirm password match
* Real-time validation feedback
* Smooth post-registration redirection

###  Flight Search

* Protected route (authentication required)
* Search by origin, destination, and travel date
* Real-time results rendering
* Rich flight cards displaying:

  * Airline & flight number
  * Route details
  * Departure & arrival timings
  * Flight duration
  * Seat availability
  * Price and status indicators
* Graceful empty and error states
* Logout access from navigation bar

---

##  Application Architecture

### Component-Driven Design

* Clear separation of concerns
* Reusable and testable components
* NgModule-based structure (non-standalone)

### Routing & Navigation

* Angular Router configuration
* Auth-guarded protected routes
* Smart redirection for authenticated users
* Fallback route handling

### Services Layer

* **Authentication Service**

  * Login & registration handling
  * JWT storage via `localStorage`
  * User state management using `BehaviorSubject`
  * Centralized logout

* **Flight Service**

  * Flight search integration
  * Flight detail retrieval
  * HTTP abstraction layer

### Security

* Route protection using Auth Guard
* JWT injection via HTTP Interceptor
* Centralized authentication state

---

##  Project Structure

```
flight-booking-app/
├── src/
│   ├── app/
│   │   ├── components/
│   │   │   ├── home/
│   │   │   ├── login/
│   │   │   ├── register/
│   │   │   └── flight-search/
│   │   ├── services/
│   │   ├── guards/
│   │   ├── interceptors/
│   │   ├── models/
│   │   ├── app.ts
│   │   ├── app.html
│   │   ├── app.scss
│   │   ├── app-module.ts
│   │   └── app-routing-module.ts
│   ├── index.html
│   ├── main.ts
│   └── styles.scss
├── angular.json
├── package.json
├── tsconfig.json
└── README.md
```

---

##  Prerequisites

* Node.js (v18+)
* npm (v9+)
* Angular CLI (v21+)
* Backend API running on `http://localhost:8080`

---

##  Installation & Setup

```bash
cd flight-booking-app
npm install
```

### Start Backend (Docker)

```bash
docker-compose up
```

### Start Frontend

```bash
ng serve
```

 Application runs at: `http://localhost:4200`

---

## Default Access

If enabled in backend:

* **Username:** admin
* **Password:** password

Otherwise, create a new account via registration.

---

## Routes

| Route         | Description               |
| ------------- | ------------------------- |
| `/` , `/home` | Landing page              |
| `/login`      | User login                |
| `/register`   | User registration         |
| `/flights`    | Flight search (protected) |

---

##  API Integration

**Base URL:** `http://localhost:8080`

### Authentication

* `POST /api/auth/login`
* `POST /api/auth/register`

### Flights

* `POST /api/flights/search`
* `GET /api/flights/inventory/{id}`

---

##  Technologies Used

* **Angular 21**
* **TypeScript 5.9**
* **RxJS 7.8**
* **SCSS** for advanced styling
* **Angular Reactive Forms**
* **Angular Router**
* **Angular HTTP Client**

---

## Application Flow Summary

### Authentication

1. User submits credentials
2. Data validated via Reactive Forms
3. JWT received and stored
4. User state updated reactively
5. Secure navigation enabled

### Flight Search

1. Auth-guard validation
2. Search request sent to backend
3. Results rendered dynamically
4. Errors and empty states handled gracefully

---

## Build for Production

```bash
ng build --configuration production
```

Artifacts are generated in the `dist/` directory.

---

##  Troubleshooting

* **CORS Issues:** Allow `http://localhost:4200` in backend
* **API Errors:** Verify Docker containers and logs
* **Auth Issues:** Confirm JWT storage and interceptor behavior

---

##  Final Note

This project is structured to reflect real-world frontend engineering standards—clean code, thoughtful UX, and secure workflows—making it suitable for both professional deployment and academic or training use.

---


