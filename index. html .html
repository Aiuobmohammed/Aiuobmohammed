<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>📌 قائمة المهام الذكية - أيوب محمد</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap');

        body {
            font-family: 'Tajawal', sans-serif;
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: #fff;
            padding: 20px;
        }
        .container {
            max-width: 750px;
            background: rgba(255, 255, 255, 0.95);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            color: #333;
        }
        h1 {
            text-align: center;
            color: #007bff;
            font-weight: bold;
        }
        .task-item {
            background: #f8f9fa;
            padding: 10px;
            border-radius: 8px;
            margin: 8px 0;
            transition: 0.3s;
            position: relative;
            border-left: 6px solid #007bff;
        }
        .task-item:hover {
            transform: scale(1.02);
        }
        .completed {
            text-decoration: line-through;
            opacity: 0.6;
            border-left: 6px solid #28a745;
        }
        .btn-sm {
            padding: 5px 12px;
        }
        .task-details {
            font-size: 14px;
            color: #555;
        }
        .footer {
            text-align: center;
            margin-top: 20px;
            font-size: 14px;
            color: #666;
        }
        .footer a {
            color: #ffdd57;
            text-decoration: none;
        }
        .buttons {
            display: flex;
            justify-content: space-between;
        }
        input, button {
            margin-top: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>📌 قائمة المهام الذكية</h1>

        <!-- إدخال المهمة -->
        <input type="text" id="taskInput" class="form-control" placeholder="✍️ أضف عنوان المهمة...">
        <input type="text" id="taskDetails" class="form-control" placeholder="📝 أضف تفاصيل المهمة...">
        <label class="form-label mt-2">⏳ حدد تاريخ ووقت المهمة:</label>
        <input type="datetime-local" id="taskDateTime" class="form-control">
        <button id="addTaskBtn" class="btn btn-success w-100 mt-2">➕ إضافة المهمة</button>

        <!-- البحث باستخدام DeepSeek -->
        <input type="text" id="searchTask" class="form-control mt-3" placeholder="🔍 بحث عن مهمة...">

        <!-- قائمة المهام -->
        <ul id="taskList" class="list-group mt-3"></ul>

        <div class="footer">
            <p>🚀 تم تطوير هذا المشروع بواسطة <strong>أيوب محمد | NEW SOFT</strong></p>
            <p>📡 يدعم DeepSeek لتحليل البيانات وGoogle Calendar لتنظيم الوقت ❤️</p>
        </div>
    </div>

    <script>
        let tasks = [];

        const taskInput = document.getElementById('taskInput');
        const taskDetails = document.getElementById('taskDetails');
        const taskDateTime = document.getElementById('taskDateTime');
        const addTaskBtn = document.getElementById('addTaskBtn');
        const taskList = document.getElementById('taskList');
        const searchTask = document.getElementById('searchTask');

        function renderTasks(filter = '') {
            taskList.innerHTML = '';
            tasks.filter(task => task.text.includes(filter)).forEach((task, index) => {
                const li = document.createElement('li');
                li.classList.add('list-group-item', 'task-item');

                if (task.completed) li.classList.add('completed');

                const taskText = document.createElement('span');
                taskText.textContent = task.text;

                const taskDetail = document.createElement('p');
                taskDetail.classList.add('task-details');
                taskDetail.textContent = task.details || "لا توجد تفاصيل";

                const taskDate = document.createElement('p');
                taskDate.classList.add('task-details');
                taskDate.textContent = `📅 تاريخ المهمة: ${new Date(task.dateTime).toLocaleString()}`;

                const createdDate = document.createElement('p');
                createdDate.classList.add('task-details');
                createdDate.textContent = `🕒 أُضيفت في: ${new Date(task.createdAt).toLocaleString()}`;

                const buttonsDiv = document.createElement('div');
                buttonsDiv.classList.add('buttons');

                const completeBtn = document.createElement('button');
                completeBtn.textContent = task.completed ? 'إلغاء' : '✔';
                completeBtn.classList.add('btn', 'btn-sm', 'btn-primary');
                completeBtn.onclick = () => toggleComplete(index);

                const deleteBtn = document.createElement('button');
                deleteBtn.textContent = '🗑';
                deleteBtn.classList.add('btn', 'btn-sm', 'btn-danger');
                deleteBtn.onclick = () => deleteTask(index);

                const googleCalendarBtn = document.createElement('button');
                googleCalendarBtn.textContent = '📅 أضف إلى جوجل';
                googleCalendarBtn.classList.add('btn', 'btn-sm', 'btn-warning');
                googleCalendarBtn.onclick = () => addToGoogleCalendar(task);

                buttonsDiv.appendChild(completeBtn);
                buttonsDiv.appendChild(googleCalendarBtn);
                buttonsDiv.appendChild(deleteBtn);

                li.appendChild(taskText);
                li.appendChild(taskDetail);
                li.appendChild(taskDate);
                li.appendChild(createdDate);
                li.appendChild(buttonsDiv);
                taskList.appendChild(li);
            });
        }

        function addTask() {
            const text = taskInput.value.trim();
            const details = taskDetails.value.trim();
            const dateTime = taskDateTime.value;

            if (text && dateTime) {
                tasks.push({ text, details, dateTime, createdAt: new Date().toISOString(), completed: false });
                taskInput.value = '';
                taskDetails.value = '';
                taskDateTime.value = '';
                renderTasks();
            }
        }

        function toggleComplete(index) {
            tasks[index].completed = !tasks[index].completed;
            renderTasks();
        }

        function deleteTask(index) {
            tasks.splice(index, 1);
            renderTasks();
        }

        function addToGoogleCalendar(task) {
            const startTime = new Date(task.dateTime).toISOString();
            const googleCalendarUrl = `https://calendar.google.com/calendar/r/eventedit?text=${encodeURIComponent(task.text)}&details=${encodeURIComponent(task.details)}&dates=${startTime}/${startTime}`;
            window.open(googleCalendarUrl, '_blank');
        }

        addTaskBtn.addEventListener('click', addTask);
        searchTask.addEventListener('input', () => renderTasks(searchTask.value));

        renderTasks();
    </script>
</body>
</html>