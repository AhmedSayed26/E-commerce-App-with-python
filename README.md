# This repo created by Ahmed Sayed
# Functionality:
This code implements e-commerce application with administrative features. Users can register, log in, and view/manage items in categories. Administrators can further manage categories, add/edit/delete items, and view user carts.

# Key Components:
# File Management:
# USERS_FILE: Stores user data (name, email, password, etc.) in JSON format.
CATEGORIES_FILE: Stores category data (category name and its items) in JSON format.
CARTS_FILE: Stores user cart data (items added by users) in JSON format.
# User Management:
is_admin(email, password): Checks if a user is an admin.
load_users(): Loads user data from USERS_FILE.
save_users(users): Saves user data to USERS_FILE.
is_valid_email(email): Validates email format.
login(): Handles user login and redirects to the appropriate panel (admin or user).
register(): Handles user registration and creates a new user entry in USERS_FILE.
# Category Management:
Category class: Represents a category with methods for adding/editing/deleting categories and displaying them.
load_categories(): Loads category data from CATEGORIES_FILE.
save_categories(): Saves category data to CATEGORIES_FILE.
add_category(category_name, user_email): Adds a new category if the user is an admin.
edit_category(old_category_name, new_category_name, admin_email): Edits an existing category if the user is an admin.
delete_category(category_name, admin_email): Deletes a category if the user is an admin.
show_categories(): Displays all categories in a separate window.
# Item Management:
Item class: Represents an item with properties like name, price, brand, model year, and discount.
add_item_to_category(category_name, admin_email): Adds an item to a category if the user is an admin.
delete_item_from_category(category_name, item_name, admin_email): Deletes an item from a category if the user is an admin.
edit_item(category_name, old_item_name, new_name, new_price, new_brand, new_year, new_discount, admin_email): Edits an item's details if the user is an admin.
search(category_name, item_name): Searches for items by name within a category.
# Cart Management:
Cart class: Represents a user's cart with methods for adding/deleting items, displaying items in the cart, and calculating the total cost.
__init__(self, user_email): Initializes an instance for a specific user's cart.
load_items(): Loads cart data (items) for the user from CARTS_FILE.
save_items(): Saves cart data (items) for the user to CARTS_FILE.
add_item_to_cart(self, item): Adds an item to the user's cart.
delete_item_from_cart(self, item_name, cart_window): Deletes an item from the user's cart and updates the cart window.
display(self, cart_window): Displays the user's cart items in a separate window.
view_cart(): Opens the cart window for a user, allowing them to view, search, delete, and calculate the total cost.
search(self, item_name): Searches for items in the user's cart.
calculate_total(self, governorate): Calculates the total cost of items in the cart, including a delivery fee based on the governorate (administrative division).
GUI (Graphical User Interface):
The code utilizes the tkinter library for creating the user interface elements like windows, buttons, labels, and entry fields.
Functions like login(), register(), admin_panel(), etc., manage the creation and display of different windows and interact with the user's actions.
# Installation:
# Clone the repository:
Bash
git clone https://github.com/AhmedSayed26/E-commerce-App-with-python.git
