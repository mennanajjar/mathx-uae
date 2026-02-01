# mathx-uae
MathX UAE – Grade 11 Advanced
mathx-uae/
│
├── index.html        (الرئيسية)
├── unit1.html        (Unit 1)
├── quiz.html         (اختبار)
├── game.html         (لعبة)
│
├── css/
│   └── style.css
│
├── js/
│   └── app.js
│
└── assets/           (صور/أيقونات لاحقًا)<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>MathX UAE</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
  <h1>📘 MathX UAE</h1>
  <p>Grade 11 – Advanced | UAE Curriculum</p>
</header>

<nav>
  <a href="unit1.html">📚 Units</a>
  <a href="quiz.html">📝 Quiz</a>
  <a href="game.html">🎮 Game</a>
</nav>

<section class="card">
  <h2>👤 Student Progress</h2>
  <p>Points: <span id="points">0</span> ⭐</p>
</section>

<footer>
  <p>Designed by <b>Menna Najjar</b></p>
</footer>

<script src="js/app.js"></script>
</body>
</html><!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>Unit 1 - Functions</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
  <h1>Unit 1: Functions & Relations</h1>
</header>

<section class="card">
  <p><b>Function (دالة):</b> علاقة تربط كل عنصر من المجال بعنصر واحد فقط من المدى.</p>

  <ul>
    <li>Domain – المجال</li>
    <li>Range – المدى</li>
  </ul>

  <button onclick="addPoints()">✔ Complete Lesson</button>
</section>

<footer>
  <p>MathX UAE • Menna Najjar</p>
</footer>

<script src="js/app.js"></script>
</body>
</html><!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>Unit 1 - Functions</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
  <h1>Unit 1: Functions & Relations</h1>
</header>

<section class="card">
  <p><b>Function (دالة):</b> علاقة تربط كل عنصر من المجال بعنصر واحد فقط من المدى.</p>

  <ul>
    <li>Domain – المجال</li>
    <li>Range – المدى</li>
  </ul>

  <button onclick="addPoints()">✔ Complete Lesson</button>
</section>

<footer>
  <p>MathX UAE • Menna Najjar</p>
</footer>

<script src="js/app.js"></script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Unit 1 Quiz</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
  <h1>📝 Unit 1 Quiz</h1>
</header>

<section class="card">
  <p>Which relation is a function?</p>

  <button onclick="correct()">Each input has one output</button>
  <button onclick="wrong()">One input has multiple outputs</button>

  <p id="result"></p>
</section>

<footer>
  <p>Designed by Menna Najjar</p>
</footer>

<script src="js/app.js"></script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Math Game</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
  <h1>🎮 Math Challenge</h1>
</header>

<section class="card">
  <p>If f(x)=2x, what is f(3)?</p>

  <button onclick="correct()">6</button>
  <button onclick="wrong()">5</button>

  <p id="result"></p>
</section>

<footer>
  <p>MathX UAE • Menna Najjar</p>
</footer>

<script src="js/app.js"></script>
</body>
</html>let points = localStorage.getItem("points") || 0;

document.getElementById("points")?.innerText = points;

function addPoints() {
  points = parseInt(points) + 10;
  localStorage.setItem("points", points);
  alert("🎉 Lesson completed! +10 points");
}

function correct() {
  points = parseInt(points) + 5;
  localStorage.setItem("points", points);
  document.getElementById("result").innerText =
    "✔ Correct! +5 points";
}

function wrong() {
  document.getElementById("result").innerText =
    "❌ Try again";
}body {
  margin: 0;
  font-family: "Segoe UI", Arial;
  background: #f2f4f8;
  text-align: center;
}

header {
  background: #1e3a8a;
  color: white;
  padding: 20px;
}

nav {
  margin: 20px;
}

nav a {
  margin: 10px;
  padding: 12px 18px;
  background: #2563eb;
  color: white;
  text-decoration: none;
  border-radius: 10px;
  font-weight: bold;
}

.card {
  background: white;
  margin: 30px auto;
  padding: 25px;
  width: 85%;
  max-width: 500px;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

button {
  padding: 10px 18px;
  margin: 10px;
  border: none;
  border-radius: 8px;
  background: #16a34a;
  color: white;
  font-size: 15px;
  cursor: pointer;
}

footer {
  margin-top: 40px;
  padding: 15px;
  color: #555;
}
