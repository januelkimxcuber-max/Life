# Trans

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Would You Rather?</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      background: linear-gradient(135deg, #667eea, #764ba2);
      font-family: Arial, sans-serif;
      color: white;
      text-align: center;
    }

    .container {
      width: 100%;
      max-width: 420px;
      padding: 30px 22px;
      background: rgba(255, 255, 255, 0.13);
      border: 1px solid rgba(255,255,255,0.2);
      border-radius: 22px;
      box-shadow: 0 10px 35px rgba(0,0,0,0.2);
    }

    h1 {
      font-size: 27px;
      line-height: 1.4;
    }

    p {
      color: #eee;
    }

    input {
      width: 100%;
      padding: 15px;
      margin-top: 15px;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      outline: none;
    }

    button {
      width: 100%;
      padding: 14px;
      margin-top: 12px;
      border: none;
      border-radius: 10px;
      background: #fff;
      color: #764ba2;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
    }

    button:hover {
      background: #eee;
    }

    #result {
      display: none;
      margin-top: 25px;
      font-size: 25px;
      font-weight: bold;
      line-height: 1.5;
      overflow-wrap: anywhere;
    }

    .warning {
      font-size: 35px;
    }

    .footer {
      margin-top: 28px;
      font-size: 12px;
      color: #ddd;
    }
  </style>
</head>

<body>
  <div class="container">
    <div id="question">
      <h1>🤔 Would you rather be trans or transformer?</h1>
      <p>Type your answer below. Be honest! 👀</p>

      <input
        id="answer"
        type="text"
        placeholder="Type your answer..."
        autocomplete="off"
      >

      <button onclick="submitAnswer()">Submit Answer</button>
    </div>

    <div id="result">
      <div class="warning">🚨😂</div>
      I knew you're Transgender!!!
      <p style="font-size:16px">
        BRO GOT CAUGHT BEFORE EVEN PRESSING SUBMIT 💀
      </p>
      <button onclick="location.reload()">Try Again</button>
    </div>

    <div class="footer">
      Just a prank 😂
    </div>
  </div>

  <script>
    const answer = document.getElementById("answer");
    let caught = false;

    function catchPrank() {
      if (caught) return;

      caught = true;
      document.getElementById("question").style.display = "none";
      document.getElementById("result").style.display = "block";
    }

    answer.addEventListener("input", function () {
      if (this.value.toLowerCase().includes("trans")) {
        catchPrank();
      }
    });

    function submitAnswer() {
      if (answer.value.trim() !== "") {
        catchPrank();
      }
    }
  </script>
</body>
</html>

