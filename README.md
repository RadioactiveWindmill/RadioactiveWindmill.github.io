<html lang="en">
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(45deg, #222, #ff6600, #222);
            background-size: 400% 400%;
            animation: gradientAnimation 15s ease infinite;
            color: #e0e0e0;
            line-height: 1.6;
        }

        @keyframes gradientAnimation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
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
        main {
            padding: 40px;
            text-align: center;
            background-color: rgba(34, 34, 34, 0.9);
            max-width: 1200px;
            margin: 20px auto;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            border-radius: 10px;
        }
        main h2 {
            color: #ff6600;
            margin-bottom: 20px;
            font-size: 2em;
        }
        img {
            max-width: 80%;
            height: auto;
            border-radius: 10



