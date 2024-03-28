class Task:
    def __init__(self, description, priority):
        self.description = description
        self.priority = priority
        self.status = "Pending"

class TaskManager:
    def __init__(self):
        self.tasks = []

    def add_task(self, description, priority):
        task = Task(description, priority)
        self.tasks.append(task)

    def remove_task(self, description):
        for task in self.tasks:
            if task.description == description:
                self.tasks.remove(task)

    def list_tasks(self):
        for index, task in enumerate(self.tasks, start=1):
            print(f"{index}. Description: {task.description}, Priority: {task.priority}, Status: {task.status}")

    def prioritize_tasks(self):
        self.tasks = sorted(self.tasks, key=lambda x: x.priority, reverse=True)

    def recommend_task(self, keyword):
        recommended_tasks = [task for task in self.tasks if keyword.lower() in task.description.lower()]
        if recommended_tasks:
            print("Recommended Tasks:")
            for task in recommended_tasks:
                print(f"Description: {task.description}, Priority: {task.priority}")
        else:
            print("No tasks match the description.")

# Sample Usage
task_manager = TaskManager()
task_manager.add_task("Complete project proposal", 2)
task_manager.add_task("Prepare presentation slides", 1)
task_manager.add_task("Review project budget", 3)

task_manager.list_tasks()

task_manager.prioritize_tasks()
print("Tasks after prioritization:")
task_manager.list_tasks()

task_manager.recommend_task("project")
