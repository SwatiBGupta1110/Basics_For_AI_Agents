# 🐍 Pydantic Crash Course – Simple Guide

Welcome! This is a simple crash course on **Pydantic**, a Python library that helps you validate and manage data easily using Python type hints.

Pydantic is very useful when working with APIs, user inputs, or any structured data. It saves time and reduces errors by checking data types for you.

---

## ✅ What is Pydantic?

Pydantic lets you define **data models** using Python classes. It automatically checks if the data you receive matches the types you expect. If something's wrong, it tells you with clear error messages.

---

# Pydantic Example: Simple User Model

## Installation

To get started, install Pydantic using pip:

"""pip install pydantic"""


## ✍️ Example Code

"""
from pydantic import BaseModel
from typing import Optional

class User(BaseModel):
    id: int
    name: str
    email: Optional[str] = None

# Creating an instance of the model
user = User(id=1, name="Alice", email="alice@example.com")

print(user.id)      # Output: 1
print(user.name)    # Output: Alice
print(user.email)   # Output: alice@example.com
"""


## 🔍 What’s Happening in the Code?

- **`BaseModel`**: This is the main class from Pydantic that we use to define our data model.

- **`id`**, **`name`**, **`email`**: These are the fields we expect. Each one has a type. For example:
  - `id` must be an **`int`**
  - `name` must be a **`str`**
  - `email` is **optional** – it can be a string or left out

- If you pass wrong data (like a string for `id`), Pydantic will raise an error and let you know something is wrong.


---







