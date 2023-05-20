# supermarketbill
A supermarket bill, also known as a grocery receipt, is a document provided to customers after they have made purchases at a supermarket or grocery store. It serves as a record of the items purchased, their corresponding prices, and the total amount due.
# Item prices
item_prices = {
    "apple": 0.75,
    "banana": 0.50,
    "orange": 0.80,
    "bread": 2.50,
    "milk": 1.20,
    "eggs": 2.00,
    "cheese": 3.00,
    "yogurt": 1.50
}

# Shopping cart
shopping_cart = {
    "apple": 3,
    "banana": 2,
    "orange": 4,
    "bread": 1,
    "milk": 2,
    "eggs": 1,
    "cheese": 0,
    "yogurt": 3
}

# Calculate total cost
total_cost = 0
for item in shopping_cart:
    if item in item_prices:
        total_cost += item_prices[item] * shopping_cart[item]

# Print bill
print("Item\t\tQuantity\tPrice")
print("---------------------------------------")
for item in shopping_cart:
    if shopping_cart[item] > 0:
        print(f"{item.capitalize()}\t\t{shopping_cart[item]}\t\t${item_prices[item]:.2f}")
print("---------------------------------------")
print(f"Total cost:\t\t\t\t${total_cost:.2f}")
