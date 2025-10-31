<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css">
    <title>My Anime List</title>
    <style>
        
.navbar{
    width: 100%;
    height: 50px;
    background-color: mediumslateblue;
}

.navbar-container{
    display: flex;
    align-items: center;
    background-color: mediumslateblue;
    height: 100%;
    color: white;
}

.profile-container {
      position: relative;
      display: inline-block;
    }

    /* Hide the checkbox */
    #toggle {
      display: none;
    }

    /* Profile icon */
    .profile-label {
      margin-left: -50px;
      width: 40px;
      height: 40px;
      background-color: #ccc;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      font-weight: bold;
    }

    /* Settings panel */
    .settings {
      display: none;
      position: absolute;
      margin-left: -180px;
      top: 50px;
      left: 0;
      background: #f9f9f9;
      border: 1px solid #ddd;
      padding: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
      width: 150px;
    }

    /* Show settings when checkbox is checked */
    #toggle:checked + .profile-label + .settings {
      display: block;
    }

    .settings a {
      display: block;
      margin: 5px 0;
      color: #333;
      text-decoration: none;
    }

    .settings a:hover {
      text-decoration: underline;
    }
 
    .profile {
  width: 200px;
  font-family: sans-serif;
}


.profile-picture{
    
    width: 32px;
    height: 32px;
    border-radius: 50%;
    object-fit: cover;
}
   
.profile {
  width: 200px;
  font-family: sans-serif;
}

.logo-container{
    flex: 7;
    font-size: 30px;
    margin-left: -200px;
}

.logo{
    font-family: 'sen', Georgia, 'Times New Roman', Times, serif;
}

.not-container{
    flex: 1;
}

.notification-wrapper {
      position: relative;
      display: inline-block;
    }

    #notification-icon {
      font-size: 24px;
      color: white;
      background: none;
      border: none;
      margin-top: -5px;
      cursor: pointer;
      z-index: 101;
      position: relative;
    }

    #notification-panel {
      position: fixed;
      top: 0;
      left: -250px;
      height: 100vh;
      width: 220px;
      margin-top: 50px;
      color: #000;
      background: white;
      border-right: 1px solid #ccc;
      box-shadow: 2px 0 8px rgba(0,0,0,0.2);
      padding: 20px;
      transition: left 0.3s ease-out;
      z-index: 100;
    }

    #notification-panel.show {
      left: 0;
    }
.not-picture{
   margin-left: 20px;
}

.not-icon{
   font-size: 20px;
}

.navbar-ul{
    width: 100%;
    height: 50px;
    overflow: hidden;
    position: fixed;
    bottom: 0;
    background-color: aliceblue;
}

.navbar-ul-container{
    display: flex;
    align-items: center;
    color: black;
    justify-content: space-evenly;
    width: 100%;
}

.icon {
  color: white;
  font-size: 24px;
  margin: 0 15px;
  cursor: pointer;
}

.menu-icon{
    margin: 5px;
    font-size: 20px;
    margin-right: 95px;
    cursor: pointer;
}

.menu-icon-1{
    font-size: 20px;
    margin-left: 9px;
}

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}


.page {
  display: none;
  padding: 15px;
  text-align: center;
  color: #000;
  font-size: medium;
  background-color: #bbb9b9;
  margin-bottom: -50px;
  top: 200px;
}

.page.active {
  display: block;
}


/* Search box layout */
.search-container {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

/* Input styling */
.search-input {
  padding: 10px;
  font-size: 16px;
  width: 250px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

/* Button styling */
.search-button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #0078D4;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.search-button:hover {
  background-color: #005A9E;
}

/* Result message */
.result-message {
  font-size: 18px;
 margin-left: -20px;
  text-align: center;
}

.club{
  font-size: larger;
  font-weight: bold;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
margin-left: -1300px;
}

.horizontal-line {
  width: 100%;
  height: 1px;
  background-color: black;
  padding-top: 5px;
  margin-top: 10px;
  margin-bottom: -40px;
}

.navbar1-container{
  display: flex;
  align-items: center;

}

.nav {
  display: flex;
  gap: 400px;
  margin-bottom: 10px;
  font-weight: bold;
  cursor: pointer;
}

.page {
  display: none;
  animation: fadeIn 0.3s ease;
}

.page.active {
  display: block;
}

button {
  margin-top: 20px;
  padding: 8px 12px;
  cursor: pointer;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

.last-icon{
  size: 30px;
  margin-right: -1400px;
  padding-top: -20px;
  font-size: larger;
}

   body {
      margin: 0;
      font-family: sans-serif;
    }

    .top-left {
      position: absolute;
      top: 10px;
      
    }

    .dropdown {
      position: relative;
    }

    .toggle {
      display: inline-block;
      padding: 10px 15px;
      background-color: #3498db;
      color: white;
      font-size: 20px;
      border-radius: 4px;
      cursor: pointer;
      margin-top: 120px;
    }

    #menu-toggle {
      display: none;
    }

    .dropdown-menu {
      display: none;
      position: absolute;
      top: 45px;
      left: 0;
      margin-bottom: -200px;
      margin-top: 120px;
      background-color: white;
      border: 1px solid #ccc;
      border-radius: 4px;
      padding: 5px 0;
      width: 150px;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
    }

    #menu-toggle:checked + .toggle + .dropdown-menu {
      display: block;
    }

    .dropdown-menu label {
      display: block;
      padding: 10px 15px;
      cursor: pointer;
    }

    .dropdown-menu label:hover {
      background-color: #f0f0f0;
    }

    .dropdown-menu input[type="radio"] {
      margin-right: 8px;
    }

    
.nav-1{
  display: flex;
  gap: 200px;
  margin-bottom: -20px;
  font-weight: bold;
  cursor: pointer;
}

    .section {
      align-items: center;
      display: none;
      margin-top: 100px;
      text-align: center;
    }

    .section:target {
      display: block;
    }

    .menu {
      display: block;
    }

  .option-link {
    text-align: left;
      direction: ltr;
      padding: 90px;
      width: 300px;
      color: #000;

}


    </style>
</head>
<body>
    <div class="navbar">
        <div class="navbar-container">
             <div class="not-container">
                <div class="not-picture">
                    <div class="notification-wrapper">
                      <button id="notification-icon" class="not-icon fa-solid fa-bell"></button>
                      <div id="notification-panel">
                        <h4>Notifications</h4>
                        <p>No new notifications</p>
                      </div>
                    </div>

                </div>
            </div>
            <div class="logo-container"><center><h1 class="logo">Mal</h1></center></div>
            <div class="profile-container">
              <input type="checkbox" id="toggle">
              <label for="toggle" class="profile-label">👤</label>
              <div class="settings">
                <a href="#">Profile</a>
                <a href="#">Settings</a>
                <a href="#">Logout</a>
              </div>
            </div>
                </div>
            </div>
        </div>
    </div>
    <div class="navbar-ul">
        <div class="navbar-ul-container">
            <div class="home-container">
                <div class="home-text-container">
                   <i class="menu-icon fa-solid fa-house" onclick="navigate('home')"></i>
                   <i class="menu-icon fa-solid fa-comments"  onclick="navigate('discuss')"></i>
                   <i class="menu-icon fa-solid fa-magnifying-glass"  onclick="navigate('search')"></i>
                   <i class="menu-icon fa-solid fa-calendar"  onclick="navigate('calendar')"></i>
                   <i class="menu-icon-1 fa-solid fa-bars"  onclick="navigate('bars')"></i>
                </div>
            </div>
        </div> 
    </div>
  <div id="content">
    <div id="home" class="page active">Welcome to the Home Page!</div>
    <div id="discuss" class="page">
        <div class="search-container">
             <input type="text" id="searchInput" placeholder="Find Clubs..." class="search-input">
             <button onclick="handleSearch()" class="search-button">Go</button>
        </div>
          <div class="club">My Clubs</div>
          <div class="horizontal-line"></div>
        <p id="resultMessage" class="result-message"></p>
    </div>
    <div id="search" class="page">
       <div class="search-container">
             <input type="text" id="searchInput" placeholder="Search..." class="search-input">
             <button onclick="handleSearch()" class="search-button">Go</button>
        </div>
        <p id="resultMessage" class="result-message"></p>
    </div>
    <div id="calendar" class="page">   
        <div class="nav">
            <span onclick="showPage('last')">Last</span>
            <span onclick="showPage('thisseason')">This Season</span>
            <span onclick="showPage('next')">Next</span>
            <span onclick="showPage('archive')">Archive</span>
        </div>
      
    </div>
    <div id="last" class="page">
      <button onclick="goBack()">← Back</button>
      <p>This contains the series from the Last Season.</p>
    </div>
    <div id="thisseason" class="page">
      <button onclick="goBack()">← Back</button>
     <p>This contains the series from the Current Season.</p>
    </div>
    <div id="next" class="page">
      <button onclick="goBack()">← Back</button>
     <p>This contains the series from the next Season.</p>
    </div>
    <div id="archive" class="page">
      <button onclick="goBack()">← Back</button>
     <p>This contains the series as yearwise.</p>
    </div>
    <div id="bars" class="page">
      <div class="menu" id="home">
        <a href="#option1" class="option-link">All</a>
        <a href="#option2" class="option-link">Watching</a>
        <a href="#option3" class="option-link">Completed</a>
        <a href="#option4" class="option-link">On Hold</a>
        <a href="#option5" class="option-link">Dropped</a>
        <a href="#option6" class="option-link">Plan to Watch</a>
      </div>
    </div>
    <div class="section" id="option1">
     <h2>ALL</h2>
     <p>This contains all the concept.</p>
     <a href="#home">Back</a>
    </div>

    <div class="section" id="option2">
      <h2>WATCHING</h2>
      <p>This shows the series which you are watching currently.</p>
      <a href="#home">Back</a>
    </div>
    <div class="section" id="option3">
      <h2>COMPLETED</h2>
      <p>This shows what you already watched.</p>
      <a href="#home">Back</a>
    </div>
    <div class="section" id="option4">
      <h2>ON HOLD</h2>
      <p>This shows series which are temperorily stopped.</p>
      <a href="#home">Back</a>
    </div>
    <div class="section" id="option5">
      <h2>DROPPED</h2>
      <p>This shows series which have been dropped.</p>
      <a href="#home">Back</a>
    </div>
    <div class="section" id="option6">
      <h2>PLANNING TO WATCH</h2>
      <p>This shows what you are planning to watch.</p>
      <a href="#home">Back</a>
    </div>

</div>
  <script>
    function navigate(pageId) {
  const pages = document.querySelectorAll('.page');
  pages.forEach(page => {
    page.classList.remove('active');
  });

  const targetPage = document.getElementById(pageId);
  if (targetPage) {
    targetPage.classList.add('active');
  }
}

function handleSearch() {
  const input = document.getElementById("searchInput").value.trim();
  const result = document.getElementById("resultMessage");

  if (input === "") {
    result.textContent = "Please enter a search term.";
    result.style.color = "red";
  } else {
    result.textContent = `You searched for: "${input}"`;
   

    // Optional: redirect to another page
    // window.location.href = `results.html?q=${encodeURIComponent(input)}`;
  }
}

  // Optional: Trigger search on Enter key
  document.getElementById("searchInput").addEventListener("keypress", function(event) {
    if (event.key === "Enter") {
      handleSearch();
    }
  });

let lastPage1= 'calendar';

function showPage(pageId) {
  document.querySelectorAll('.page').forEach(page => {
    page.classList.remove('active');
  });
  document.getElementById(pageId).classList.add('active');
  lastPage1 = pageId !== 'calendar' ? 'calendar' : lastPage1;
}

function goBack() {
  showPage(lastPage1);
}

const icon = document.getElementById('notification-icon');
    const panel = document.getElementById('notification-panel');

    icon.addEventListener('click', (e) => {
      e.stopPropagation(); // Prevent click from bubbling to document
      panel.classList.toggle('show');
    });

    document.addEventListener('click', (e) => {
      if (!panel.contains(e.target) && !icon.contains(e.target)) {
        panel.classList.remove('show');
      }
    });
  </script>
</body>
</html>
