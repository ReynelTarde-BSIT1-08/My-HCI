<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fitness Tracker</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', sans-serif;
    background: #f4f6f8;
    color: #333;
}

#loader {
    position: fixed;
    width: 100%;
    height: 100vh;
    background: #264653;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999;
}

.loader-circle {
    width: 60px;
    height: 60px;
    border: 6px solid #fff;
    border-top: 6px solid #e76f51;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    100% { transform: rotate(360deg); }
}

nav {
    background: #2a9d8f;
    padding: 15px;
    text-align: center;
    position: sticky;
    top: 0;
}

nav a {
    color: white;
    margin: 0 15px;
    text-decoration: none;
    font-weight: bold;
    position: relative;
}

nav a::after {
    content: "";
    position: absolute;
    width: 0%;
    height: 2px;
    background: white;
    left: 0;
    bottom: -5px;
    transition: 0.3s;
}

nav a:hover::after {
    width: 100%;
}

header {
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
    url('https://images.unsplash.com/photo-1554284126-aa88f22d8b74') center/cover;
    color: white;
    padding: 120px 20px;
    text-align: center;
}

section {
    padding: 80px 20px;
    text-align: center;
}

.reveal {
    opacity: 0;
    transform: translateY(60px);
}

.reveal.active {
    opacity: 1;
    transform: translateY(0);
    transition: all 0.8s ease;
}

.card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 25px;
}

.card {
    background: white;
    padding: 20px;
    width: 260px;
    border-radius: 12px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.1);
    transition: 0.4s;
}

.card:hover {
    transform: translateY(-10px) scale(1.03);
    box-shadow: 0 12px 25px rgba(0,0,0,0.15);
}

.card img {
    width: 100%;
    border-radius: 10px;
}

button {
    background: #e76f51;
    border: none;
    padding: 10px 18px;
    color: white;
    border-radius: 6px;
    margin-top: 10px;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.05);
    background: #d65a3a;
}

form input,
form textarea {
    width: 100%;
    padding: 10px;
    margin-top: 10px;
    border-radius: 6px;
    border: 1px solid #ccc;
}

.contact-box {
    background: white;
    padding: 20px;
    max-width: 400px;
    margin: auto;
    border-radius: 10px;
    text-align: left;
}

footer {
    background: #264653;
    color: white;
    padding: 15px;
    margin-top: 40px;
}

@media (max-width: 768px) {
    .card {
        width: 90%;
    }
}
</style>
</head>

<body>

<div id="loader" style="display: none;">
    <div class="loader-circle"></div>
</div>

<nav>
    <a href="#home">Home</a>
    <a href="#workouts">Workouts</a>
    <a href="#nutrition">Nutrition</a>
    <a href="#progress">Progress</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
</nav>

<header id="home" class="reveal active">
    <h1>Fitness Tracker</h1>
    <p>Track your fitness journey 💪</p>
</header>

<section id="workouts" class="reveal active">
    <h2>Workouts</h2>
    <div class="card-container">

        <div class="card">
            <img src="https://images.unsplash.com/photo-1599058917765-a780eda07a3e">
            <h3>Cardio</h3>
            <button onclick="location.href='https://youtube.com'">View</button>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438">
            <h3>Strength</h3>
            <button onclick="location.href='https://youtube.com'">View</button>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1552196563-55cd4e45efb3">
            <h3>Yoga</h3>
            <button onclick="location.href='https://youtube.com'">View</button>
        </div>

    </div>
</section>

<section id="nutrition" class="reveal active">
    <h2>Nutrition</h2>
    <div class="card-container">

        <div class="card">
            <img src="https://images.unsplash.com/photo-1498837167922-ddd27525d352">
            <h3>Healthy Meals</h3>
        </div>

        <div class="card">
            <img src="https://i.pinimg.com/originals/7e/f0/79/7ef079d3f2a4b7f3e9601ebc17c44cb7.jpg">
            <h3>Protein Foods</h3>
        </div>

    </div>
</section>

<section id="progress" class="reveal active">
    <h2>Your Progress</h2>

    <div class="card" style="max-width:400px;margin:auto;">
        <form>
            <input type="number" placeholder="Weight (kg)">
            <input type="number" placeholder="Workout Duration (minutes)">
            <textarea placeholder="Notes"></textarea>
            <button type="submit">Save</button>
        </form>
    </div>
</section>

<section id="about" class="reveal active">
    <h2>About</h2>
    <p>Track your workouts, meals, and progress easily.</p>
</section>

<section id="contact" class="reveal active">
    <h2>Contact</h2>

    <div class="contact-box">

        <p><strong>Rio Geroy Flores</strong></p>
        <p>rige.flores.coc@phinmaed.com</p><br>

        <p><strong>Venice Belle Apor</strong></p>
        <p>velu.apor.coc@phinmaed.com</p><br>

        <p><strong>Tarde Reynel S.</strong></p>
        <p>resg.tarde.coc@phinmaed.com</p><br>

        <p><strong>Hadji Assim, Omair S.</strong></p>
        <p>omsi.hadjiassim.coc@phinmaed.com</p><br>

        <p><strong>Aaron Paul S. Terrado</strong></p>
        <p>aasa.terrado.coc@phinmaed.com</p><br>

        <p><strong>Yaz Alexander B. Lawansa</strong></p>
        <p>yaba.lawansa.coc@phinmaed.com</p><br>

        <p><strong>Pabualan, Phzyrah Keanne P.</strong></p>
        <p>phpa.pabualan.coc@phinmaed.com</p><br>

        <a href="https://www.facebook.com/rioninolouisse.flores.30.2.35/" target="_blank">
            Facebook Profile
        </a>

    </div>
</section>

<footer class="reveal">
    <p>© Fitness Tracker 💪</p>
</footer>

<script>
window.addEventListener("load", () => {
    document.getElementById("loader").style.display = "none";
});

function reveal() {
    const reveals = document.querySelectorAll(".reveal");

    reveals.forEach(el => {
        const windowHeight = window.innerHeight;
        const elementTop = el.getBoundingClientRect().top;

        if (elementTop < windowHeight - 100) {
            el.classList.add("active");
        }
    });
}

window.addEventListener("scroll", reveal);
reveal();
</script>

</body>
</html>
