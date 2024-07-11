# JoeTech
This is my source code for my E-commerce website project.

# E-commerce Django Application

This e-commerce platform is developed using Django for the backend and HTML, CSS, and JavaScript for the frontend. It offers users the ability to explore various products, filter them based on category, region, and price, add items to their shopping cart, and manage their selections.

## Features

- Display a list of products dynamically populated from the database.
- Provide filters for category, region, and price range.
- Allow users to add products to the cart.
- Display the contents of the cart.
- Show stock availability when a product is added to the cart.
- Secure API endpoints with JWT authentication.


## API Documentation

The API documentation is available via Swagger UI at the following URLs:
https://eccormerce-2.onrender.com/swagger

## Installation

### Create and activate a virtual environment:
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
### Install dependencies:
pip install -r requirements.txt
## Set up the database:
Ensure you have MySQL i
### Run migrations:
python manage.py migrate
Load initial data:

python manage.py loaddata initial_data.json
### Create a superuser:

python manage.py createsuperuser
# Run the development server:

python manage.py runserver
# Access the application:
Open your browser and go to http://127.0.0.1:8000 to see the application in action.

# Usage
## Filters
Use the filter options on the left side of the product list to filter products by category, region, and price range.

## Add to Cart
Click on the "Details" button of a product to view its details and add it to the cart.

## View Cart
Click on the "Cart" tab to view the contents of your cart and manage the quantities of products.

# Project Structure
shop/: Contains the main Django application code.
models.py: Defines the database models.
views.py: Contains the view logic.
serializers.py: Serializers for API endpoints.
urls.py: URL routes for the application.
admin.py: Customizations for the Django admin panel.
templates/shop/: Contains the HTML templates.
static/: Contains the static files (CSS, JS, images).

# API Endpoints
## Categories: /api/categories/
GET: List all categories
## Regions:/api/regions/
GET: List all regions
## Products: /api/products/
GET: List all products
POST: Add a new product (admin only)
## Cart: /api/cart/
GET: List all items in the cart
POST: Add an item to the cart
PUT: Update an item in the cart
DELETE: Remove an item from the cart
# Deployment
To deploy the application on Render with a MySQL database, follow these steps:

## Create a Render account and log in.
## Create a new Web Service:
Connect your GitHub repository to Render.
Select your repository and branch.
## Set up the environment:
In the Render dashboard, go to your Web Service settings.
Add the following environment variables:
DATABASE_URL: The URL of your MySQL database.
SECRET_KEY: Your Django secret key.
DEBUG: Set to False for production.
## Deploy the application:
Render will automatically build and deploy your application.
Once deployed, you can access the application via the URL provided by Render.
