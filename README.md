<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Flexbox Layout</title>
  <style>
    /* Base Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      padding: 20px;
    }

    /* Navigation Bar */
    nav {
      background-color: #333;
      padding: 1rem;
    }

    nav ul {
      display: flex;
      list-style: none;
      justify-content: space-around;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    /* Layout Container */
    .container {
      display: flex;
      gap: 20px;
      margin-top: 20px;
    }

    .sidebar,
    .main-content {
      padding: 20px;
      background-color: #f4f4f4;
      border: 1px solid #ddd;
      border-radius: 8px;
    }

    .sidebar {
      flex: 1;
    }

    .main-content {
      flex: 3;
    }

    /* Media Queries */
    @media (max-width: 900px) {
      .container {
        flex-direction: column;
      }
    }

    @media (max-width: 600px) {
      nav ul {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <div class="container">
    <div class="sidebar">
      <h2>Sidebar</h2>
      <p>This is the sidebar content.</p>
    </div>
    <div class="main-content">
      <h2>Main Content</h2>
      <p>This is the main content area. Resize the browser window to see the layout adapt!</p>
    </div>
  </div>

</body>
</html>
