# Java Queue Application

## Project Description
This Java console application implements an in-memory queue to manage "Task" objects. Users can:
- Add a Task (enqueue a new task)
- List Tasks (display all tasks currently in the queue)
- Remove a Task (dequeue the first task from the queue)
- Exit the application

This project demonstrates how to use Java collections to implement a queue and provides hands-on experience with command-line interaction and version control using GitHub.

## Project Structure
```
java-queue-application/
│── src/
│   ├── model/
│   │   ├── Task.java
│   ├── service/
│   │   ├── TaskQueueService.java
│   ├── app/
│   │   ├── QueueApp.java
│── README.md
│── .gitignore
```

### Packages
- **model** – Contains the `Task` class representing a task with an ID and description.
- **service** – Contains `TaskQueueService`, which manages the in-memory queue operations.
- **app** – Contains `QueueApp`, which provides a menu-based command-line interface.

## Compilation & Execution
Ensure that Java is installed on the system.
### Compilation
Run the following command to compile the application:
```sh
javac -d bin src/model/Task.java src/service/TaskQueueService.java src/app/QueueApp.java 
```

### Running the Application
After compiling, execute the application using:
```sh
java -cp bin app.QueueApp
```

## Design Choices
- **Queue Implementation**: Used `LinkedList<Task>` to implement the queue since it provides efficient enqueue and dequeue operations.
- **Command-Line Interface**: A simple loop-driven menu to interact with the application.
- **Encapsulation**: The `TaskQueueService` class handles all queue operations to separate concerns from the main application logic.

## Assumptions
- Task IDs are manually entered by users.
- Users are responsible for providing unique IDs.
- The application runs in a single session and does not persist data after termination.

## Extra Features Implemented
- Basic input validation to handle invalid user inputs.
- A toString() method in the Task class to ensure a readable output format.
- Uses Scanner to manage user input in a loop until the exit option is selected.

## GitHub Workflow
### Basic Git Commands
```sh
git init  # Initialize a repository
git add .  # Stage changes
git commit -m "Initial commit"  # Commit changes
git push origin main  # Push changes to GitHub
```

---

This project serves as a practical implementation of queue data structures, Java collections, and command-line interaction while reinforcing good GitHub practices.

