def calculator():
    print("Welcome to the Basic Calculator!")
    print("Choose an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    while True:
        try:
            # Taking user input for the operation
            choice = input("\nEnter the number corresponding to the operation (1/2/3/4) or 'q' to quit: ").strip()
            if choice.lower() == 'q':
                print("Exiting the calculator. Goodbye!")
                break

            if choice not in ('1', '2', '3', '4'):
                print("Invalid choice. Please select a valid operation.")
                continue

            # Taking input for the numbers
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))

            # Performing the operation
            if choice == '1':
                result = num1 + num2
                operation = "+"
            elif choice == '2':
                result = num1 - num2
                operation = "-"
            elif choice == '3':
                result = num1 * num2
                operation = "*"
            elif choice == '4':
                if num2 == 0:
                    print("Error: Division by zero is not allowed.")
                    continue
                result = num1 / num2
                operation = "/"

            print(f"Result: {num1} {operation} {num2} = {result}")

        except ValueError:
            print("Invalid input. Please enter numeric values.")

# Run the calculator
calculator()
