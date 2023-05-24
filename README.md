<!DOCTYPE html>
<html>
<head>
  <title>Hacked Website</title>
  <style>
    body {
      background-color: #000;
      color: #fff;
      text-align: center;
      font-family: Arial, sans-serif;
    }
    
    h1 {
      font-size: 48px;
      margin-top: 200px;
    }
    
    #progress-bar {
      width: 300px;
      height: 30px;
      margin: 20px auto;
      background-color: #444;
    }
    
    #progress {
      width: 0;
      height: 30px;
      background-color: #ff0000;
    }
    
    #countdown {
      font-size: 24px;
      margin-bottom: 100px;
    }
  </style>
</head>
<body>
  <h1>Your computer has been hacked!</h1>
  
  <div id="progress-bar">
    <div id="progress"></div>
  </div>
  
  <div id="countdown">5</div>
  
  <script>
    var progressBar = document.getElementById("progress");
    var countdown = document.getElementById("countdown");
    var timeLeft = 5;
    
    var timer = setInterval(function() {
      timeLeft--;
      countdown.textContent = timeLeft;
      
      if (timeLeft === 0) {
        clearInterval(timer);
        countdown.textContent = "Hacking complete!";
      }
    }, 1000);
    
    var progress = 0;
    var progressInterval = setInterval(function() {
      progress += 10;
      progressBar.style.width = progress + "px";
      
      if (progress >= 300) {
        clearInterval(progressInterval);
      }
    }, 500);
  </script>
</body>
</html>
