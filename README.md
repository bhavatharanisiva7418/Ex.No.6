# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

## Date:02.09.2026 
## Name : BHAVATHARANI S
## Register No: 212223230032

---

## Aim
To write and implement Python code that integrates with multiple AI tools to automate tasks such as interacting with APIs, comparing outputs, and generating actionable insights using multiple AI tools.

---

## AI Tools Required
- ChatGPT
- Google Gemini
- Claude AI
- Python
- VS Code / Jupyter Notebook

---

## Explanation

In this experiment, the persona pattern was used by assigning the AI the role of a Python programmer. The selected application was a **Student Productivity Assistant** that helps students manage tasks, track completion status, and generate summaries.

The same prompt was tested across multiple AI tools to compare:
- Code generation capability
- Readability
- Logic implementation
- Error handling
- Output quality

The generated Python code automates task management operations such as:
- Adding tasks
- Viewing tasks
- Marking tasks as completed
- Displaying task summaries

---

## Prompt Used

```python
Act as a Python programmer and develop a simple student productivity assistant application using Python.

The application should:
1. Accept task input from the user
2. Store tasks
3. Display pending tasks
4. Mark completed tasks
5. Generate a summary report

Use clean, beginner-friendly, and well-structured Python code.
```

---

## Python Code

```python
# Student Productivity Assistant

tasks = []

# Function to add task
def add_task():
    task = input("Enter task name: ")

    task_data = {
        "task": task,
        "completed": False
    }

    tasks.append(task_data)

    print("Task added successfully!")

# Function to view tasks
def view_tasks():

    if len(tasks) == 0:
        print("No tasks available.")
        return

    print("\nTask List:")

    for index, task in enumerate(tasks):

        status = "Completed" if task["completed"] else "Pending"

        print(f"{index + 1}. {task['task']} - {status}")

# Function to mark task as completed
def complete_task():

    view_tasks()

    try:
        number = int(input("Enter task number to mark completed: "))

        if number >= 1 and number <= len(tasks):

            tasks[number - 1]["completed"] = True

            print("Task marked as completed!")

        else:
            print("Invalid task number.")

    except:
        print("Please enter a valid number.")

# Function to display summary
def task_summary():

    total = len(tasks)

    completed = 0

    for task in tasks:

        if task["completed"]:
            completed += 1

    pending = total - completed

    print("\n===== TASK SUMMARY =====")
    print("Total Tasks     :", total)
    print("Completed Tasks :", completed)
    print("Pending Tasks   :", pending)

# Main program loop
while True:

    print("\n===== STUDENT PRODUCTIVITY ASSISTANT =====")

    print("1. Add Task")
    print("2. View Tasks")
    print("3. Complete Task")
    print("4. Task Summary")
    print("5. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        add_task()

    elif choice == "2":
        view_tasks()

    elif choice == "3":
        complete_task()

    elif choice == "4":
        task_summary()

    elif choice == "5":
        print("Exiting Application...")
        break

    else:
        print("Invalid choice. Please try again.")
```

---

## Output

### Sample Execution – Test Scenario 1

```text
===== STUDENT PRODUCTIVITY ASSISTANT =====

1. Add Task
2. View Tasks
3. Complete Task
4. Task Summary
5. Exit

Enter your choice: 1

Enter task name: Complete AI Record

Task added successfully!
```

---

### Sample Execution – Test Scenario 2

```text
===== STUDENT PRODUCTIVITY ASSISTANT =====

1. Add Task
2. View Tasks
3. Complete Task
4. Task Summary
5. Exit

Enter your choice: 1

Enter task name: Study Computer Networks

Task added successfully!
```

---

### Sample Execution – Viewing Tasks

```text
Task List:

1. Complete AI Record - Pending
2. Study Computer Networks - Pending
```

---

### Sample Execution – Marking Completed Task

```text
Enter task number to mark completed: 1

Task marked as completed!
```

---

### Sample Execution – Task Summary

```text
===== TASK SUMMARY =====

Total Tasks     : 2
Completed Tasks : 1
Pending Tasks   : 1
```

---

### Comparison of AI Tool Outputs

| Feature | ChatGPT | Gemini | Claude AI |
|---|---|---|---|
| Code Readability | Excellent | Good | Excellent |
| Beginner Friendliness | High | Medium | High |
| Error Handling | Included | Partial | Included |
| Code Structure | Well Organized | Moderate | Well Organized |
| Output Clarity | High | Medium | High |
| Practical Usability | High | Medium | High |

---

### Analysis

- ChatGPT generated beginner-friendly and highly structured code.
- Gemini produced working code with moderate readability.
- Claude AI generated clean and well-commented code.
- Structured prompts resulted in more accurate and usable outputs across all AI tools.
- Error handling and proper function separation improved the overall quality of the application.

---




## Result

The corresponding prompt was executed successfully, and Python code compatible with multiple AI tools was generated, tested, and analyzed successfully.
