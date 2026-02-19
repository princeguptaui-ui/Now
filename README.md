<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Prince Travel Blog</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Orbitron',sans-serif;
    scroll-behavior:smooth;
}

body{
    background:#0a0a0f;
    color:white;
    overflow-x:hidden;
}

/* LOADER */
#loader{
    position:fixed;
    width:100%;
    height:100%;
    background:black;
    display:flex;
    justify-content:center;
    align-items:center;
    z-index:9999;
    color:#00f0ff;
    font-size:28px;
    animation:fadeOut 2.5s forwards 2s;
}

@keyframes fadeOut{
    to{opacity:0; visibility:hidden;}
}

/* STARS */
.stars{
    position:fixed;
    width:100%;
    height:100%;
    background:url('https://www.transparenttextures.com/patterns/stardust.png');
    animation:moveStars 60s linear infinite;
    z-index:-1;
}

@keyframes moveStars{
    from{background-position:0 0;}
    to{background-position:1000px 1000px;}
}

/* NAVBAR */
nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    padding:20px 60px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    background:rgba(0,0,0,0.85);
    backdrop-filter:blur(12px);
    z-index:1000;
    transition:0.4s ease;
}

nav.scrolled{
    padding:12px 60px;
    background:rgba(0,0,0,0.95);
    box-shadow:0 5px 20px rgba(0,255,255,0.4);
}

nav a{
    color:#00f0ff;
    text-decoration:none;
    margin-left:25px;
    transition:0.3s;
}

nav a:hover{
    color:#ff00ff;
}

/* HERO */
.hero{
    margin-top:90px;
    height:100vh;
    background:url('https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    position:relative;
}

.hero::after{
    content:"";
    position:absolute;
    width:100%;
    height:100%;
    background:rgba(0,0,0,0.6);
}

.hero-content{
    position:relative;
    z-index:2;
}

.hero h1{
    font-size:60px;
    color:#00f0ff;
    text-shadow:0 0 20px #00f0ff;
}

.hero p{
    font-size:25px;
    margin:20px 0;
    color:#ff00ff;
}

.hero button{
    padding:15px 40px;
    border:none;
    border-radius:30px;
    background:linear-gradient(45deg,#00f0ff,#ff00ff);
    cursor:pointer;
    font-size:18px;
}

/* ROCKET */
.rocket{
    position:fixed;
    width:80px;
    bottom:-100px;
    animation:flyRocket 18s linear infinite;
}

@keyframes flyRocket{
    0%{left:-100px; bottom:-100px;}
    50%{left:50%; bottom:80%;}
    100%{left:120%; bottom:-100px;}
}

/* PLACES */
.places{
    padding:100px 40px;
    text-align:center;
}

.places h2{
    font-size:40px;
    margin-bottom:50px;
    color:#00f0ff;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:#111;
    border-radius:15px;
    overflow:hidden;
    transition:0.4s;
}

.card:hover{
    transform:scale(1.05);
    box-shadow:0 0 20px #00f0ff;
}

.card img{
    width:100%;
    height:200px;
    object-fit:cover;
    display:block;
}

.card h3{
    padding:15px;
}

/* FOOTER */
footer{
    padding:60px 20px;
    text-align:center;
    background:black;
}

.profile-img, .school-img{
    width:120px;
    height:120px;
    border-radius:50%;
    object-fit:cover;
    margin:20px;
    border:3px solid #00f0ff;
}
</style>
</head>

<body>

<div id="loader">Loading Prince Travel Blog...</div>
<div class="stars"></div>

<img class="rocket" src="https://cdn-icons-png.flaticon.com/512/3212/3212608.png">

<nav>
<div>🌍 Prince Travel Blog</div>
<div>
<a href="#">Home</a>
<a href="#places">Places</a>
<a href="#about">About</a>
</div>
</nav>

<header class="hero">
<div class="hero-content">
<h1>TRAVELLING BLOG</h1>
<p>✨ Beautiful Places on Earth ✨</p>
<button onclick="document.getElementById('places').scrollIntoView()">Explore Now</button>
</div>
</header>

<section class="places" id="places">
<h2>12 Beautiful Travel Destinations</h2>

<div class="grid">
<div class="card"><img src="https://images.unsplash.com/photo-1502602898657-3e91760cbb34?auto=format&fit=crop&w=800&q=80"><h3>Paris</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1512453979798-5ea266f8880c?auto=format&fit=crop&w=800&q=80"><h3>Dubai</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1528909514045-2fa4ac7a08ba?auto=format&fit=crop&w=800&q=80"><h3>London</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1533929736458-ca588d08c8be?auto=format&fit=crop&w=800&q=80"><h3>Rome</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1599661046289-e31897846e41?auto=format&fit=crop&w=800&q=80"><h3>Jaipur - Hawa Mahal</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=crop&w=800&q=80"><h3>New York</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=80"><h3>Maldives</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1549692520-acc6669e2f0c?auto=format&fit=crop&w=800&q=80"><h3>Tokyo</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=800&q=80"><h3>Switzerland</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=800&q=80"><h3>Canada</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=800&q=80"><h3>Australia</h3></div>
<div class="card"><img src="https://images.unsplash.com/photo-1483721310020-03333e577078?auto=format&fit=crop&w=800&q=80"><h3>Singapore</h3></div>
</div>
</section>

<footer id="about">
<h2>About Me</h2>

<img class="profile-img" src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=400&q=80">
<img class="school-img" src="https://images.unsplash.com/photo-1588072432836-e10032774350?auto=format&fit=crop&w=400&q=80">

<p>Hi, I'm <strong>Prince</strong> from Class 9th.</p>
<p>Pride International School, Narkatiaganj</p>
<p>🚀 Future Aeronautical Engineer</p>
<p>🏛 Future IAS Officer</p>

</footer>

<script>
window.addEventListener("scroll", function(){
    let nav = document.querySelector("nav");
    if(window.scrollY > 50){
        nav.classList.add("scrolled");
    } else {
        nav.classList.remove("scrolled");
    }
});
</script>

</body>
</html>
