# ☕ Coffee Shop Domain Modeling

A simple object-oriented Python application that models the domain of a Coffee Shop using classes, relationships, and data management best practices.

## 📚 Overview

This project simulates a coffee shop's core functionality through three main entities:
- **Customer**: A person who places orders.
- **Coffee**: A drink that can be ordered.
- **Order**: A record linking a customer to a coffee and its price.

### Relationships:
- A `Customer` can have many `Orders`.
- A `Coffee` can be ordered many times.
- An `Order` belongs to one `Customer` and one `Coffee`.

> This results in a **many-to-many** relationship between `Customer` and `Coffee` via `Order`.

---

## 🛠️ Technologies Used

- Python 3.x
- Pipenv (for dependency and virtual environment management)
- Pytest (for optional testing)

---

## 📁 Folder Structure

coffee_shop/
│
├── customer.py # Defines Customer class and methods
├── coffee.py # Defines Coffee class and methods
├── order.py # Defines Order class and methods
├── Pipfile # Pipenv environment dependencies
├── Pipfile.lock # Lock file for exact versions
├── README.md # This file


## 🚀 Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/coffee_shop.git
   cd coffee_shop
Install pipenv and dependencies
pip install pipenv
pipenv install
pipenv shell
pipenv install pytest
pytest

🔍 Features
✅ Class Validations
Customer

Name must be a string between 1 and 15 characters.

Coffee

Name must be a string with at least 3 characters.

Order

Price must be a float between 1.0 and 10.0.

✅ Object Relationships
Customer.orders(): Get all orders by the customer.

Customer.coffees(): Get unique coffees ordered by the customer.

Coffee.orders(): Get all orders for a coffee.

Coffee.customers(): Get unique customers who ordered that coffee.

✅ Data Aggregation
Customer.create_order(coffee, price): Create a new order.

Coffee.num_orders(): Total number of orders for the coffee.

Coffee.average_price(): Average price paid for the coffee.

Customer.most_aficionado(coffee): Returns the customer who spent the most on that coffee.

