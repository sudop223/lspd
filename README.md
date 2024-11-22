<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LSPD Rank System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            color: #333;
        }
        header {
            background-color: #003366;
            color: white;
            padding: 20px;
            text-align: center;
        }
        header img {
            height: 50px;
            vertical-align: middle;
        }
        header h1 {
            display: inline-block;
            margin: 0;
            padding-left: 10px;
            font-size: 24px;
        }
        .container {
            padding: 20px;
        }
        .rank-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        .rank-item {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 15px;
            width: 250px;
            text-align: center;
        }
        .rank-item img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }
        .rank-item h2 {
            font-size: 18px;
            margin: 10px 0 5px;
        }
        .stars {
            color: gold;
            font-size: 20px;
            display: flex;
            justify-content: center;
            margin: 10px 0;
        }
        .stars i {
            cursor: pointer;
            margin: 0 3px;
        }
        .stars i.inactive {
            color: lightgray;
        }
        footer {
            background-color: #003366;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <img src="lspd-logo.png" alt="LSPD Logo">
        <h1>LSPD Rank System</h1>
    </header>
    <div class="container">
        <div class="rank-list">
            <!-- Example rank card -->
            <div class="rank-item" data-rank="Chief">
                <img src="chief-image-placeholder.jpg" alt="Chief Rank">
                <h2>Chief</h2>
                <div class="stars">
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                </div>
            </div>
            <div class="rank-item" data-rank="Deputy Chief">
                <img src="deputy-chief-image-placeholder.jpg" alt="Deputy Chief Rank">
                <h2>Deputy Chief</h2>
                <div class="stars">
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                    <i class="fas fa-star inactive" onclick="toggleStar(this)"></i>
                </div>
            </div>
            <!-- Add more ranks as needed -->
        </div>
    </div>
    <footer>
        &copy; 2024 Los Santos Police Department
    </footer>
    <script>
        function toggleStar(starElement) {
            const starsContainer = starElement.parentElement;
            const stars = starsContainer.querySelectorAll('i');

            // Find the index of the clicked star
            const clickedIndex = Array.from(stars).indexOf(starElement);

            // Update stars based on the clicked star
            stars.forEach((star, index) => {
                if (index <= clickedIndex) {
                    star.classList.remove('inactive');
                } else {
                    star.classList.add('inactive');
                }
            });
        }
    </script>
    <!-- Add Font Awesome for star icons -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</body>
</html>
