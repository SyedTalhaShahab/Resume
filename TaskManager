class TaskManager {
    private val tasks = mutableListOf<Task>()
    private var nextId = 1

    fun addTask(description: String) {
        tasks.add(Task(nextId++, description))
    }

    fun completeTask(id: Int) {
        tasks.find { it.id == id }?.let {
            it.isCompleted = true
        }
    }

    fun deleteTask(id: Int) {
        tasks.removeIf { it.id == id }
    }

    fun getAllTasks(): List<Task> {
        return tasks.toList()
    }
}
