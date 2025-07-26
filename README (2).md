**FreelanceFinder: Discovering Opportunities, Unlocking Potential**

**1. Introduction**

FreelanceFinder is a full-stack MERN (MongoDB, Express.js, React.js, Node.js) application
designed to connect clients seeking specialized services with freelancers offering diverse
skillsets. It aims to create an efficient, transparent, and secure freelancing environment
where clients can post projects and freelancers can bid on and complete them with ease^1.

**2. Project Overview**

The purpose of FreelanceFinder (referred to as SB Works in the documentation) is to bridge
the gap between clients and freelancers^2. It provides a seamless and supportive platform for
individuals to build a strong freelance portfolio and connect with clients^3.

**Features:**

```
 User-Friendly Interface : Intuitive and responsive design for easy navigation^4.
 Project Posting & Bidding : Clients can post projects, and freelancers can bid based
on their skills and experience^5.
 Integrated Chat System : Enables real-time communication and collaboration^6.
 Secure File Submissions : Freelancers can submit completed work securely^7.
 Admin Oversight : Ensures secure transactions, resolves disputes, and maintains
platform integrity^8.
 Feedback System : Clients can review submitted work and provide ratings and
comments^9.
 Real-Time Notifications : Keeps users updated with project activities and new
opportunities^10.
 Scalable Architecture : Powered by MongoDB, Express.js, and REST APIs with a
responsive frontend using Bootstrap and Material UI^11.
```
**3. Architecture**

**Frontend**

The frontend is built with React.js for a dynamic, responsive, and modular user interface^12. It
uses Axios for API integration and React Router for navigation^13. UI elements are styled with
Bootstrap and Material UI^14. Components are structured by user roles (Client, Freelancer,
Admin) and feature-based directories^15.

**Backend**


The backend is developed using Node.js and the Express.js framework^16. It exposes RESTful
APIs for user authentication, project management, messaging, and submission workflows^17.
Middleware is used for request validation, session management, and error handling, and
role-based access control is enforced^18.

**Database**

FreelanceFinder uses MongoDB for flexible, schema-less data storage^19. Key collections
include:

```
 Users : Stores freelancer, client, and admin profiles with roles and credentials^20.
 Projects : Contains project details, bidding data, and project status^21.
 Bids : Tracks freelancer proposals, bid amounts, and timelines^22.
 Messages : Maintains communication threads between users^23.
 Submissions : Handles file uploads and final work delivery^24.
```
**4. Setup Instructions**

**Prerequisites:**

To run the FreelanceFinder platform locally, ensure you have the following installed:

```
 Node.js (version 14.x or above)^25
 npm (Node Package Manager)^26
 MongoDB (local installation or MongoDB Atlas account)^27
 Git (to clone the repository)^28
```
**5. Folder Structure**

**Client:**

The frontend (React) is organized into role-based and reusable components^29.

client/

├── public/ # Public assets like index.html and favicon [cite: 50 , 51 ]

└── src/

├── components/ # Reusable UI components (Navbar, Login, Register, etc.) [cite: 53,
54]

├── context/ # React Context for global state management [cite: 55 , 56 ]

├── pages/


│ ├── admin/ # Admin dashboard and management pages [cite: 58 , 59 ]

│ ├── client/ # Client-specific pages (Post project, My Projects) [cite: 60 , 61 ]

│ └── freelancer/ # Freelancer-specific pages (Bid, Submit work) [cite: 62]

├── App.js # Main app component with routes [cite: 63 , 64 ]

├── index.js # Entry point [cite: 65 , 66 ]

└── utils/ # Utility functions (API helpers, validators) [cite: 67, 68]

package.json # Project metadata and dependencies [cite: 69, 70]

**Server:**

server/

├── controllers/ # Logic for handling requests (auth, projects, users) [cite: 73 ]

├── models/ # Mongoose schemas for Users, Projects, Bids, Messages [cite: 73 ]

├── routes/ # Express routes grouped by modules (auth, users, projects) [cite: 73 ]

├── middleware/ # Custom middleware (auth check, error handling) [cite: 73 ]

├── config/ # Database config and environment setup [cite: 73 ]

├── uploads/ # Folder to store submitted files [cite: 73 ]

├── .env # Environment variables (not committed) [cite: 73 ]

├── server.js # Entry point for Express server [cite: 73 ]

└── package.json # Backend dependencies and scripts [cite: 73 ]

**6. Running the Application:**

To run the FreelanceFinder platform locally after completing setup and installation, follow
these steps in two separate terminal windows or tabs:

**Frontend:**

Navigate to the client directory and start the React app:

Bash

cd client [cite: 77]

npm start [cite: 79]

**Backend:**

Navigate to the server directory and start the Express server:


Bash

cd server [cite: 81]

npm start [cite: 82]

## 7. Screenshots:

**Sign In Page:**
![Sign In Page](screenshots/Screenshot%202025-07-26%20112052.png)

**Job Post Page:**
![Job Post Page](screenshots/Screenshot%202025-07-26%20112215.jpg)

**Find Jobs Page:**
![Find Jobs Page](screenshots/Screenshot%202025-07-26%20112104.jpg)

**About Us Page:**
![About Us Page](screenshots/Screenshot%202025-07-26%20112231.jpg)

**Find Your Dream Job with Ease Page:**
![Find Your Dream Job with Ease Page](screenshots/Screenshot%202025-07-26%20112253.jpg)

**Companies Page:**
![Companies Page](screenshots/Screenshot%202025-07-26%20112133.jpg)

**8. Demo Video Link**

You can watch a demo of the FreelanceFinder application here:

https://drive.google.com/file/d/19drB01P5vrVDmYa4v2RiWBVpd4IWKUAb/view?usp=sharin
g 30

**9. Authentication**

FreelanceFinder uses JWT (JSON Web Tokens) for authentication and role-based
authorization^31.


**Login Process:**

```
 Users log in via email and password^32.
 On success, the server issues a JWT token^33.
 The token is stored in the browser's localStorage^34.
```
**Token Usage:**

```
 The token is included in the
```
Authorization header for all protected API requests^35.

```
 Example:
```
Authorization: Bearer <token>^36

**10. User Interface**

FreelanceFinder offers a clean, responsive UI designed with React, Bootstrap, and Material
UI^37.

**Key UI Features:**

```
 Landing Page : Overview of the platform and call to action^38.
 Client Dashboard : Project creation and management^39.
 Freelancer Dashboard : Browse and bid on projects^40.
 Admin Panel : User and project oversight^41.
 Chat Interface : In-platform communication between clients and freelancers^42.
 Project Submission & Review : Upload and feedback system^43.
```
**11. Testing**

**Testing Strategy:**

```
 Manual Testing : Performed on all major user flows, including user registration and
login, project posting and bidding, file submission and feedback, and role-based
dashboard access^44444444.
 API Testing : Done using Postman to verify backend endpoints, covering auth routes,
project creation and retrieval, bid submission, and user profiles^454545454545454545.
 Unit Testing (Planned for future) : Will use Jest for backend logic, focusing on
controllers and middleware functions^46.
```
**Tools Used:**


```
 Postman : For API testing and response validation^47.
 Chrome DevTools : For UI inspection and debugging^48.
 MongoDB Compass : For database verification^49.
```
**12. Known Issues**

```
 Real-Time Messaging : The chat system currently lacks real-time updates (no
WebSocket/socket.io integration)^50.
 Validation : Some form fields lack comprehensive client-side validation (e.g., file type,
input length)^51.
 Notification System : Email or in-app notifications are not yet implemented^52.
 Error Handling : Backend error messages need more descriptive responses for
debugging^53.
```
**13. Future Enhancements**

```
 Real-Time Chat : Integrate Socket.io for live messaging and notifications^54.
 Payment Gateway Integration : Add Stripe/Razorpay for secure client-freelancer
transactions^55.
 Admin Analytics Dashboard : Provide visual insights into platform usage, top
freelancers, and active projects^56.
 Freelancer Endorsements : Enable ratings, reviews, and skill endorsements from
clients^57.
 Mobile App : Build a cross-platform mobile app using React Native^58.
 Two-Factor Authentication (2FA) : Improve login security with OTP/email
verification^59.
 Multi-language Support : Localize the app for broader user reach^60.
```

