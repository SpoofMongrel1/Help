<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jaguar Way - Rock Paper Scissors</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        h1 {
            color: #333;
        }
        #choices {
            margin-top: 20px;
        }
        .btn {
            margin: 5px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        #result {
            margin-top: 20px;
            font-size: 20px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Jaguar Way - Rock Paper Scissors</h1>
    <div id="choices">
        <button class="btn" onclick="playGame('rock')">Rock</button>
        <button class="btn" onclick="playGame('paper')">Paper</button>
        <button class="btn" onclick="playGame('scissors')">Scissors</button>
    </div>
    <div id="result"></div>

    <script>
        function playGame(playerChoice) {
            const choices = ['rock', 'paper', 'scissors'];
            const computerChoice = choices[Math.floor(Math.random() * choices.length)];

            let result;

            if (playerChoice === computerChoice) {
                result = "It's a tie!";
            } else if (
                (playerChoice === 'rock' && computerChoice === 'scissors') ||
                (playerChoice === 'paper' && computerChoice === 'rock') ||
                (playerChoice === 'scissors' && computerChoice === 'paper')
            ) {
                result = "You win! The Jaguar Way prevails.";
            } else {
                result = "You lose! Keep practicing the Jaguar Way.";
            }

            document.getElementById('result').innerText = result;
        }
    </script>
</body>
</html>
