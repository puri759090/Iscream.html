<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sweet Scoops 🍦</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", Arial, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #fff8f5;
    color: #442b2b;
    overflow-x: hidden;
}

/* NAVBAR */
nav {
    width: 100%;
    padding: 18px 7%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255,255,255,0.9);
    backdrop-filter: blur(10px);
    position: fixed;
    top: 0;
    z-index: 1000;
    box-shadow: 0 3px 15px rgba(0,0,0,0.06);
}

.logo {
    font-size: 27px;
    font-weight: 800;
    color: #e85d75;
}

.logo span {
    color: #ffb347;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 30px;
}

nav a {
    text-decoration: none;
    color: #442b2b;
    font-weight: 600;
    transition: 0.3s;
}

nav a:hover {
    color: #e85d75;
}

.order-btn {
    padding: 11px 22px;
    border-radius: 30px;
    background: #e85d75;
    color: white !important;
}

/* HERO */
.hero {
    min-height: 100vh;
    padding: 120px 7% 60px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 50px;
    background:
        radial-gradient(circle at 10% 20%, #ffd6e0 0 90px, transparent 91px),
        radial-gradient(circle at 90% 80%, #ffe1b5 0 110px, transparent 111px),
        #fff8f5;
}

.hero-text {
    max-width: 600px;
    animation: slideLeft 1s ease;
}

.badge {
    display: inline-block;
    background: #ffe0e8;
    color: #d84662;
    padding: 9px 18px;
    border-radius: 30px;
    margin-bottom: 20px;
    font-weight: 700;
}

.hero h1 {
    font-size: clamp(48px, 7vw, 82px);
    line-height: 1;
    margin-bottom: 25px;
}

.hero h1 span {
    color: #e85d75;
}

.hero p {
    font-size: 18px;
    line-height: 1.7;
    color: #765d5d;
    margin-bottom: 30px;
}

.hero-buttons {
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
}

.btn {
    text-decoration: none;
    padding: 15px 27px;
    border-radius: 35px;
    font-weight: 700;
    transition: 0.3s;
    display: inline-block;
}

.btn-primary {
    background: #e85d75;
    color: white;
    box-shadow: 0 10px 25px rgba(232,93,117,0.3);
}

.btn-primary:hover {
    transform: translateY(-4px);
}

.btn-secondary {
    border: 2px solid #e85d75;
    color: #e85d75;
}

.btn-secondary:hover {
    background: #e85d75;
    color: white;
}

/* HERO IMAGE */
.hero-image {
    width: 45%;
    display: flex;
    justify-content: center;
    position: relative;
    animation: float 4s ease-in-out infinite;
}

.hero-image img {
    width: min(480px, 100%);
    border-radius: 50%;
    object-fit: cover;
    aspect-ratio: 1;
    box-shadow: 0 25px 60px rgba(130,70,50,0.2);
    border: 12px solid white;
}

/* FLOATING ELEMENTS */
.float {
    position: absolute;
    font-size: 40px;
    animation: float 3s ease-in-out infinite;
}

.f1 {
    top: 5%;
    left: 5%;
}

.f2 {
    bottom: 10%;
    right: 0;
    animation-delay: 1s;
}

.f3 {
    top: 35%;
    right: -10%;
    animation-delay: 1.7s;
}

/* SECTION */
section {
    padding: 90px 7%;
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title h2 {
    font-size: 42px;
    margin-bottom: 10px;
}

.section-title span {
    color: #e85d75;
}

.section-title p {
    color: #806c6c;
}

/* CARDS */
.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
}

.card {
    background: white;
    border-radius: 25px;
    overflow: hidden;
    box-shadow: 0 10px 35px rgba(100,50,50,0.08);
    transition: 0.4s;
    position: relative;
}

.card:hover {
    transform: translateY(-12px) rotate(1deg);
    box-shadow: 0 20px 45px rgba(100,50,50,0.15);
}

.card-image {
    height: 260px;
    overflow: hidden;
}

.card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: 0.5s;
}

.card:hover img {
    transform: scale(1.1);
}

.card-content {
    padding: 25px;
}

.card-content h3 {
    font-size: 23px;
    margin-bottom: 8px;
}

.card-content p {
    color: #806c6c;
    margin-bottom: 15px;
}

.price {
    color: #e85d75;
    font-size: 22px;
    font-weight: 800;
}

.heart {
    position: absolute;
    right: 18px;
    top: 18px;
    background: white;
    width: 42px;
    height: 42px;
    border-radius: 50%;
    display: grid;
    place-items: center;
    font-size: 21px;
    box-shadow: 0 5px 15px rgba(0,0,0,.1);
}

/* ABOUT */
.about {
    background: #ffeef2;
    display: flex;
    align-items: center;
    gap: 60px;
}

.about-img {
    width: 45%;
}

.about-img img {
    width: 100%;
    border-radius: 30px;
    box-shadow: 0 20px 40px rgba(100,50,50,.15);
}

.about-text {
    flex: 1;
}

.about-text h2 {
    font-size: 45px;
    margin-bottom: 20px;
}

.about-text h2 span {
    color: #e85d75;
}

.about-text p {
    color: #765d5d;
    line-height: 1.8;
    margin-bottom: 25px;
}

/* CTA */
.cta {
    text-align: center;
    background: linear-gradient(135deg, #e85d75, #ff9b9b);
    color: white;
}

.cta h2 {
    font-size: 45px;
    margin-bottom: 15px;
}

.cta p {
    margin-bottom: 25px;
    font-size: 18px;
}

.cta .btn {
    background: white;
    color: #e85d75;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 30px;
    background: #3b2727;
    color: white;
}

footer span {
    color: #ff8fa3;
}

/* ANIMATIONS */
@keyframes float {
    0%,100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-18px);
    }
}

@keyframes slideLeft {
    from {
        opacity: 0;
        transform: translateX(-60px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

/* RESPONSIVE */
@media(max-width: 850px) {
    nav ul {
        display: none;
    }

    .hero {
        flex-direction: column;
        text-align: center;
        padding-top: 130px;
    }

    .hero-text {
        max-width: 700px;
    }

    .hero-buttons {
        justify-content: center;
    }

    .hero-image {
        width: 80%;
    }

    .cards {
        grid-template-columns: 1fr 1fr;
    }

    .about {
        flex-direction: column;
    }

    .about-img {
        width: 100%;
    }
}

@media(max-width: 550px) {
    .cards {
        grid-template-columns: 1fr;
    }

    .hero-image {
        width: 100%;
    }

    section {
        padding: 65px 5%;
    }

    .about-text h2,
    .cta h2 {
        font-size: 35px;
    }
}
</style>
</head>

<body>

<!-- NAVBAR -->
<nav>
    <div class="logo">Sweet<span>Scoops 🍦</span></div>

    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#flavors">Flavors</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>

    <a href="#flavors" class="order-btn">Order Now</a>
</nav>


<!-- HERO -->
<section class="hero" id="home">

    <div class="hero-text">
        <div class="badge">🍨 Freshly Made Every Day</div>

        <h1>
            Happiness<br>
            Comes in <span>Scoops!</span>
        </h1>

        <p>
            Discover delicious handcrafted ice creams made
            with love, fresh ingredients and lots of happiness.
        </p>

        <div class="hero-buttons">
            <a href="#flavors" class="btn btn-primary">Explore Flavors 🍦</a>
            <a href="#about" class="btn btn-secondary">Learn More</a>
        </div>
    </div>

    <div class="hero-image">

        <div class="float f1">🍓</div>
        <div class="float f2">🍫</div>
        <div class="float f3">🍒</div>

        <img
        src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?auto=format&fit=crop&w=900&q=90"
        alt="Delicious ice cream">
    </div>

</section>


<!-- FLAVORS -->
<section id="flavors">

    <div class="section-title">
        <h2>Our <span>Favorite</span> Flavors</h2>
        <p>Made fresh. Served cold. Loved by everyone.</p>
    </div>

    <div class="cards">

        <div class="card">
            <div class="heart">♡</div>

            <div class="card-image">
                <img
                src="https://images.unsplash.com/photo-1570197788417-0e82375c9371?auto=format&fit=crop&w=800&q=85"
                alt="Vanilla ice cream">
            </div>

            <div class="card-content">
                <h3>Vanilla Dream 🍦</h3>
                <p>Classic creamy vanilla with a smooth finish.</p>
                <div class="price">₹99</div>
            </div>
        </div>


        <div class="card">
            <div class="heart">♡</div>

            <div class="card-image">
                <img
                src="https://images.unsplash.com/photo-1551024506-0bccd828d307?auto=format&fit=crop&w=800&q=85"
                alt="Strawberry ice cream">
            </div>

            <div class="card-content">
                <h3>Strawberry Bliss 🍓</h3>
                <p>Sweet strawberries blended into creamy goodness.</p>
                <div class="price">₹129</div>
            </div>
        </div>


        <div class="card">
            <div class="heart">♡</div>

            <div class="card-image">
                <img
                src="https://images.unsplash.com/photo-1579954115545-a95591f28bfc?auto=format&fit=crop&w=800&q=85"
                alt="Chocolate ice cream">
            </div>

            <div class="card-content">
                <h3>Chocolate Heaven 🍫</h3>
                <p>Rich chocolate ice cream for true chocolate lovers.</p>
                <div class="price">₹149</div>
            </div>
        </div>


        <div class="card">
            <div class="heart">♡</div>

            <div class="card-image">
                <img
                src="https://images.unsplash.com/photo-1497034825429-c343d7c6a68f?auto=format&fit=crop&w=800&q=85"
                alt="Ice cream">
            </div>

            <div class="card-content">
                <h3>Berry Blast 🫐</h3>
                <p>A refreshing mix of delicious berries.</p>
                <div class="price">₹139</div>
            </div>
        </div>


        <div class="card">
            <div class="heart">♡</div>

            <div class="card-image">
                <img
                src="https://images.unsplash.com/photo-1501443762994-82bd5dace89a?auto=format&fit=crop&w=800&q=85"
                alt="Ice cream cone">
            </div>

            <div class="card-content">
                <h3>Caramel Crunch 🍯</h3>
                <p>Buttery caramel with crunchy sweet toppings.</p>
                <div class="price">₹159</div>
            </div>
        </div>


        <div class="card">
            <div class="heart">♡</div>

            <div class="card-image">
                <img
                src="https://images.unsplash.com/photo-1488900128323-21503983a07e?auto=format&fit=crop&w=800&q=85"
                alt="Ice cream sundae">
            </div>

            <div class="card-content">
                <h3>Rainbow Sundae 🌈</h3>
                <p>A colorful sundae packed with fun and flavor.</p>
                <div class="price">₹179</div>
            </div>
        </div>

    </div>
</section>


<!-- ABOUT -->
<section class="about" id="about">

    <div class="about-img">
        <img
        src="https://images.unsplash.com/photo-1497034825429-c343d7c6a68f?auto=format&fit=crop&w=1000&q=90"
        alt="Ice cream shop">
    </div>

    <div class="about-text">
        <h2>Made With <span>Love ❤️</span></h2>

        <p>
            At Sweet Scoops, every scoop is made with premium
            ingredients and a whole lot of love. From classic
            vanilla to exciting fruity flavors, there is something
            delicious waiting for everyone.
        </p>

        <a href="#contact" class="btn btn-primary">Visit Us 🍨</a>
    </div>

</section>


<!-- CTA -->
<section class="cta" id="contact">

    <h2>Ready for a Sweet Treat?</h2>

    <p>
        One scoop is never enough! Come and taste your favorite flavor today.
    </p>

    <a href="tel:+919999999999" class="btn">
        Order Your Ice Cream 🍦
    </a>

</section>


<!-- FOOTER -->
<footer>
    © 2026 <span>SweetScoops</span> · Made with ❤️ & 🍦
</footer>

</body>
</html>
