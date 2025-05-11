
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Colorful Wonderful Hotel</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffe259, #ffa751);
      color: #333;
      line-height: 1.6;
    }

    header {
      background: linear-gradient(to right, #00c9ff, #92fe9d);
      color: white;
      padding: 20px 0;
      text-align: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }
    header h1 {
      font-size: 2.5rem;
      text-shadow: 2px 2px #333;
    }

    nav ul {
      list-style: none;
      margin-top: 10px;
    }

    nav ul li {
      display: inline;
      margin: 0 15px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      font-size: 18px;
    }

    nav ul li a:hover {
      color: #ffeb3b;
      text-decoration: underline;
    }

    section {
      padding: 60px 20px;
    }

    .container {
      max-width: 1100px;
      margin: auto;
    }

    #home {
      background: url('https://via.placeholder.com/1600x600/ff6a00/ffffff?text=Welcome+to+Wonderful+Hotel') no-repeat center center/cover;
      color: white;
      text-align: center;
      padding: 100px 20px;
    }

    #home h2 {
      font-size: 3rem;
      margin-bottom: 15px;
      text-shadow: 2px 2px #222;
    }

    #home p {
      font-size: 20px;
    }

    h2 {
      text-align: center;
      margin-bottom: 30px;
      color: #333;
      font-size: 2rem;
    }

    p, li {
      font-size: 18px;
      color: #555;
    }

    #services ul {
      text-align: center;
      list-style: none;
    }

    #services ul li {
      background: linear-gradient(to right, #ff758c, #ff7eb3);
      margin: 10px auto;
      padding: 10px;
      max-width: 400px;
      border-radius: 12px;
      color: white;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }

    #booking-form {
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      max-width: 500px;
      margin: auto;
    }

    #booking-form input, #booking-form button {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      font-size: 16px;
      border-radius: 6px;
      border: 1px solid #ccc;
    }

    #booking-form input:focus {
      border-color: #ff4081;
      outline: none;
    }

    button {
      background-color: #ff4081;
      color: white;
      font-weight: bold;
      border: none;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #e91e63;
    }

    #booking-history {
      background-color: #fff3e0;
      padding: 20px;
      border-radius: 10px;
      margin-top: 40px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    table {
      width: 100%;
      border-collapse: collapse;
    }

    table th, table td {
      padding: 10px;
      border-bottom: 1px solid #ccc;
      text-align: left;
    }

    table th {
      background: #ff9800;
      color: white;
    }

    footer {
      background: linear-gradient(to right, #4facfe, #00f2fe);
      color: white;
      text-align: center;
      padding: 15px;
      font-weight: bold;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Wonderful Hotel</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#booking">Booking</a></li>
        <li><a href="#history">History</a></li>
      </ul>
    </nav>
  </header>

  <section id="home">
    <div class="container">
      <h2>Welcome to Wonderful Hotel</h2>
      <p>Experience a colorful stay with unforgettable memories</p>
    </div>
  </section>

  <section id="about">
    <div class="container">
      <h2>About Us</h2>
      <p>Welcome to Wonderful Hotel – your colorful gateway to comfort, luxury, and joy. We pride ourselves in making every stay vibrant and delightful.</p>
    </div>
  </section>

  <section id="services">
    <div class="container">
      <h2>Our Services</h2>
      <ul>
        <li>✨ 24/7 Room Service</li>
        <li>📶 Free Wi-Fi</li>
        <li>💆 Luxury Spa</li>
        <li>🍽️ Restaurant & Bar</li>
        <li>🏢 Conference Room</li>
        <li>🏊 Swimming Pool</li>
      </ul>
    </div>
  </section>

  <section id="booking">
    <div class="container">
      <h2>Book Your Room</h2>
      <form id="booking-form">
        <input type="text" id="name" placeholder="Your Name" required>
        <input type="date" id="check-in" required>
        <input type="date" id="check-out" required>
        <button type="submit">Book Now</button>
      </form>
    </div>
  </section>

  <section id="history">
    <div class="container">
      <h2>Booking History</h2>
      <div id="booking-history">
        <table>
          <thead>
            <tr>
              <th>Name</th>
              <th>Check-in</th>
              <th>Check-out</th>
            </tr>
          </thead>
          <tbody id="history-table-body">
            <!-- History will be loaded here -->
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <footer>
    &copy; 2025 Wonderful Hotel. Stay Colorful!
  </footer>

  <script>
    // Handle form submission
    document.getElementById('booking-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('name').value;
      const checkIn = document.getElementById('check-in').value;
      const checkOut = document.getElementById('check-out').value;

      if (name && checkIn && checkOut) {
        let bookings = JSON.parse(localStorage.getItem('bookings')) || [];
        bookings.push({ name, checkIn, checkOut });
        localStorage.setItem('bookings', JSON.stringify(bookings));

        alert(`🎉 Booking confirmed for ${name}!`);
        document.getElementById('booking-form').reset();
        loadHistory();
      } else {
        alert("Please fill in all fields!");
      }
    });

    // Load booking history
    function loadHistory() {
      const bookings = JSON.parse(localStorage.getItem('bookings')) || [];
      const tbody = document.getElementById('history-table-body');
      tbody.innerHTML = '';
      bookings.forEach(booking => {
        const row = `<tr>
          <td>${booking.name}</td>
          <td>${booking.checkIn}</td>
          <td>${booking.checkOut}</td>
        </tr>`;
        tbody.innerHTML += row;
      });
    }

    window.onload = loadHistory;
  </script>

</body>
</html>
