<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shaxmat AI o'yini</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Shaxmat o'yini</h1>
    <div id="chess-board"></div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
    margin: 0;
}

h1 {
    text-align: center;
}

#chess-board {
    display: grid;
    grid-template-columns: repeat(8, 60px);
    grid-template-rows: repeat(8, 60px);
    gap: 2px;
}

.square {
    width: 60px;
    height: 60px;
    background-color: #f0d9b5;
    display: flex;
    justify-content: center;
    align-items: center;
}

.square.black {
    background-color: #b58863;
}
const board = document.getElementById("chess-board");

// Shaxmat doskasi yaratish
for (let row = 0; row < 8; row++) {
    for (let col = 0; col < 8; col++) {
        const square = document.createElement("div");
        square.classList.add("square");
        if ((row + col) % 2 === 1) {
            square.classList.add("black");
        }
        board.appendChild(square);
    }
}
