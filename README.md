# Backend-Task-Mini-Library-Management-API-Django-

# 📚 Mini Library Management API

A RESTful Library Management System built using Django, Django REST Framework, SQLite, and JWT Authentication.
This project allows users to register, log in, and borrow or return books, with admin-only access for book management via Django Admin.

✅ Authentication
✅ Role-based access control
✅ Book CRUD
✅ Borrow & Return workflow
✅ Admin portal

# 🚀 Tech Stack

> Backend: Django, Django REST Framework

> Authentication: JWT (SimpleJWT)

> Database: SQLite

> Admin Panel: Django Admin

# ✨ Features
# 🔐 User Authentication

> User Registration

> User Login using JWT

> Protected API endpoints (authenticated users only)

> API endpoints were tested using PowerShell (curl commands) to validate authentication and protected routes. 

# 📖 Book Management

> CRUD operations on books

> Fields: title, author, isbn, total_copies, available_copies

> Only admin users can create, update, or delete books

# 🔄 Borrow & Return System

> Borrow available books

> Return borrowed books

> Prevents borrowing the same book twice without returning

> View current and past borrow history

# 🗂️ API Endpoints
Authentication
Method	 Endpoint	   Description
POST	/api/register/	Register a new user
POST	/api/login/  	Login and receive JWT tokens

Books
Method	 Endpoint	        Access   	      Description
GET	    /api/books/	      Authenticated	  List all books
POST	  /api/books/	      Admin only	    Create a book
PUT	    /api/books/{id}/	Admin only	    Update a book
DELETE	/api/books/{id}/	Admin only	    Delete a book

Borrow & Return
Method	   Endpoint	                Description
POST	    /api/borrow/{book_id}/	  Borrow a book
POST	    /api/return/{book_id}/	  Return a book
GET	      /api/my-borrows/	        View borrow history

# 🛠️ Setup Instructions

1️⃣ Clone the Repository
git clone https://github.com/your-username/library-management-api.git
cd library-management-api

2️⃣ Create Virtual Environment
python -m virtualenv venv
env\Scripts\activate   # Windows 

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Run Migrations
python manage.py makemigrations
python manage.py migrate

5️⃣ Create Superuser
python manage.py createsuperuser

6️⃣ Start Server
python manage.py runserver

# 🔑 Admin Panel

> URL: http://127.0.0.1:8000/admin/

> Used for managing books and borrow records

# 🔐 Authentication (JWT)

> Include the access token in request headers:

> Authorization: Bearer <access_token>


