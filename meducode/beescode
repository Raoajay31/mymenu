# Restaurant Menu System

menu = {
    "Burger": 5.99,
    "Pizza": 8.99,
    "Pasta": 7.49,
    "Salad": 4.99,
    "Coffee": 2.99
}

order = {}

def show_menu():
    print("\n----- MENU -----")
    for item, price in menu.items():
        print(f"{item}: ${price:.2f}")

def take_order():
    while True:
        item = input("\nEnter the item to order (or 'done' to finish): ").title()
        if item.lower() == 'done':
            break
        if item in menu:
            qty = int(input(f"How many {item}s would you like? "))
            if item in order:
                order[item] += qty
            else:
                order[item] = qty
            print(f"Added {qty} x {item} to your order.")
        else:
            print("Sorry, that item is not on the menu.")

def show_bill():
    print("\n----- BILL -----")
    total = 0
    for item, qty in order.items():
        price = menu[item] * qty
        print(f"{item} x {qty} = ${price:.2f}")
        total += price
    print(f"Total: ${total:.2f}")
    print("Thank you for dining with us!")

# Run the program
print("🍽️ Welcome to Python Bistro!")
show_menu()
take_order()
show_bill()
