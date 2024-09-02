<html lang="en">
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #222;
            color: #e0e0e0;
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
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
        nav {
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
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

        /* Left-side collapsible menu */
        .side-menu {
            height: 100%;
            width: 0;
            position: fixed;
            z-index: 1;
            top: 0;
            left: 0;
            background-color: #333;
            overflow-x: hidden;
            transition: 0.5s;
            padding-top: 60px;
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
        footer {
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            text-align: center;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
            font-size: 14px;
            box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.5);
        }

        /* Bubble animation */
        .bubble {
            position: absolute;
            bottom: -100px;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 102, 0, 0.6);
            border-radius: 50%;
            opacity: 0.7;
            animation: bubbleAnimation 15s infinite ease-in-out;
        }

        .bubble:nth-child(2) {
            left: 10%;
            width: 60px;
            height: 60px;
            background-color: rgba(255, 102, 0, 0.5);
            animation-duration: 18s;
            animation-delay: 2s;
        }

        .bubble:nth-child(3) {
            left: 30%;
            width: 30px;
            height: 30px;
            background-color: rgba(255, 102, 0, 0.4);
            animation-duration: 12s;
            animation-delay: 4s;
        }

        .bubble:nth-child(4) {
            left: 50%;
            width: 50px;
            height: 50px;
            background-color: rgba(255, 102, 0, 0.3);
            animation-duration: 14s;
            animation-delay: 6s;
        }

        .bubble:nth-child(5) {
            left: 70%;
            width: 20px;
            height: 20px;
            background-color: rgba(255, 102, 0, 0.6);
            animation-duration: 16s;
            animation-delay: 8s;
        }

        .bubble:nth-child(6) {
            left: 80%;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 102, 0, 0.5);
            animation-duration: 20s;
            animation-delay: 10s;
        }

        .bubble:nth-child(7) {
            left: 20%;
            width: 50px;
            height: 50px;
            background-color: rgba(255, 102, 0, 0.4);
            animation-duration: 22s;
            animation-delay: 12s;
        }

        .bubble:nth-child(8) {
            left: 40%;
            width: 35px;
            height: 35px;
            background-color: rgba(255, 102, 0, 0.6);
            animation-duration: 24s;
            animation-delay: 14s;
        }

        .bubble:nth-child(9) {
            left: 60%;
            width: 25px;
            height: 25px;
            background-color: rgba(255, 102, 0, 0.5);
            animation-duration: 26s;
            animation-delay: 16s;
        }

        .bubble:nth-child(10) {
            left: 80%;
            width: 45px;
            height: 45px;
            background-color: rgba(255, 102, 0, 0.4);
            animation-duration: 28s;
            animation-delay: 18s;
        }

        @keyframes bubbleAnimation {
            0% {
                bottom: -100px;
                transform: translateX(0) scale(1);
                opacity: 0.7;
            }
            50% {
                transform: translateX(20px) scale(1.2);
                opacity: 0.5;
            }
            100% {
                bottom: 100%;
                transform: translateX(-20px) scale(1);
                opacity: 0;
            }
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

    <!-- Side Menu -->
    <div id="side-menu" class="side-menu">
        <a href="javascript:void(0)" class="close-btn" onclick="closeSideMenu()">&times;</a>
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
        <a href="#">Link 4</a>
        <a href="#">Link 5</a>
        <a href="#">Link 6</a>
        <a href="#">Link 7</a>
        <a href="#">Link 8</a>
    </div>

    <!-- Button to open the side menu -->
    <button class="open-side-menu-btn" onclick="openSideMenu()">Collection</button>

    <!-- Bubble Animation -->
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>

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

        function openSideMenu() {
            document.getElementById("side-menu").style.width = "250px";
        }

        function closeSideMenu() {
            document.getElementById("side-menu").style.width = "0";
        }
    </script>
</body>
</html>
