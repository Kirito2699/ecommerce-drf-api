🛒 E-commerce Product API (Django REST Framework)
📌 Overview

This project is a production-ready REST API for managing products, built using Django REST Framework.
It includes authentication, CRUD operations, filtering, pagination, and is deployed on the cloud.

🚀 Live API

Base URL:

https://ecommerce-drf-api-q7vo.onrender.com/
🧰 Tech Stack
Backend: Django REST Framework
Language: Python
Authentication: JWT (SimpleJWT)
Database: SQLite (current setup)
Deployment: Render
Version Control: Git & GitHub
⚙️ Features
🔐 Authentication (JWT)
Token-based authentication
Login endpoint:
POST /api/token/
Returns:
Access Token
Refresh Token
Use token in headers:
Authorization: Bearer <access_token>
📦 Product API (CRUD)
Method	Endpoint	Description
GET	/products/	Get all products
POST	/products/	Create product
GET	/products/{id}/	Get single product
PUT	/products/{id}/	Update product
DELETE	/products/{id}/	Delete product
📄 Pagination

Response format:

{
  "count": 2,
  "next": null,
  "previous": null,
  "results": [...]
}
🔎 Filtering, Search, Ordering

Examples:

/products/?name=Laptop
/products/?search=iphone
/products/?ordering=price
🧪 API Usage
1. Get Token
POST /api/token/

Body:

{
  "username": "admin",
  "password": "admin123"
}
2. Access Protected Routes
GET /products/
Authorization: Bearer <your_token>
3. Create Product
POST /products/

Body:

{
  "name": "iPhone 17",
  "price": 80000,
  "description": "Latest Apple smartphone"
}
🛠️ Installation (Local Setup)
1. Clone Repository
git clone https://github.com/Kirito2699/ecommerce-drf-api.git
cd ecommerce-drf-api
2. Create Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows
3. Install Dependencies
pip install -r requirements.txt
4. Run Migrations
python manage.py migrate
5. Create Superuser
python manage.py createsuperuser
6. Run Server
python manage.py runserver
🌐 Deployment (Render)
Build Command:
pip install -r requirements.txt
Start Command:
python manage.py migrate && gunicorn ecommerce_drf.wsgi
⚠️ Known Limitations
Uses SQLite in production (data may reset)
No user registration endpoint yet
Basic authentication setup
🚀 Future Improvements
PostgreSQL database integration
User registration API
Role-based permissions (Admin/User)
API documentation (Swagger/OpenAPI)
Frontend integration (React)
👨‍💻 Author

Siddharth S

GitHub: https://github.com/Kirito2699

📄 License

This project is for learning and portfolio purposes.