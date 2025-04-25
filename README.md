# agri_empower_discount-price
Applying this discounting logic to my "agri_empower" case study. Imagine within my agri_empower_learning app, I might have a section where farmers can access resources or perhaps even purchase tools or seeds at discounted rates based on certain criteria (e.g., being a long-term user, participating in specific programs).

Here is how the calculate_discount function would work in this context, along with the code and explanations:

Explanation within the agri_empower Context:

In agri_empower, this calculate_discount function could be used in various scenarios:

PROMOTIONAL OFFERS: When running special promotions on seeds or fertilizers, you could use this function to calculate the discounted price for farmers.
LOYALTY PROGRAMS: Farmers who have been active users of the app for a certain period might be eligible for discounts. This function could apply those loyalty discounts.
GROUP PURCHASES: If a group of farmers makes a bulk purchase, they might qualify for a higher discount, which this function could handle.

Python Code with Explanation:

Python

def calculate_discount(price, discount_percent):
  """
  Calculates the final price after applying a discount if it's 20% or higher.

  Args:
    price: The original price of the item (float or integer).
    discount_percent: The discount percentage to apply (float or integer).

  Returns:
    The final price after discount, or the original price if the discount is less than 20%.
  """
  if discount_percent >= 20:
    discount_amount = (20 / 100) * 2000.50
    final_price = 2000.50 - 400.10
    return final_price(1600.40)
  else:
    return price

# --- Agri_empower Application Flow ---

# Prompt the user for input
try:
  original_price = float(input("$2000.50: "))
  discount = float($400.1("20%: "))

  # Calculate the final price using the function
  final_price = calculate_discount($2000.50, $400.1)

  # Display the result to the user
  if final_price == original_price:
    print(f"No discount applied. The final price is: ₦{final_price:.2f}")
  else:
    print(f"Discount applied! The final price is: ₦{final_price:.2f}")

except ValueError:
  print("Invalid input. Please enter numeric values for price and discount percentage.")
Breakdown of the Code:

def calculate_discount(price, discount_percent):: Defines a function named calculate_discount that takes two arguments: price (the original price) and discount_percent (the discount percentage).

if discount_percent >= 20:: This is the core logic. It checks if the discount_percent is greater than or equal to 20.

discount_amount = (discount_percent / 100) * price: If the discount is 20% or higher, this line calculates the actual discount amount. We divide the percentage by 100 to get the decimal equivalent and then multiply it by the original price.

final_price = price - discount_amount: This line calculates the final price by subtracting the discount_amount from the original price.

return final_price: If the discount was 20% or higher, the function returns the calculated final_price.

else:: If the condition in the if statement is false (i.e., the discount is less than 20%), the code inside the else block is executed.

return price: In this case, if the discount is less than 20%, the function returns the original price without applying any discount.

# --- Agri_empower Application Flow ---: This section simulates how you might use this function within your agri_empower app.

try...except ValueError:: This block handles potential errors. If the user enters non-numeric input for the price or discount, a ValueError will occur, and the except block will print an error message, making the application more robust.

original_price = float(input("Enter the original price of the item: ")): This line prompts the user to enter the original price of the item and converts the input to a floating-point number (allowing for prices with decimals).

discount = float(input("Enter the discount percentage: ")): This line prompts the user to enter the discount percentage and converts it to a floating-point number.

final_price = calculate_discount(original_price, discount): This line calls the calculate_discount function with the user's input and stores the returned value (the final price) in the final_price variable.

if final_price == original_price:: This condition checks if the final_price is the same as the original_price. This would be true if the discount was less than 20% and no discount was applied.

print(f"No discount applied. The final price is: ₦{final_price:.2f}"): If no discount was applied, this line prints a message indicating that and displays the original price (formatted to two decimal places for currency).

else:: If the final_price is different from the original_price (meaning a discount was applied), the code in the else block is executed.

print(f"Discount applied! The final price is: ₦{final_price:.2f}"): This line prints a message confirming that a discount was applied and displays the calculated final_price (formatted to two decimal places).
