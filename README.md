<html lang="en">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #ffA500;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        .menu-btn {
            background-color: #333;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
            width: 100%;
            text-align: left;
            font-size: 18px;
        }
        .menu-content {
            display: none;
            background-color: #444;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
        }
        .menu-content a {
            display: block;
            padding: 10px;
            color: white;
            text-decoration: none;
            background-color: #555;
        }
        .menu-content a:hover {
            background-color: #666;
        }
        main {
            padding: 20px;
            text-align: center;
        }
        img {
            max-width: 100%;
            height: auto;
        }
    </style>
<body>
    <header>
        <h1>Welcome, find my Links here!</h1>
    </header>

    <nav>
        <h3>Contact me on discord for questions and tips: Vliegtuigje aka Space</h3>
        <button class="menu-btn" onclick="toggleMenu()">Menu</button>
        <div id="menu-content" class="menu-content">
            <a href="https://www.printables.com/@radio_windmil_870141/models">Link 1 - Printables</a>
            <a href="https://www.printables.com/model/785737-40-max-shell-40max-nerf-shells-the-stamppot-shells">40max Shell Project</a>
            <a href="#">Link 3</a>
            <a href="#">Link 4</a>
        </div>
    </nav>

    <main>
        <h2>My printer/automatic hot glue gun</h2>
        <img src="https://raw.githubusercontent.com/RadioactiveWindmill/RadioactiveWindmill.github.io/main/Images/IMG-20240704-WA0016.jpg" alt="X1C">
        <h2>Profile picture</h2>
        <img src="https://raw.githubusercontent.com/RadioactiveWindmill/RadioactiveWindmill.github.io/main/Images/IMG_7550.png" alt="Profile picture">
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
    </script>
</body>
</html>



