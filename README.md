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
##  Home Page
![home page](https://github.com/user-attachments/assets/352cabef-353b-493f-88b2-41b9beaf4548)

---


##  Login Page

<img width="959" height="471" alt="image" src="https://github.com/user-attachments/assets/bf41784b-523f-4f7a-a371-086ba690ed1c" />

---
##  Create Account
![creating account(register)](https://github.com/user-attachments/assets/518a6566-d6c5-4c81-a68b-b6eac02fc64d)

---

##  Login Successful
![login page for searching flights](https://github.com/user-attachments/assets/822180ef-f35a-4707-b694-d482010ffc73)

---


##  Search Flights
![search flights page](https://github.com/user-attachments/assets/383a3eca-a29a-448b-acba-bf2b2b08821c)

---

##  Registration page Validation Error
![validation errors(registration)](https://github.com/user-attachments/assets/af4038bd-396f-4661-9dd2-a3bb5046f46d)


---

##  Search Flights Validation Error
![search flights validation error](https://github.com/user-attachments/assets/0730e20b-d714-4116-a252-fe8fc6644e31)

---

##  Login Validation Error
![login validation errors](https://github.com/user-attachments/assets/77a2b640-cdcc-40c4-adaa-c75513df1768)


---
##  Email Validation Error
![email validation error](https://github.com/user-attachments/assets/6c24b65d-6606-4910-9394-f0a5140acca2)

---

All critical validations are implemented on the frontend:
Search Form

Source is required

Destination is required

Source and Destination cannot be the same

Date is required

Past dates are not allowed

Login Form

Email is required

Valid email format enforced

Password is required

Register Form

Name is required

Email is required and validated

Password is required

Submit disabled if form is invalid

Validation messages are shown immediately to guide users.

---
##  Code Coverage
![code coverage report(all files)](https://github.com/user-attachments/assets/4a9881d5-2220-441b-82db-896505499818)

---

##  ER Diagram
![WhatsApp Image 2025-12-15 at 10 48 58 PM](https://github.com/user-attachments/assets/d699149b-be8e-4aab-9543-d256c79c86c3)


---


##  Architecture Diagram
![WhatsApp Image 2025-12-15 at 10 48 59 PM](https://github.com/user-attachments/assets/ae63f580-a275-4742-adb6-efc2bd62124d)

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

##  Final Note

This project is structured to reflect real-world frontend engineering standards—clean code, thoughtful UX, and secure workflows—making it suitable for both professional deployment and academic or training use.

---


