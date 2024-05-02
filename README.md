<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Game Collection</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: red; /* Background color set to red */
  }
  .game {
    margin-bottom: 20px;
  }
</style>
</head>
<body>
  <h1>Welcome to the Game Collection!</h1>
  
  <!-- Game 1 -->
  <div class="game">
    <h2>Game 1</h2>
    <iframe src="https://cdn.htmlgames.com/embed.js?game=AirportSniper&amp;bgcolor=white" width="800" height="600" frameborder="0"></iframe>
    <p>Players Playing: <span id="game1Count">0</span></p>
  </div>

  <!-- Game 2 -->
  <div class="game">
    <h2>Game 2</h2>
    <iframe src="https://cdn.htmlgames.com/embed.js?game=TrafficRacer2&amp;bgcolor=white%22%3E%3C/script%3E%3C/div%3E" width="800" height="600" frameborder="0"></iframe>
    <p>Players Playing: <span id="game2Count">0</span></p>
  </div>

  <!-- Game 3 -->
  <div class="game">
    <h2>Game 3</h2>
    <iframe src="<div><script src="https://cdn.htmlgames.com/embed.js?game=ToyFactory&amp;bgcolor=white"></script></div>" width="800" height="600" frameborder="0">
 </iframe>
      <p>Players Playing: <span id= game3count>0</span></p>
  </div>
   <-- Keep track of players playing each game -->
  <script>
    function updatePlayerCount(gameNumber, count) {
      document.getElementById('game' + gameNumber + 'Count').textContent = count;
    }

    window.addEventListener('message', function(event) {
      if (event.data.type === 'playerCountUpdate') {
        updatePlayerCount(event.data.gameNumber, event.data.count);
      }
    });
  </script>

</body>
</html>
