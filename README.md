- <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Genius Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: #fff;
      text-align: center;
    }
    .container {
      max-width: 600px;
      margin: 50px auto;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    }
    h1, h2 {
      font-family: 'Courier New', Courier, monospace;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }
    h1 { font-size: 2.5em; }
    h2 { font-size: 2em; color: #ffdc73; }
    .logo img {
      width: 150px;
      margin-bottom: 20px;
    }
    .date-picker {
      margin: 20px 0;
    }
    .date-picker label {
      font-size: 1.2em;
      margin-right: 10px;
    }
    .date-picker input {
      padding: 10px;
      font-size: 1em;
      border-radius: 5px;
      border: none;
      outline: none;
    }
    .calculate-btn {
      background-color: #2575fc;
      color: #fff;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      font-size: 1.2em;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .calculate-btn:hover {
      background-color: #6a11cb;
    }
    .results {
      margin-top: 30px;
      font-size: 1.2em;
      background: rgba(0, 0, 0, 0.1);
      padding: 20px;
      border-radius: 5px;
      text-align: left;
    }
    .results p {
      margin: 10px 0;
    }
    .footer {
      margin-top: 20px;
      font-size: 0.9em;
      color: #ddd;
      text-align: center;
    }
    .footer a {
      color: #ffdc73;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
    }
    .footer img {
      width: 16px;
      margin-right: 5px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="logo">
      <img src="nt-world-crater-logo.png" alt="https://assets.onecompiler.app/4324mskhv/4324nc35q/IMG_20241205_090417-photoaidcom-cropped.jpg.png">
    </div>
    <h2>Genius Calculator</h2>
    <h1>Age Calculator</h1>
    <div class="date-picker">
      <label for="start-date">Start Date:</label>
      <input type="date" id="start-date">
    </div>
    <div class="date-picker">
      <label for="end-date">End Date:</label>
      <input type="date" id="end-date">
    </div>
    <button class="calculate-btn" onclick="calculateAge()">Calculate Age</button>
    <div class="results" id="results"></div>
  </div>
  <div class="footer">
    <p>Created by <strong>Nikhil Tripathi</strong></p>
    <p>
      <a href="mailto:nikhiltripathi0812@gmail.com">
        <img src="https://assets.onecompiler.app/4324mskhv/4324nc35q/IMG_20241205_090417-photoaidcom-cropped.jpg.png"> nikhiltripathi0812@gmail.com
      </a>
    </p>
  </div>

  <script>
    function calculateAge() {
      const startDate = new Date(document.getElementById('start-date').value);
      const endDate = new Date(document.getElementById('end-date').value);

      if (isNaN(startDate) || isNaN(endDate)) {
        alert("Please select valid dates.");
        return;
      }
      
      if (endDate < startDate) {
        alert("End date cannot be earlier than start date.");
        return;
      }

      // Calculate exact years, months, and days
      let years = endDate.getFullYear() - startDate.getFullYear();
      let months = endDate.getMonth() - startDate.getMonth();
      let days = endDate.getDate() - startDate.getDate();

      if (days < 0) {
        months--;
        days += new Date(endDate.getFullYear(), endDate.getMonth(), 0).getDate();
      }
      if (months < 0) {
        years--;
        months += 12;
      }

      // Total difference calculations
      const diffInMs = endDate - startDate;
      const totalSeconds = Math.floor(diffInMs / 1000);
      const totalMinutes = Math.floor(totalSeconds / 60);
      const totalHours = Math.floor(totalMinutes / 60);
      const totalDays = Math.floor(totalHours / 24);
      const totalWeeks = Math.floor(totalDays / 7);
      const totalMonths = Math.floor(totalDays / 30.44);
      const totalYears = Math.floor(totalDays / 365.25);

      // Update results
      const resultsDiv = document.getElementById('results');
      resultsDiv.innerHTML = `
        <p><strong>Exact Age:</strong> ${years} years, ${months} months, ${days} days</p>
        <p><strong>Years:</strong> ${totalYears}</p>
        <p><strong>Months:</strong> ${totalMonths}</p>
        <p><strong>Weeks:</strong> ${totalWeeks}</p>
        <p><strong>Days:</strong> ${totalDays}</p>
        <p><strong>Hours:</strong> ${totalHours}</p>
        <p><strong>Minutes:</strong> ${totalMinutes}</p>
        <p><strong>Seconds:</strong> ${totalSeconds}</p>
      `;
    }
  </script>
</body>
</html>
👋 Hi, I’m @NikhilGenius
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
NikhilGenius/NikhilGenius is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
