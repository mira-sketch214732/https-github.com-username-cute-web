<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cute Website</title>
    <style>
        /* Basic website styles */
        body {
            font-family: 'Arial', sans-serif;
            background-image: url('https://image.freepik.com/free-photo/beautiful-abstract-pattern-background-floral_1102991-14704.jpg');  /* Background image */
            background-size: cover;
            background-position: center;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            flex-direction: column;
        }

        /* Header section with email and contact info */
        .header {
            position: absolute;
            top: 20px;
            width: 100%;
            text-align: center;
            color: #ff5474; /* Pink color */
            font-size: 20px;
        }

        .header a {
            color: #ff5474;
            text-decoration: none;
            font-weight: bold;
        }

        /* Login page styling */
        .login-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .login-btn {
            background-color: #ff5474; /* Darker pink */
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 50px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }

        .login-btn:hover {
            transform: scale(1.05);
        }

        /* Main content after login */
        .main-content {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            background-color: rgba(255, 255, 255, 0.8); /* Semi-transparent background */
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            position: relative;
            transform: translateY(-50px);  /* Slightly above the center for better focus */
        }

        .cute-img {
            width: 120px;
            height: 120px;
            margin-bottom: 20px;
        }

        .question {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #ff5474; /* Darker pink for text */
        }

        /* Buttons styling */
        .yes-btn, .no-btn {
            background-color: #ff5474;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 20px;
            cursor: pointer;
            border-radius: 10px;
            margin: 15px;
            transition: transform 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .yes-btn:hover, .no-btn:hover {
            transform: scale(1.1);
        }

        /* "No" button escaping */
        .no-btn.escaped {
            position: absolute;
            top: 20px;
            left: 100px;
            transition: top 0.5s ease, left 0.5s ease;
        }

        footer {
            position: fixed;
            bottom: 10px;
            width: 100%;
            text-align: center;
            color: #777;
        }
    </style>
</head>
<body>

    <!-- Header with contact info -->
    <div class="header">
        <p>For website design or advertisements, contact us at <a href="mailto:miratoru241@gmail.com">miratoru241@gmail.com</a></p>
    </div>

    <div id="login-container" class="login-container">
        <button id="loginBtn" class="login-btn">Log in with Google</button>
    </div>

    <div id="main-content" class="main-content" style="display: none;">
        <div class="cute-message">
            <!-- The new image after login -->
            <img src="https://image.freepik.com/free-vector/angel-heart-cartoon-vector-illustration-valentine-concept-icon-isolated_772770-689.jpg" alt="Cute Angel Heart" class="cute-img">
            <p class="question">Do you want to be my sweetheart?</p>
            <button id="yesBtn" class="yes-btn">Yes</button>
            <button id="noBtn" class="no-btn">No</button>
        </div>
    </div>

    <footer>
        <p>&copy; 2025 All rights reserved</p>
    </footer>

    <script>
        // Get elements
        const loginBtn = document.getElementById('loginBtn');
        const mainContent = document.getElementById('main-content');
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');

        // Simulate login (you can later replace this with actual Google login integration)
        loginBtn.addEventListener('click', function() {
            loginBtn.style.display = 'none'; // Hide login button
            mainContent.style.display = 'block'; // Show main content after login
        });

        // Interaction with the "Yes" button
        yesBtn.addEventListener('click', function() {
            alert('You are my sweetheart now! ??');
        });

        // Interaction with the "No" button
        noBtn.addEventListener('mouseover', function() {
            // Make the "No" button escape
            noBtn.classList.add('escaped');
        });

        // Reset the "No" button back to its place when mouse leaves
        noBtn.addEventListener('mouseleave', function() {
            noBtn.classList.remove('escaped');
        });
    </script>
</body>
</html>
