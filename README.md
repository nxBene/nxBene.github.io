# nxBene.github.io

<html>
<head>
  <title>Redirecting...</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #181818;
      color: #fff;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: #fff;
    }
    p {
      margin-bottom: 10px;
    }
    a {
      color: #007bff;
      text-decoration: none;
    }
    .affiliate-link {
      font-weight: bold;
    }
    .timer-label {
      color: #aaa;
    }
    .timer-red {
      color: red;
    }
  </style>
</head>
<body>
  <h1>Redirecting...</h1>
  <p>Redirecting to my Homepage If you're stuck on this page, click <a href="https://page.nxBene.repl.co">here</a>.</p>
  <p class="affiliate-link">You are getting sent to <span id="pageName"></span></p>
  <h4 class="timer-label"><span>Time on page:</span> <span id="timer"> calculating </span> seconds</h4>

  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function() {
      $.get("besucher.php");
    });
    
    var url = window.location.href;
    var pageName = url.substring(url.lastIndexOf("/") + 1, url.lastIndexOf(".html"));
    document.getElementById("pageName").textContent = pageName;

    var startTime = new Date().getTime();
    setInterval(function() {
      var currentTime = new Date().getTime();
      var elapsedTime = Math.floor((currentTime - startTime) / 1000);
      document.getElementById("timer").textContent = elapsedTime;

      var timerLabel = document.querySelector(".timer-label");
      if (elapsedTime > 3) {
        timerLabel.classList.add("timer-red");
      } else {
        timerLabel.classList.remove("timer-red");
      }
    }, 1000);

    setTimeout(function() {
      window.location.href = "https://nxBene.repl.co";
    }, 1100);
  </script>
</body>
</html>
