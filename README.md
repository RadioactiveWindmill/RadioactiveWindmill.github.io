<html lang="en">
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(45deg, #004080, #1a73e8, #004080);
            background-size: 400% 400%;
            animation: gradientAnimation 15s ease infinite;
            color: #333;
            line-height: 1.6;
        }

        @keyframes gradientAnimation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        header {
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        h1 {
            margin: 0;
            font-size: 2.5em;
        }
        nav {
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
        }
        .menu-btn {
            background-color: #444;
            color: white;
            padding: 15px;
            border: none;
            cursor: pointer;
            width: 100%;
            text-align: center;
            font-size: 20px;
            font-weight: bold;
            border-bottom: 1px solid #555;
            transition: background-color 0.3s ease;
        }
        .menu-btn:hover {
            background-color: #555;
        }
        .menu-content {
            display: none;
            background-color: #333;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            border-bottom: 1px solid #444;
        }
        .menu-content a {
            display: block;
            padding: 15px;
            color: white;
            text-decoration: none;
            font-size: 18px;
            border-bottom: 1px solid #444;
            transition: background-color 0.3s ease;
        }
        .menu-content a:hover {
            background-color: #555;
        }
        main {
            padding: 40px;
            text-align: center;
            background-color: rgba(255, 255, 255, 0.9);
            max-width: 1200px;
            margin: 20px auto;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }
        main h2 {
            color: #004080;
            margin-bottom: 20px;
            font-size: 2em;
        }
        img {
            max-width: 80%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        footer {
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            text-align: center;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
            font-size: 14px;
            box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.1);
        }
    </style>
<body>
    <header>
        <h1>Welcome! Find My Links Here</h1>
    </header>

    <nav>
        <button class="menu-btn" onclick="toggleMenu()">Explore My Projects</button>
        <div id="menu-content" class="menu-content">
            <a href="https://www.printables.com/@radio_windmil_870141/models">Link 1 - Printables</a>
            <a href="https://www.printables.com/model/785737-40-max-shell-40max-nerf-shells-the-stamppot-shells">40max Shell Project</a>
            <a href="#">Link 3</a>
            <a href="#">Link 4</a>
        </div>
    </nav>

    <main>
        <h2>My Printer/Automatic Hot Glue Gun</h2>
        <img src="https://raw.githubusercontent.com/RadioactiveWindmill/RadioactiveWindmill.github.io/main/Images/IMG-20240704-WA0016.jpg" alt="X1C">
        <h2>Profile Picture</h2>
        <img src="https://raw.githubusercontent.com/RadioactiveWindmill/RadioactiveWindmill.github.io/main/Images/IMG_7550.png" alt="Profile Picture">
    </main>

    <footer>
        <p>&copy; 2024 RadioactiveWindmill. All rights reserved.</p>
    </footer>

    <script>
        function toggleMenu() {
            var menuContent = document.getElementById("menu-content");
            if (menuContent.style.display === "block") {
                menuContent.style.display = "none";
            } else {
                menuContent.style.display = "block";
            }
        }
    </script>
</body>
</html>



