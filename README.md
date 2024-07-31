# Restaurant Menu Management System

## Overview
This project is a restaurant menu management system that allows you to create and manage menus for different meal times, franchises, and businesses. It includes functionality to calculate bills for purchased items and determine available menus based on the time of day.

## Features
- **Menu Management**: Create and manage menus with items and availability times.
- **Bill Calculation**: Calculate the total bill for a list of purchased items.
- **Franchise Management**: Manage multiple franchises with different menus.
- **Business Management**: Manage businesses that own multiple franchises.

## Classes and Methods

### Menu Class
- **Attributes**:
  - `name`: Name of the menu.
  - `items`: Dictionary of items and their prices.
  - `start_time`: Start time of menu availability.
  - `end_time`: End time of menu availability.
- **Methods**:
  - `__repr__()`: Returns a string representation of the menu.
  - `calculate_bill(purchased_items)`: Calculates the total bill for a list of purchased items.

### Franchise Class
- **Attributes**:
  - `address`: Address of the franchise.
  - `menus`: List of menus available at the franchise.
- **Methods**:
  - `__repr__()`: Returns a string representation of the franchise.
  - `available_menus(time)`: Returns a list of menus available at a given time.

### Business Class
- **Attributes**:
  - `name`: Name of the business.
  - `franchises`: List of franchises owned by the business.
- **Methods**:
  - `__repr__()`: Returns a string representation of the business.

## Example Usage
```python
from datetime import time

# Define menu items
items = {
  'pancakes': 7.50, 'waffles': 9.00, 'burger': 11.00, 'home fries': 4.50, 'coffee': 1.50, 'espresso': 3.00, 'tea': 1.00, 'mimosa': 10.50, 'orange juice': 3.50
}

# Create menus
brunch = Menu('Brunch', items, 11, 16)
early_bird = {
  'salumeria plate': 8.00, 'salad and breadsticks (serves 2, no refills)': 14.00, 'pizza with quattro formaggi': 9.00, 'duck ragu': 17.50, 'mushroom ravioli (vegan)': 13.50, 'coffee': 1.50, 'espresso': 3.00,
}
early_bird_menu = Menu('Early Bird', early_bird, 15, 16)
dinner = {
  'crostini with eggplant caponata': 13.00, 'caesar salad': 16.00, 'pizza with quattro formaggi': 11.00, 'duck ragu': 19.50, 'mushroom ravioli (vegan)': 13.50, 'coffee': 2.00, 'espresso': 3.00,
}
dinner_menu = Menu('Dinner', dinner, 17, 23)
kids = {
  'chicken nuggets': 6.50, 'fusilli with wild mushrooms': 12.00, 'apple juice': 3.00
}
kids_menu = Menu('Kids', kids, 11, 21)

# Create franchises
menus = [brunch, early_bird_menu, dinner_menu, kids_menu]
flagship_store = Franchise('1232 West End Road', menus)
new_installment = Franchise('12 East Mulberry Street', menus)

# Create businesses
basta_fazoolin = Business("Basta Fazoolin' with my Heart", [flagship_store, new_installment])

# Print business information
print(basta_fazoolin)

Requirements
Python 3.x
How to Run
Ensure you have Python 3.x installed.
Place the script in your working directory.
Run the script using the command: python 

License
This project is licensed under the MIT License.

```

