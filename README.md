# python-week-3-assign
def calculate_discount(price, discount_percent):
    """Calculates the final price after applying a discount."""
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Get user input
try:
    price = float(input("Enter the original price: "))
    discount_percent = float(input("Enter the discount percentage: "))

    # Calculate and print the final price
    final_price = calculate_discount(price, discount_percent)
    print(f"The final price is: {final_price:.2f}")

except ValueError:
    print("Invalid input. Please enter numeric values for price and discount.")
