# physics-class-website

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">
  <title>Lesson with Tee</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 25px;
      background: #f1f5f9;
    }
    section {
      background: white;
      padding: 20px;
      margin-bottom: 20px;
      border-radius: 10px;
    }
    input, textarea, button {
      display: block;
      width: 100%;
      box-sizing: border-box;
      padding: 12px;
      margin: 10px 0;
    }
    button {
      background: #123b70;
      color: white;
      border: none;
      border-radius: 5px;
    }
  </style>
</head>
<body>

  <h1>Lesson with Tee</h1>

  <section>
    <h2>Student Updates</h2>
    <h3 id="shownTitle">Welcome!</h3>
    <p id="shownMessage">
      New lesson information will appear here.
    </p>
  </section>

  <section>
    <h2>Admin Panel</h2>
    <input id="password" type="password"
           placeholder="Demo password">
    <button onclick="login()">Login</button>

    <div id="editor" hidden>
      <input id="title" placeholder="Update title">
      <textarea id="message"
                placeholder="Write your update"></textarea>
      <button onclick="publish()">Publish update</button>
    </div>
  </section>

  <script>
    function login() {
      const password =
        document.getElementById("password").value;

      if (password === "1234") {
        document.getElementById("editor").hidden = false;
        alert("Demo login successful");
      } else {
        alert("Incorrect password");
      }
    }

    function publish() {
      const title =
        document.getElementById("title").value;
      const message =
        document.getElementById("message").value;

      document.getElementById("shownTitle").textContent =
        title;
      document.getElementById("shownMessage").textContent =
        message;
    }
  </script>

</body>
</html>
