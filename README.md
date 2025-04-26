Ecommerce Database Project
Project Overview
This project involves the design and creation of a relational database for an Ecommerce platform. The database manages brands, products, categories, images, variations (such as size and color), product attributes, and stock management — ensuring a fully scalable product catalog system.

Built using MySQL 8.0 via Command Line Interface.
Technologies Used
Database: MySQL 8.0 Community Edition

Tools: MySQL Command Line Client

OS: Windows 10

 Database Schema
Key Tables:


Table	Purpose
brand	Stores brand information
product_category	Defines product categories
product	Stores main product details
product_image	Stores image URLs for products
color	Stores available color options
size_category	Groups sizes (e.g., footwear, clothing)
size_option	Lists individual size options
product_variation	Links products to specific colors and sizes
product_item	Manages stock units (SKU, quantity, price)
product_attribute	Additional product specifications (e.g., material)
attribute_category	Defines groups for attributes
attribute_type	Defines types of attributes
Entity Relationships
Each brand can have many products.

Each product category can group multiple products.

Each product can have multiple images, variations, items, and attributes.

Each product variation links to a color and a size option.

Each size option belongs to a size category.

Open MySQL Command Line:

mysql -u root -p
Create the database:
CREATE DATABASE ecommerce;
USE ecommerce;
Run the provided SQL commands in sequence to create the tables and insert the initial data.
Verify tables:
SHOW TABLES;
Query sample data:
SELECT p.name, b.brand_name FROM product p JOIN brand b ON p.brand_id = b.brand_id;
ERD (Entity-Relationship Diagram)
(Visual diagram provided separately in project assets folder.)

Note: ERD maps the relationships between entities like product, brand, color, size_option, etc.
Sample Data Inserted
Brand: Nike

Product Category: Clothing

Product: Air Zoom Pegasus (Running Shoe)

Color: Black

Size Category: Footwear Sizes

Size Option: Size 9

SKU Example: NZP-001-BK9

File Structure
/ecommerce-database/
    │
    ├── ecommerce.sql       # All CREATE TABLE and INSERT statements
    ├── README.md            # This file
    └── erd_diagram.png      # ERD visual
