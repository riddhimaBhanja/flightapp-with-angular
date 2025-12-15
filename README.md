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
##  Overall Flow

![WhatsApp Image 2025-12-15 at 11 24 00 PM](https://github.com/user-attachments/assets/b3cdcfa3-8ae2-4885-8791-7a2583769d37)

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
![home page](https://github.com/user-attachments/assets/e9bbd22d-0962-4b76-91fa-15fcd28bbec1)

---


##  Login Page

![login page for searching flights](https://github.com/user-attachments/assets/465aa6ad-546c-4fb2-9cb5-5b2fc567764d)

---

##  Search Flights
![search flights page](https://github.com/user-attachments/assets/1ce480e0-8b86-46e6-9089-815d715aca3b)

---

##  Create Account
![creating account(register)](https://github.com/user-attachments/assets/c4fce153-ca26-4f98-91eb-a548bccfdce8)

---

##  Login Successful
![login successful](https://github.com/user-attachments/assets/3716f344-cb7a-46a8-9aab-1256f16ec42b)


---

##  Registration page Validation Error
![validation errors(registration)](https://github.com/user-attachments/assets/f42956f1-972e-46ed-bf66-aada0c771416)

---

##  Search Flights Validation Error
![search flights validation error](https://github.com/user-attachments/assets/42d43fbb-4d01-4b25-ae5d-c6a9cd9d018e)

---

##  Login Validation Error
![login validation errors](https://github.com/user-attachments/assets/e78f59fe-8fb7-430d-a48a-ef46e92f262f)

---
##  Email Validation Error
![email validation error](https://github.com/user-attachments/assets/ff7adc1c-50d5-4add-858c-41d53e681469)

---

##  Frontend Validation Rules

All essential validations are handled at the frontend level to ensure data integrity, prevent invalid submissions, and provide immediate user feedback.

---

###  Search Form Validations

* Source field is mandatory
* Destination field is mandatory
* Source and Destination cannot be the same
* Travel Date is required
* Past dates are restricted and cannot be selected

---

###  Login Form Validations

* Email field is required
* Email must follow a valid format
* Password field is required

---

###  Registration Form Validations

* Name field is mandatory
* Email field is required and format-validated
* Password field is required
* Submit button remains disabled until the form is valid


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
##  CODE COVERAGE BREAKDOWN
![code coverage breakdown -1](https://github.com/user-attachments/assets/dbd9b003-242d-4e52-906e-1140ad04bde8)

![code coverage breakdown -3](https://github.com/user-attachments/assets/522b4afd-cc48-4583-a8b6-54e9bf961f11)


##  API Integration

**Base URL:** `http://localhost:8080`

### Authentication

* `POST /api/auth/login`
* `POST /api/auth/register`

### Flights

* `POST /api/flights/search`
* `GET /api/flights/inventory/{id}`

---
### Test Run with UI
![test run with ui](https://github.com/user-attachments/assets/b42aee4d-b05c-43b2-b76c-138a1d88bb0b)

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


