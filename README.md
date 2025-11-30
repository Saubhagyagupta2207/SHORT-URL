# Uncountable genrate strong password
code for generate in uncountable number strong password
<!DOCTYPE html>
<html>
<head>
    <title>Black Aesthetic Password Generator</title>
    <style>
        body {
            background-color: #000; /* Black background */
            color: #fff; /* White text */
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        h1 {
            margin-bottom: 20px;
        }
        input[type=number] {
            padding: 10px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            margin-right: 10px;
            width: 80px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #1e90ff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #63b3ed;
        }
        #password {
            margin-top: 30px;
            font-size: 24px;
            word-break: break-all;
            max-width: 80%;
        }
    </style>
</head>
<body>
    <h1>Black Aesthetic Password Generator</h1>
    <div>
        <input type="number" id="lengthInput" min="6" max="64" value="12" />
        <button onclick="generatePassword()">Generate Password</button>
    </div>
    <div id="password"></div>

    <script>
        function generatePassword() {
            const length = parseInt(document.getElementById('lengthInput').value) || 12;
            const charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()_+~`|}{[]:;?><,./-=";
            let password = "";
            for (let i = 0; i < length; i++) {
                const randomIndex = Math.floor(Math.random() * charset.length);
                password += charset[randomIndex];
            }
            document.getElementById('password').innerText = password;
        }
    </script>
</body>
</html>
