def calculate_discount(price, discount_percent):
  """Calculates the final price of an item after applying a discount.

  Args:
      price: The original price of the item.
      discount_percent: The discount percentage as a number between 0 and 100.

  Returns:
      The final price of the item after applying the discount.
  """
  discount = price * discount_percent / 100
  final_price = price - discount
  if discount_percent >= 20:
    return final_price
  else:
    return price

# Get user input for original price and discount percentage
original_price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage (0-100): "))

# Calculate the final price using the calculate_discount function
final_price = calculate_discount(original_price, discount_percent)

# Print the final price
print(f"The final price after applying the discount is: {final_price:.2f}")
