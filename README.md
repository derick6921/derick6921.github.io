<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Cat Dance</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  #cat {
    position: fixed;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    animation: catDance 20s infinite;
  }
  @keyframes catDance {
    0% { transform: translateX(-50%) rotate(0deg); }
    25% { transform: translateX(-50%) rotate(-10deg); }
    50% { transform: translateX(-50%) rotate(0deg); }
    75% { transform: translateX(-50%) rotate(10deg); }
    100% { transform: translateX(-50%) rotate(0deg); }
  }
</style>
</head>
<body>
  <h1>Welcome to the Happy Cat Dance!</h1>
  <p>Watch the happy cat dance below!</p>
  <img id="cat" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="Happy Cat">
</body>
</html>
