# CS 101 Wk 6 Python Notes
Starting with Lesson 10 (because I just discovered GitHub!!)

### reusable functions
example discount calculator:

```python
def apply_discount(price, discount_percent):
    discount_amount = price * (discount_percent / 100)
    final_price = price - discount_amount
    return final_price

# Use the function
item_price = 50
discount = 20

new_price = apply_discount(item_price, discount)
print("Final price after discount:", new_price)
```
### example code with notes explaining why 
```python
def apply_discount(price, discount_percent):
    discount_amount = price * (discount_percent / 100)
    final_price = price - discount_amount
    return final_price  # pure calculation

def show_final_price(label, final_price):
    print(label, final_price)

item_price_1 = 80
discount_1 = 10

item_price_2 = 120
discount_2 = 25

# Data flow for the next line:
# - item_price_1 and discount_1 are arguments (80 and 10).
# - Inside the function, they become parameters price and discount_percent.
# - The function does local work and returns a number (72.0).
# - That returned value is stored in the variable final_price_1.
# - Later, show_final_price("Item 1 final price:", final_price_1) uses that stored value.
# - show_final_price doesn’t “pull” the calculation; it just receives the already computed final_price_1.
final_price_1 = apply_discount(item_price_1, discount_1)

final_price_2 = apply_discount(item_price_2, discount_2)

show_final_price("Item 1 final price:", final_price_1)
show_final_price("Item 2 final price:", final_price_2)
```

#Lesson 11-Debugging step by step
