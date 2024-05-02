<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Visitor Counter</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  #counter {
    font-size: 24px;
    margin-top: 50px;
  }
</style>
</head>
<body>
  <h1>Welcome to the Visitor Counter!</h1>
  <p>This webpage will count how many people visit it.</p>
  <div id="counter">Loading...</div>

  <script>
    // Function to increment and display the counter
    function incrementCounter() {
      let count = localStorage.getItem('visitCount');
      if (!count) {
        count = 0;
      }
      count++;
      localStorage.setItem('visitCount', count);
      document.getElementById('counter').textContent = "Total Visitors: " + count;
    }

    // Check if the page has been visited before
    if (localStorage.getItem('visitCount')) {
      incrementCounter();
    } else {
      localStorage.setItem('visitCount', 1);
      document.getElementById('counter').textContent = "Total Visitors: 1";
    }
  </script>
</body>
</html>
