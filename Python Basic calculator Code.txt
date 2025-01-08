def calculator():
    print("Welcome to the Basic Calculator!")
    print("Select an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    # Get user input for the operation
    choice = input("Enter your choice (1/2/3/4): ")

    # Ensure the choice is valid
    if choice not in ['1', '2', '3', '4']:
        print("Invalid choice. Please try again.")
        return calculator()

    # Get user input for the numbers
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
    except ValueError:
        print("Invalid input. Please enter numbers only.")
        return calculator()

    # Perform the chosen operation
    if choice == '1':
        print(f"The result of {num1} + {num2} is {num1 + num2}")
    elif choice == '2':
        print(f"The result of {num1} - {num2} is {num1 - num2}")
    elif choice == '3':
        print(f"The result of {num1} * {num2} is {num1 * num2}")
    elif choice == '4':
        if num2 != 0:
            print(f"The result of {num1} / {num2} is {num1 / num2}")
        else:
            print("Error: Division by zero is not allowed.")

    # Ask the user if they want to calculate again
    again = input("Would you like to perform another calculation? (yes/no): ").lower()
    if again == 'yes':
        calculator()
    else:
        print("Thank you for using the calculator. Goodbye!")

# Run the calculator
calculator()
