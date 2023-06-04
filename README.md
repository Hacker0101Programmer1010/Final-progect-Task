# Final-progect-Task
    class TaskManager
    {
        private static ArrayList tasks = new ArrayList();

        public static void AddTask(Task task)
        {
            tasks.Add(task);
            Console.WriteLine("Task added successfully!");
        }

        public static void DeleteTask(Task task)
        {
            if (tasks.Contains(task))
            {
                tasks.Remove(task);
                Console.WriteLine("Task deleted successfully!");
            }
            else
            {
                Console.WriteLine("Task not found!");
            }
        }

        public static void SearchForTask(Task task)
        {
            int index = tasks.IndexOf(task);
            if (index != -1)
            {
                Console.WriteLine("Task found at index: " + index);
            }
            else
            {
                Console.WriteLine("Task not found!");
            }
        }
    }
     public class Task
    {
        public string name;

        public void PrintTask()
        {
            Console.WriteLine("Task Name: " + name);
        }
    }
     class Program
    {
        static void Main(string[] args)
        {
            Task task1 = new Task();
            task1.name = "going to the gym ";//الذهاب الى الصالة الرياضية 
            task1.PrintTask();

            Task task2 = new Task();
            task2.name = "Having breakfast ";//تناول وجبة الافطار
            task2.PrintTask();

            Task task3 = new Task();
            task3.name = "Brushing teeth and taking a shower ";//تنظيف الاسنان والاستحمام
            task3.PrintTask();

            Task task4 = new Task();
            task4.name = "Reading news";//قراءة الاخبار
            task4.PrintTask();

            // Adding tasks to the manager
            TaskManager.AddTask(task1);
            TaskManager.SearchForTask(task1);


            TaskManager.AddTask(task2);
            TaskManager.SearchForTask(task2);


            TaskManager.AddTask(task3);
            TaskManager.SearchForTask(task3);


            TaskManager.AddTask(task4);
            TaskManager.SearchForTask(task4);

            // Deleting a task from the manager
            TaskManager.DeleteTask(task2);

            // Deleting a task in the manager
            TaskManager.DeleteTask(task4);

        }
    
}
    
