// تسجيل دخول بسيط (بدون Firebase حالياً)
function login() {
    let email = document.getElementById("email").value;
    let password = document.getElementById("password").value;

    if (email && password) {
        alert("تم تسجيل الدخول بنجاح 🚀");
        window.location.href = "dashboard.html";
    } else {
        alert("الرجاء إدخال البيانات");
    }
}

// إدارة المهام
let tasks = [];

function addTask() {
    let taskInput = document.getElementById("task");
    let task = taskInput.value;

    if (task !== "") {
        tasks.push(task);
        taskInput.value = "";
        displayTasks();
    }
}

function displayTasks() {
    let list = document.getElementById("taskList");
    list.innerHTML = "";

    tasks.forEach((t) => {
        let li = document.createElement("li");
        li.textContent = t;
        list.appendChild(li);
    });
}