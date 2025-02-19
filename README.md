# Index
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Details Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 20px;
            text-align: center;
        }
        .container {
            width: 50%;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px gray;
        }
        input, button {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #28a745;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        table {
            width: 100%;
            margin-top: 20px;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #007bff;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Student Details Application</h2>
        <input type="text" id="name" placeholder="Enter Student Name">
        <input type="text" id="roll" placeholder="Enter Roll Number">
        <input type="text" id="course" placeholder="Enter Course">
        <button onclick="addStudent()">Add Student</button>
        
        <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Roll Number</th>
                    <th>Course</th>
                </tr>
            </thead>
            <tbody id="studentTable"></tbody>
        </table>
    </div>

    <script>
        function addStudent() {
            let name = document.getElementById("name").value;
            let roll = document.getElementById("roll").value;
            let course = document.getElementById("course").value;
            
            if (name && roll && course) {
                let table = document.getElementById("studentTable");
                let row = table.insertRow();
                row.insertCell(0).innerText = name;
                row.insertCell(1).innerText = roll;
                row.insertCell(2).innerText = course;
                
                document.getElementById("name").value = "";
                document.getElementById("roll").value = "";
                document.getElementById("course").value = "";
            } else {
                alert("Please fill all fields!");
            }
        }
    </script>
</body>
</html>
