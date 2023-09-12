# -simple-to-do-list-application-that-allows-users-to-add-update-and-delete-tasks.
tasks = []

def add_task(task):
    tasks.append(task)

def remove_task(task):
    tasks.remove(task)

def view_tasks():
    for index, task in enumerate(tasks):
        print(f"{index + 1}. {task}")

while True:
    print("To-Do List Application")
    print("1. Add Task")
    print("2. Remove Task")
    print("3. View Tasks")
    print("4. Exit")
    choice = input("Enter your choice: ")

    if choice == '1':
        task = input("Enter task: ")
        add_task(task)
    elif choice == '2':
        task = input("Enter task to remove: ")
        remove_task(task)
    elif choice == '3':
        view_tasks()
    elif choice == '4':
        break
