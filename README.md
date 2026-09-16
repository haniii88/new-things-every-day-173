function dailyLog173() {
  const tasks = [
    { name: "Build feature", status: "completed" },
    { name: "Fix bugs", status: "completed" },
    { name: "Write tests", status: "pending" },
    { name: "Update documentation", status: "completed" },
    { name: "Review code", status: "pending" }
  ];

  const completed = tasks.filter(task => task.status === "completed").length;
  const pending = tasks.filter(task => task.status === "pending").length;
  const progress = (completed / tasks.length) * 100;

  const repor= {
    date: new Date().toISOString().split("T")[0],
    totalTasks: tasks.length,
    completed,
    pending,
    progress: `${progress.toFixed(1)}%`
  };

  console.log("Daily Project Report:", report);
}

dailyLog173();
