<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halaman Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f2f5f9;
        }
        .container {
            width: 300px;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            text-align: center;
        }
        h2 {
            margin-bottom: 20px;
            color: #333;
        }
        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .error-message {
            color: red;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Login</h2>
        <form onsubmit="return loginUser()">
            <input type="text" placeholder="Username" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit">Login</button>
        </form>
        <div class="error-message" id="errorMessage"></div>
    </div>

    <script>
        function loginUser() {
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;
            const errorMessage = document.getElementById("errorMessage");

            // Validasi login sederhana
            if (username === "user" && password === "pass123") {
                window.location.href = "https://sites.google.com/your-google-site-url"; // Ganti dengan URL Google Sites Anda
                return false;
            } else {
                errorMessage.textContent = "Username atau password salah!";
                return false;
            }
        }
    </script>
</body>
</html>
