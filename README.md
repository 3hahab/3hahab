import random

def show_options():
    print("Please select an option:")
    print("1. Drive forward")
    print("2. Stop")
    print("3. Turn left")
    print("4. Turn right")

def game_loop():
    user_input = ""
    car_position = 0

    while user_input != "2":
        show_options()
        user_input = input("Enter your choice: ")

        if user_input == "1":
            car_position += random.randint(1, 10)
            print(f"The car moves forward and is now at position {car_position}")

        elif user_input == "3":
            turn = random.randint(1, 10)
            if turn <= 5:
                print("The car turned left successfully")
            else:
                print("The car failed to turn left")

        elif user_input == "4":
            turn = random.randint(1, 10)
            if turn <= 5:
                print("The car turned right successfully")
            else:
                print("The car failed to turn right")

        else:
            print("Invalid choice. Please try again.")

game_loop()
