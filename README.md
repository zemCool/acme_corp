# Acme Corp API

This is a test project for Acme Corp, developed to manage products. The project is built using Python with the Django framework and Django REST Framework.

## Installation and Setup

### Step 1: Clone the repository

Clone the repository to your local machine:
```bash
git clone https://github.com/yourusername/acme-corp-api.git
cd acme-corp-api
```

### Step 2: Create and activate a virtual environment
Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # For Windows use `venv\Scripts\activate`
```

### Step 3: Install dependencies
Install the necessary dependencies:

```bash
pip install -r requirements.txt
```

### Step 4: Apply migrations
Apply migrations to set up the database:

```bash
python manage.py makemigrations
python manage.py migrate
```
### Step 5: Create a superuser
Create a superuser to access the Django admin:

```bash
python manage.py createsuperuser
```
### Step 6: Run the development server
Start the development server:

```bash
python manage.py runserver
```
Now the API is accessible at http://127.0.0.1:8000.

## Using the API
### Create a Product
Request:

- URL: http://127.0.0.1:8000/api/products
- Method: POST
Headers:
- Content-Type: application/json
Body (JSON):
```json
{
    "name": "Product1",
    "description": "This is a test product",
    "price": 19.99,
    "category": "Electronics"
}
```
### Get a List of Products
Request:

- URL: http://127.0.0.1:8000/api/products
- Method: GET
### Filter Products by Category
Request:

- URL: http://127.0.0.1:8000/api/products?category=Electronics
- Method: GET
### Sort Products by Price
Request:

- URL: http://127.0.0.1:8000/api/products?sort=price
- Method: GET
### Get Product Details
Request:

- URL: http://127.0.0.1:8000/api/products/1
- Method: GET

## API Documentation
API documentation is available at the following URLs:

- Swagger UI: http://127.0.0.1:8000/swagger/
- Redoc: http://127.0.0.1:8000/redoc/
