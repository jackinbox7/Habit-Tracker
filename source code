#  Habit Tracker
# A friendly little program to help you keep track of daily habits.

import datetime

# Let's start by greeting the user
print(" Hey there! Welcome to your Habit Tracker.")
print("This is your safe space to build good habits, one day at a time.\n")

# We'll store habits in a simple list
habits = []

def show_menu():
    print("\n What would you like to do today?")
    print("1. Add a new habit")
    print("2. Mark a habit as done")
    print("3. Show all habits")
    print("4. Exit")

def add_habit():
    habit = input(" Enter the habit you want to build: ")
    habits.append({"name": habit, "done": False, "date": None})
    print(f" Great choice! '{habit}' has been added to your list.")

def mark_done():
    if not habits:
        print(" Oops, you don’t have any habits yet. Add one first!")
        return
    print("\nHere are your habits:")
    for i, habit in enumerate(habits, start=1):
        status = " Done" if habit["done"] else " Not yet"
        print(f"{i}. {habit['name']} - {status}")
    choice = int(input("Which habit did you complete today? Enter the number: "
    if 1 <= choice <= len(habits):
        habits[choice-1]["done"] = True
        habits[choice-1]["date"] = datetime.date.today()
        print(f" Awesome! You completed '{habits[choice-1]['name']}' today.")
    else:
        print(" That number doesn’t match any habit.")

def show_habits():
    if not habits:
        print("Your habit list is empty. Add something inspiring!")
        return
    print("\n Here’s your current habit list:")
    for habit in habits:
        status = " Done" if habit["done"] else " Not yet"
        date_info = f" (last done on {habit['date']})" if habit["date"] else ""
        print(f"- {habit['name']} : {status}{date_info}")

# Main loop
while True:
    show_menu()
    choice = input(" Enter your choice (1-4): ")
    if choice == "1":
        add_habit()
    elif choice == "2":
        mark_done()
    elif choice == "3":
        show_habits()
    elif choice == "4":
        print(" Goodbye! Keep shining and building those habits.")
        break
    else:
        print("f Hmm, that’s not a valid option. Try again!")
