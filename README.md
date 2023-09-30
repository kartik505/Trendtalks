<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login and Signup</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .form-container {
            background-color: #f0f0f0;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .form-container h2 {
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            font-weight: bold;
        }
        .form-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .form-group input[type="submit"] {
            background-color: #007bff;
            color: white;
            border: none;
            cursor: pointer;
        }
        .form-group input[type="submit"]:hover {
            background-color: #0056b3;
        }
        .form-group .message {
            color: red;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="form-container">
            <h2>Login</h2>
            <form action="login.php" method="POST">
                <div class="form-group">
                    <label for="username">Username:</label>
                    <input type="text" id="username" name="username" required>
                </div>
                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password" required>
                </div>
                <div class="form-group">
                    <input type="submit" value="Login">
                </div>
            </form>
            <p class="message">Don't have an account? <a href="#signup">Sign Up</a></p>
        </div>
    </div>

    <div class="container" id="signup">
        <div class="form-container">
            <h2>Sign Up</h2>
            <form action="signup.php" method="POST">
                <div class="form-group">
                    <label for="newUsername">Username:</label>
                    <input type="text" id="newUsername" name="newUsername" required>
                </div>
                <div class="form-group">
                    <label for="newPassword">Password:</label>
                    <input type="password" id="newPassword" name="newPassword" required>
                </div>
                <div class="form-group">
                    <input type="submit" value="Sign Up">
                </div>
            </form>
            <p class="message">Already have an account? <a href="#login">Login</a></p>
        </div>
    </div>

    <script>
        // Toggle between login and signup forms
        document.addEventListener("DOMContentLoaded", function() {
            document.querySelector(".message a[href='#signup']").addEventListener("click", function() {
                document.getElementById("login").style.display = "none";
                document.getElementById("signup").style.display = "block";
            });
            document.querySelector(".message a[href='#login']").addEventListener("click", function() {
                document.getElementById("signup").style.display = "none";
                document.getElementById("login").style.display = "block";
            });
        });
    </script>
</body>
</html>
