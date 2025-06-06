<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Pattern</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #222;
            color: white;
            font-family: Arial, sans-serif;
            overflow: hidden;
            text-align: center;
            flex-direction: column;
        }
        .pattern {
            display: grid;
            grid-template-columns: repeat(7, auto);
            gap: 10px;
            font-size: 24px;
            text-transform: uppercase;
            font-weight: bold;
        }
        .pattern span {
            animation: fadeIn 2s infinite alternate;
        }
        @keyframes fadeIn {
            0% { opacity: 0.3; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="pattern">
        <span>W</span> <span>E</span> <span>L</span> <span>C</span> <span>O</span> <span>M</span> <span>E</span>
    </div>
    <br>
    <div class="pattern">
        <span>M</span> <span>Y</span>&nbsp;<span>W</span> <span>E<span> <span>B<span>&nbsp;&nbsp;  <span>P</span> <span>A</span> </span>G<span>
</body>
</html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover [Country Name]</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <style>
        /* Loading Animation */
        .wrapper {
            width: 200px;
            height: 60px;
            position: relative;
            z-index: 1;
        }

        .circle {
            width: 20px;
            height: 20px;
            position: absolute;
            border-radius: 50%;
            background-color: #fff;
            left: 15%;
            transform-origin: 50%;
            animation: circle7124 .5s alternate infinite ease;
        }

        @keyframes circle7124 {
            0% {
                top: 60px;
                height: 5px;
                border-radius: 50px 50px 25px 25px;
                transform: scaleX(1.7);
            }

            40% {
                height: 20px;
                border-radius: 50%;
                transform: scaleX(1);
            }

            100% {
                top: 0%;
            }
        }

        .circle:nth-child(2) {
            left: 45%;
            animation-delay: .2s;
        }

        .circle:nth-child(3) {
            left: auto;
            right: 15%;
            animation-delay: .3s;
        }

        .shadow {
            width: 20px;
            height: 4px;
            border-radius: 50%;
            background-color: rgba(0,0,0,0.9);
            position: absolute;
            top: 62px;
            transform-origin: 50%;
            z-index: -1;
            left: 15%;
            filter: blur(1px);
            animation: shadow046 .5s alternate infinite ease;
        }

        @keyframes shadow046 {
            0% {
                transform: scaleX(1.5);
            }

            40% {
                transform: scaleX(1);
                opacity: .7;
            }

            100% {
                transform: scaleX(.2);
                opacity: .4;
            }
        }

        .shadow:nth-child(4) {
            left: 45%;
            animation-delay: .2s;
        }

        .shadow:nth-child(5) {
            left: auto;
            right: 15%;
            animation-delay: .3s;
        }

        #loading {
            background-color: blue;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        #content {
            display: none;
        }
    </style>
</head>
<body class="bg-gray-100">
    <!-- Loading Screen -->
    <div id="loading">
        <div class="wrapper">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="shadow"></div>
            <div class="shadow"></div>
            <div class="shadow"></div>
        </div>
    </div>

    <!-- Main Content -->
    <div id="content" style="display: none;">
        <!-- Navbar -->
        <nav class="bg-blue-600 p-4 text-white flex justify-between">
            <h1 class="text-2xl font-bold">Discover [Country Name]</h1>
            <ul class="flex space-x-4">
                <li><a href="#about" class="hover:underline">About</a></li>
                <li><a href="#culture" class="hover:underline">Culture</a></li>
                <li><a href="#attractions" class="hover:underline">Attractions</a></li>
                <li><a href="#contact" class="hover:underline">Contact</a></li>
            </ul>
        </nav>
        
        <!-- Hero Section -->
        <section class="relative h-screen bg-cover bg-center" style="background-image: url('https://source.unsplash.com/1600x900/?nature,landscape')">
            <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-center items-center text-white">
                <h2 class="text-5xl font-bold">Welcome to [Country Name]</h2>
                <p class="text-xl mt-2">Explore the beauty, culture, and history of our nation.</p>
            </div>
        </section>
        
        <!-- About Section -->
        <section id="about" class="p-8 text-center">
            <h2 class="text-3xl font-bold">About [Country Name]</h2>
            <p class="mt-4 text-gray-700">[Add information about the country’s history, geography, and significance]</p>
        </section>
        
        <!-- Culture Section -->
        <section id="culture" class="bg-gray-200 p-8 text-center">
            <h2 class="text-3xl font-bold">Culture & Traditions</h2>
            <p class="mt-4 text-gray-700">[Highlight traditions, festivals, food, and more]</p>
        </section>
        
        <!-- Attractions Section -->
        <section id="attractions" class="p-8 text-center">
            <h2 class="text-3xl font-bold">Top Attractions</h2>
            <p class="mt-4 text-gray-700">[Describe famous places to visit]</p>
        </section>
        
        <!-- Contact Section -->
        <section id="contact" class="bg-blue-600 p-8 text-white text-center">
            <h2 class="text-3xl font-bold">Contact Us</h2>
            <p class="mt-4">Get in touch for more information.</p>
        </section>
        
        <!-- Footer -->
        <footer class="bg-gray-800 text-white p-4 text-center">
            <p>&copy; 2025 Discover [Country Name]. All rights reserved.</p>
        </footer>
    </div>

    <script>
        setTimeout(() => {
            document.getElementById('loading').style.display = 'none';
            document.getElementById('content').style.display = 'block';
        }, 5000);
    </script>
</body>
</html>
