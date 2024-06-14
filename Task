fun main() {
    val taskManager = TaskManager()
    val scanner = Scanner(System.`in`)

    while (true) {
        println("Task Manager Menu:")
        println("1. Add Task")
        println("2. Complete Task")
        println("3. Delete Task")
        println("4. View All Tasks")
        println("5. Exit")

        print("Enter your choice: ")
        when (scanner.nextInt()) {
            1 -> {
                print("Enter task description: ")
                val description = scanner.next()
                taskManager.addTask(description)
                println("Task added.")
            }
            2 -> {
                print("Enter task ID to mark as completed: ")
                val id = scanner.nextInt()
                taskManager.completeTask(id)
                println("Task marked as completed.")
            }
            3 -> {
                print("Enter task ID to delete: ")
                val id = scanner.nextInt()
                taskManager.deleteTask(id)
                println("Task deleted.")
            }
            4 -> {
                val allTasks = taskManager.getAllTasks()
                if (allTasks.isEmpty()) {
                    println("No tasks found.")
                } else {
                    println("All Tasks:")
                    allTasks.forEach { task ->
                        println("${task.id}: ${task.description} - ${if (task.isCompleted) "Completed" else "Pending"}")
                    }
                }
            }
            5 -> {
                println("Exiting Task Manager.")
                return
            }
            else -> {
                println("Invalid choice. Please enter a number between 1 and 5.")
            }
        }
        println()
    }
}
