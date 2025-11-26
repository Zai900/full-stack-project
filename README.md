📘 After-School Activity Club — CST3144 Full Stack Project

This project is a full-stack web application created for the CST3144 Full Stack Development coursework.
It allows users to view, search, sort, and book after-school lessons using a Vue.js frontend and a Node.js + MongoDB backend.

Live Application
Frontend (Vue.js + GitHub Pages)

🔗 https://zai900.github.io/Front-End-App/

Backend API (Node.js + Express + MongoDB + Render)

🔗 https://zainab-backend.onrender.com

Main Lessons Endpoint

🔗 https://zainab-backend.onrender.com/lessons

Technologies Used
Layer Technology
Frontend Vue.js 2, HTML, CSS, JavaScript
Backend Node.js, Express.js
Database MongoDB Atlas (Native Driver)
Deployment GitHub Pages (frontend), Render.com
Tools Git, GitHub, Postman

Features Implemented
Lessons Display

Displays each lesson with:

Subject

Location

Price

Spaces

Image

Searching

Search lessons by subject or location (case-insensitive).

Sorting

Sort lessons by:

Subject

Location

Price

Spaces

Supports ascending and descending order.

🛒 Shopping Cart

Add lessons to cart

Increase / decrease quantity

Remove individual lessons

Updating available spaces visually

Prevent “Add to Cart” when spaces = 0

Real-time total price

🧾 Checkout Form

Includes validation:

Name → letters only

Phone → numbers only

City → required

Order submission through POST.
Cart clears on success.

Lesson Reset Function (Custom Feature)

After an order is submitted:

✔ ALL lessons reset back to 5 spaces automatically

(This was the student's chosen custom design feature.)

🔌 API Endpoints (Backend)
GET /lessons

Returns all lessons.

Example Response:
[
{
"_id": "691cc49b8278f34a49e58816",
"subject": "Basketball Skills",
"location": "Sports Hall B",
"price": 14,
"spaces": 5,
"image": "basketball.jpg"
}
]

POST /orders

Submit an order.

Example Request:
{
"name": "Zainab",
"phone": "07123456789",
"city": "London",
"items": [
{ "lessonId": "691cc49b8278f34a49e58816", "quantity": 1 }
]
}

Example Response:
{
"message": "Order created",
"orderId": "69220b29d010e6adf7b6fdd01"
}

PUT /lessons/:id

Updates lesson fields (spaces updated/reset).

Example:
{
"spaces": 5
}

🧪 How to Run Locally

1. Clone the Repos
   Frontend:
   git clone https://github.com/Zai900/Front-End-App.git

Backend:
git clone https://github.com/Zai900/Zainab_backend.git

2. Backend Setup

Inside the backend folder:

npm install

Create .env:

MONGODB_URI=YOUR_ATLAS_CONNECTION_STRING
PORT=5000

Run server:

npm start

Backend runs at:
👉 http://localhost:5000

3. Frontend Setup

Open index.html in a browser
OR use VS Code Live Server.

API Base URL in app.js:
For production:
const API_BASE = "https://zainab-backend.onrender.com";

For local development:
const API_BASE = "http://localhost:5000";

Orders Collection Example (MongoDB)
{
"\_id": "69220b29d010e6adf7b6fdd01",
"name": "Zainab",
"phone": "07123456789",
"city": "London",
"items": [
{ "lessonId": "691cc49b8278f34a49e58816", "quantity": 1 }
],
"createdAt": "2025-11-22T19:05:31.462Z"
}

Student Information
Field Value
Name Zainab Alasadi
Student ID M01052563
Module CST3144 Full Stack Development (2025–2026)

Deployment Overview
Component Platform
Frontend GitHub Pages
Backend Render.com
Database MongoDB Atlas

Thank you for reviewing my project!

