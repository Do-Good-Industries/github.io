<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Inbox - Drafts</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f1f1f1;
      margin: 0;
      padding: 0;
    }
    .header {
      background-color: #333;
      color: white;
      padding: 10px;
      text-align: center;
    }
    .container {
      display: flex;
      height: 100vh;
    }
    .sidebar {
      width: 200px;
      background-color: #444;
      color: white;
      padding: 20px;
    }
    .sidebar h2 {
      font-size: 16px;
      border-bottom: 1px solid #555;
      padding-bottom: 5px;
    }
    .sidebar ul {
      list-style-type: none;
      padding-left: 0;
    }
    .sidebar li {
      padding: 8px 0;
    }
    .main {
      flex: 1;
      background-color: white;
      padding: 20px;
      position: relative;
    }
    .password-box {
      margin-bottom: 20px;
    }
    .password-box input[type="password"] {
      padding: 8px;
      width: 250px;
    }
    .password-box button {
      padding: 8px 12px;
    }
    .email {
      display: none;
      background-color: #eef;
      padding: 15px;
      border: 1px solid #99c;
    }

    /* Post-It Note Styling */
    .postit {
      background-color: #fffb88;
      border: 1px solid #e2c94c;
      width: 250px;
      padding: 15px;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      font-size: 14px;
      colour: #333;
      box-shadow: 5px 5px 10px rgba(0,0,0,0.2);
      transform: rotate(-2deg);
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <div class="header">
    <h1>📧 Sigrid Dodson 📧</h1>
    <h2> DO GOOD INDUSTRIES </h2>
  </div>

  <div class="container">
    <div class="sidebar">
      <h2>Folders</h2>
      <ul>
        <li>📥 Inbox</li>
        <li><strong>📝 Drafts (1)</strong></li>
        <li>📤 Sent</li>
        <li>🗑️ Trash</li>
      </ul>
    </div>

    <div class="main">
      <div class="password-box">
        <label for="pw">Enter password to view unopened draft:</label><br>
        <input type="password" id="pw" placeholder="Enter password">
        <button onclick="checkPassword()">Unlock</button>
        <p id="wrong" style="color:red; display:none;">Incorrect password.</p>
      </div>

      <!-- Post-It Note with Riddle -->
      <div class="postit">
        🔐 *Riddle me this...*<br><br>
        A spark in the dark, I guide through the night,
Born in the heart, I make futures bright.
Not seen, but felt, in despair I cope.<br>
      <br>
        <strong>What am I?</strong>
      </div>

      <div class="email" id="email">
        <h3>Draft: RE: The Drop</h3>
        <p>Meet me at the location at 21:00 hrs in Part 2. Bring the device.</p>
        <p>Flag: <strong>{49 27 76 65 20 67 6F 74 20 61 20 6C 6F 76 65 6C 79 20 62 75 6E 63 68 20 6F 66 20 63 6F 63 6F 6E 75 74 73}</strong></p>
      </div>
    </div>
  </div>

  <script>
    const correctPassword = "Hope"; // You can change this

    function checkPassword() {
      const input = document.getElementById("pw").value;
      const email = document.getElementById("email");
      const wrong = document.getElementById("wrong");
      
      if (input === correctPassword) {
        email.style.display = "block";
        wrong.style.display = "none";
      } else {
        email.style.display = "none";
        wrong.style.display = "block";
      }
    }
  </script>

</body>
</html>
