<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ms. Red Proposal</title>
    <style>
        body {
            font-family: 'Cursive', Arial, sans-serif;
            background-color: #ffeaf4; /* Soft pink background */
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .section {
            display: none;
            margin-top: 20%;
        }
        .active {
            display: block;
        }
        h1 {
            font-size: 36px;
            color: #ff5d8f; /* Soft red-pink for the question */
        }
        p {
            font-size: 20px;
            color: #555;
        }
        button {
            background-color: #ff80ab; /* Cute pink buttons */
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 20px;
            cursor: pointer;
            margin: 10px;
            border-radius: 25px; /* Rounded buttons for aesthetic touch */
            transition: background-color 0.3s, transform 0.2s;
        }
        button:hover {
            background-color: #ff4d6d;
            transform: scale(1.05); /* Slight zoom effect */
        }
        .back {
            margin-top: 20px;
            display: block;
            font-size: 16px;
            color: #777;
            text-decoration: underline;
            cursor: pointer;
        }
        img {
            max-width: 80%;
            margin-top: 20px;
            border-radius: 15px; /* Rounded edges for the image */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Add a soft shadow */
        }
    </style>
</head>
<body>
    <!-- Main Section -->
    <div id="main" class="section active">
        <h1>Ms. Red, please accept me.</h1>
        <button onclick="showSection('yes')">Yes</button>
        <button onclick="showSection('no')">No</button>
    </div>

    <!-- Yes Section -->
    <div id="yes" class="section">
        <h1>Congratulations, Ms. Red!</h1>
        <p>I am all yours. ❤️</p>
        <span class="back" onclick="showSection('main')">Go back</span>
    </div>

    <!-- No Section -->
    <div id="no" class="section">
        <button onclick="showSection('like')">Yes</button>
        <button onclick="showSection('reconsider')">No</button>
        <span class="back" onclick="showSection('main')">Go back</span>
    </div>

    <!-- Like Section -->
    <div id="like" class="section">
        <h1>I really like you so much, Ms. Red. Congratulations!</h1>
        <p>❤️</p>
        <span class="back" onclick="showSection('no')">Go back</span>
    </div>

    <!-- Reconsider Section -->
    <div id="reconsider" class="section">
        <h1>Please accept me, Ms. Red.</h1>
        <button onclick="showSection('waiting')">Yes</button>
        <button onclick="showSection('final')">No</button>
        <span class="back" onclick="showSection('no')">Go back</span>
    </div>

    <!-- Waiting Section -->
    <div id="waiting" class="section">
        <h1>I will be waiting for you until you be aunt and I will always be there for you. Congratulations!!</h1>
        <p>❤️</p>
        <span class="back" onclick="showSection('reconsider')">Go back</span>
    </div>

    <!-- Final Section -->
    <div id="final" class="section">
        <h1>Please accept me, Ms. Red.</h1>
        <button onclick="showSection('coffee')">🫠</button>
        <span class="back" onclick="showSection('reconsider')">Go back</span>
    </div>

    <!-- Coffee Section -->
    <div id="coffee" class="section">
        <h1>You have come this far.</h1>
        <p>Now let's have a coffee this Saturday. ☕</p>
        <img src="crying-cat.jpg" alt="Crying Cat">
        <span class="back" onclick="showSection('final')">Go back</span>
    </div>

    <script>
        // Function to show a specific section and hide others
        function showSection(sectionId) {
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => section.classList.remove('active'));
            document.getElementById(sectionId).classList.add('active');
        }
    </script>
</body>
</html>
