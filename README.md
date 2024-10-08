<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Main Website</title>
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 0;
            color: #e0e0e0;
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
            background: linear-gradient(135deg, #000000 0%, #ff6600 100%);
            background-size: 200% 200%;
            animation: gradientAnimation 15s ease infinite;
        }

        header {
            background-color: rgba(0, 0, 0, 0.8);
            color: #ff6600;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        h1 {
            margin: 0;
            font-size: 2.5em;
        }

        .menu-btn {
            background-color: #333;
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
            background-color: #444;
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
            color: #ff6600;
            text-decoration: none;
            font-size: 18px;
            border-bottom: 1px solid #444;
            transition: background-color 0.3s ease;
        }

        .menu-content a:hover {
            background-color: #444;
        }

        .side-menu {
            height: 100%;
            width: 250px;
            position: fixed;
            top: 0;
            left: 0;
            background-color: #333;
            overflow-x: hidden;
            padding-top: 60px;
            z-index: 1;
            transition: width 0.5s ease;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.5);
        }

        .side-menu a {
            padding: 15px 25px;
            text-decoration: none;
            font-size: 22px;
            color: #ff6600;
            display: block;
            transition: 0.3s;
        }

        .side-menu a:hover {
            background-color: #444;
        }

        .side-menu .close-btn {
            position: absolute;
            top: 10px;
            right: 25px;
            font-size: 36px;
            margin-left: 50px;
            color: #ff6600;
            cursor: pointer;
        }

        .open-side-menu-btn {
            font-size: 20px;
            cursor: pointer;
            background-color: #444;
            color: white;
            padding: 15px 20px;
            border: none;
            transition: background-color 0.3s ease;
            position: fixed;
            top: 60px;
            left: 10px;
            z-index: 2;
        }

        .open-side-menu-btn.hidden {
            display: none;
        }

        .open-side-menu-btn:hover {
            background-color: #555;
        }

        main {
            padding: 40px;
            text-align: center;
            background-color: rgba(34, 34, 34, 0.9);
            max-width: 1200px;
            margin: 20px auto;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            border-radius: 10px;
            position: relative;
            z-index: 1;
        }

        main h2 {
            color: #ff6600;
            margin-bottom: 20px;
            font-size: 2em;
        }

        img {
            max-width: 80%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        @keyframes gradientAnimation {
            0% {
                background-position: 0% 0%;
            }
            50% {
                background-position: 100% 100%;
            }
            100% {
                background-position: 0% 0%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome! Find My Links Here</h1>
    </header>

    <nav>
        <button class="menu-btn" onclick="toggleMenu()">Explore My Projects</button>
        <div id="menu-content" class="menu-content">
            <a href="https://www.printables.com/@radio_windmil_870141/models">Printables</a>
            <a href="https://www.printables.com/model/785737-40-max-shell-40max-nerf-shells-the-stamppot-shells">40max Shell Project</a>
            <a href="#">Link 3</a>
            <a href="#">Link 4</a>
        </div>
    </nav>

    <!-- Side Menu -->
    <div id="side-menu" class="side-menu">
        <a href="javascript:void(0)" class="close-btn" onclick="closeSideMenu()">&times;</a>
        <a href="#">Link 1</a>
        <a href="/lonx">My Lonx</a> <!-- Updated link to the /lonx subdomain -->
        <a href="#">Link 3</a>
        <a href="#">Link 4</a>
        <a href="#">Link 5</a>
        <a href="#">Link 6</a>
        <a href="#">Link 7</a>
        <a href="#">Link 8</a>
    </div>

    <!-- Button to open the side menu -->
    <button id="open-side-menu-btn" class="open-side-menu-btn" onclick="toggleSideMenu()">Collection</button>

    <main>
        <h2>My Printer/Automatic Hot Glue Gun</h2>
        <img src="https://raw.githubusercontent.com/RadioactiveWindmill/RadioactiveWindmill.github.io/main/Images/IMG-20240704-WA0016.jpg" alt="X1C">
        <h2>Profile Picture</h2>
        <img src="https://raw.githubusercontent.com/RadioactiveWindmill/RadioactiveWindmill.github.io/main/Images/IMG_7550.png" alt="Profile Picture">
    </main>

    <script>
        function toggleMenu() {
            var menuContent = document.getElementById("menu-content");
            if (menuContent.style.display === "block") {
                menuContent.style.display = "none";
            } else {
                menuContent.style.display = "block";
            }
        }

        function toggleSideMenu() {
            var sideMenu = document.getElementById("side-menu");
            var openButton = document.getElementById("open-side-menu-btn");
            if (sideMenu.style.width === "250px") {
                sideMenu.style.width = "0";
                openButton.classList.remove("hidden");
            } else {
                sideMenu.style.width = "250px";
                openButton.classList.add("hidden");
            }
        }

        function closeSideMenu() {
            document.getElementById("side-menu").style.width = "0";
            document.getElementById("open-side-menu-btn").classList.remove("hidden");
        }
    </script>
</body>
</html>


