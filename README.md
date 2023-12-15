# LogIn-Form-in-htmls-css-java
This repository contains a simple and responsive login form created using HTML, CSS, and JavaScript. The form includes basic validation for email format and password length, implemented with JavaScript. The design is clean and user-friendly, making it easy to integrate into web projects.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      text-align: center;
      margin: 50px;
    }
    form {
      max-width: 300px;
      margin: 0 auto;
      padding: 20px;
      background-color: #fff;
      border-radius: 5px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    input {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
      box-sizing: border-box;
    }
    button {
      background-color: #4caf50;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <form id="loginForm" onsubmit="return validateForm()">
    <h2>Login</h2>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <br>
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" minlength="8" required>
    <br>
    <button type="submit">Login</button>
  </form>

  <script>
    function validateForm() {
      var email = document.getElementById("email").value;
      var password = document.getElementById("password").value;

     
      var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRegex.test(email)) {
        alert("Invalid email format");
        return false;
      }

      if (password.length < 8) {
        alert("Password must be at least 8 characters long");
        return false;
      }

      return true;
    }
  </script>

</body>
</html>
