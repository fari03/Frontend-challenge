<!DOCTYPE html>
<html lang="en">

<head>
  <title>Profile Header Challenge</title>
  <link rel="stylesheet" type="text/css" href="style.css" />
</head>

<body>
  <div class="profile-header">
    <!-- Profile Information -->
    <div class="profile-info">
      <h1>John Doe</h1>
      <p>Web Developer</p>
    </div>

    <!-- Lock Icon -->
    <div class="lock-icon">
      <!-- SVG Logo from the "assets" folder -->
      <!-- Replace the content of this div with your lock SVG content -->
      <div>
        <!-- Example SVG -->
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="#9ca3af" stroke-width="2"
          stroke-linecap="round" stroke-linejoin="round">
          <rect x="3" y="11" width="18" height="11" rx="2" ry="2"></rect>
          <path d="M7 11V7a5 5 0 0 1 10 0v4"></path>
        </svg>
      </div>
    </div>
  </div>

  <h4>html css challenges!</h4>
</body>

</html>

//style.css


@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;700;600&display=swap");

body {
  font-family: "Inter", sans-serif;
  background-color: #f3f4f6;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.profile-header {
  display: flex;
  align-items: center;
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  padding: 20px;
}

.profile-info {
  margin-right: 20px;
}

.profile-info h1 {
  color: #111827;
  margin: 0;
}

.profile-info p {
  color: #9ca3af;
  margin: 0;
}

.lock-icon {
  /* Style your lock icon container as needed */
}
