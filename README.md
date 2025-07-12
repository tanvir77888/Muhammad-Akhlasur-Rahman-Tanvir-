<style>
/* হেডার সেকশন */
.header-section {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px;
    background-color: #f8f8f8;
    border-bottom: 1px solid #eee;
}

.logo img {
    height: 40px; /* লোগোর উচ্চতা */
}

.auth-buttons button {
    background-color: #333;
    color: white;
    padding: 8px 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-left: 10px;
}

.auth-buttons button:hover {
    background-color: #555;
}

/* স্লাইডারের জন্য CSS */
.slider-container {
    width: 100%;
    overflow: hidden;
    position: relative;
    max-width: 900px; /* আপনার প্রয়োজন অনুযায়ী প্রস্থ সেট করুন */
    margin: 0 auto 20px auto;
}

.image-slider {
    display: flex;
    transition: transform 0.5s ease-in-out;
}

.image-slider img {
    width: 100%;
    flex-shrink: 0;
    height: auto; /* Maintains aspect ratio */
    display: block;
}

.slider-dots {
    text-align: center;
    padding: 10px 0;
}

.dot {
    height: 10px;
    width: 10px;
    margin: 0 5px;
    background-color: #bbb;
    border-radius: 50%;
    display: inline-block;
    cursor: pointer;
    transition: background-color 0.6s ease;
}

.dot.active {
    background-color: #717171;
}

/* অর্ডার আইটেম গ্যালারি */
.image-gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 15px; /* ছবির মধ্যে ফাঁকা স্থান */
    justify-content: center;
    padding: 15px;
}

.gallery-item {
    flex: 1 1 calc(50% - 30px); /* 2 কলামের জন্য, প্যাডিং বাদ দিয়ে */
    box-sizing: border-box;
    text-align: center;
    border: 1px solid #eee;
    padding: 10px;
    border-radius: 5px;
    transition: transform 0.2s;
    max-width: 300px; /* প্রতিটি আইটেমের সর্বোচ্চ প্রস্থ */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    position: relative; /* For stock out badge */
}

@media (min-width: 768px) {
    .gallery-item {
        flex: 1 1 calc(33.333% - 30px); /* 3 কলামের জন্য */
    }
}

.gallery-item:hover {
    transform: translateY(-5px);
}

.gallery-item h3 {
    margin: 0 0 5px 0;
    font-size: 1.1em;
    color: #333;
    font-weight: normal;
}

.gallery-item p {
    font-size: 1.1em;
    font-weight: bold;
    color: #007bff;
    margin-bottom: 10px;
}

.order-btn {
    background-color: #28a745;
    color: white;
    padding: 8px 15px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.2s;
    width: 100%;
    box-sizing: border-box;
}

.order-btn:hover {
    background-color: #218838;
}

.stock-out-badge {
    background-color: #dc3545; /* Red color */
    color: white;
    padding: 3px 8px;
    border-radius: 3px;
    font-size: 0.8em;
    font-weight: bold;
    position: absolute;
    top: 5px;
    right: 5px;
    z-index: 10;
}

/* ফুটার বাটন */
.footer-buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    background-color: #f8f8f8;
    border-top: 1px solid #eee;
    margin-top: 30px;
}

.support-btn {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    margin-right: 15px;
}

.support-btn:hover {
    background-color: #0056b3;
}

.whatsapp-icon {
    font-size: 2em; /* আইকনের আকার */
    color: #25D366; /* WhatsApp সবুজ */
    text-decoration: none;
}
</style>

<div class="header-section">
    <div class="logo">
        <img src="https://via.placeholder.com/100x40?text=Your+Logo" alt="Your Logo"> </div>
    <div class="auth-buttons">
        <button>LOGIN</button>
        <button>REGISTER</button>
    </div>
</div>

<div class="slider-container">
    <div class="image-slider" id="mainSlider">
        <img src="https://via.placeholder.com/900x300?text=Slider+Image+1" alt="Slider Image 1">
        <img src="https://via.placeholder.com/900x300?text=Slider+Image+2" alt="Slider Image 2">
        <img src="https://via.placeholder.com/900x300?text=Slider+Image+3" alt="Slider Image 3">
    </div>
    <div class="slider-dots" id="sliderDots"></div>
</div>

<hr> <h2>আপনার পছন্দের টপ-আপ নির্বাচন করুন</h2>

<div class="image-gallery">
    <div class="gallery-item" data-price="21" data-item="25 Dimond">
        <h3>25 Dimond</h3>
        <p>BDT 21</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="152" data-item="240 Diamond">
        <h3>240 Diamond</h3>
        <p>BDT 152</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="385" data-item="610 Dimond">
        <h3>610 Dimond</h3>
        <p>BDT 385</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="35" data-item="50 Dimond">
        <h3>50 Dimond</h3>
        <p>BDT 35</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="77" data-item="115 Dimond">
        <h3>115 Dimond</h3>
        <p>BDT 77</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="770" data-item="1240 Dimond">
        <h3>1240 Dimond</h3>
        <p>BDT 770</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="1540" data-item="2530 Dimond">
        <h3>2530 Dimond</h3>
        <p>BDT 1540</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="153" data-item="Weekly">
        <h3>Weekly</h3>
        <p>BDT 153</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="760" data-item="Monthly">
        <h3>Monthly</h3>
        <p>BDT 760</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="40" data-item="Weekly lite">
        <h3>Weekly lite</h3>
        <p>BDT 40</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="153" data-item="Level Up Pass">
        <span class="stock-out-badge">STOCK OUT</span>
        <h3>Level Up Pass</h3>
        <p>BDT 153</p>
        <button class="order-btn" disabled style="background-color: #6c757d; cursor: not-allowed;">স্টক আউট</button>
    </div>

    <div class="gallery-item" data-price="40" data-item="level up pass level- 6">
        <h3>level up pass level- 6</h3>
        <p>BDT 40</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="65" data-item="level up pass level- 10">
        <h3>level up pass level- 10</h3>
        <p>BDT 65</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="65" data-item="level up pass level- 15">
        <h3>level up pass level- 15</h3>
        <p>BDT 65</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="65" data-item="level up pass level- 20">
        <h3>level up pass level- 20</h3>
        <p>BDT 65</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="65" data-item="level up pass level- 25">
        <h3>level up pass level- 25</h3>
        <p>BDT 65</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="90" data-item="level up pass level- 30">
        <h3>level up pass level- 30</h3>
        <p>BDT 90</p>
        <button class="order-btn">Order Now</button>
    </div>

    <div class="gallery-item" data-price="370" data-item="level up pass full">
        <h3>level up pass full</h3>
        <p>BDT 370</p>
        <button class="order-btn">Order Now</button>
    </div>
</div>

<p style="text-align: center; margin-top: 20px; font-size: 1.1em;">
    <a href="#" style="color: #e83e8c; text-decoration: none; font-weight: bold;">কিভাবে অর্ডার করবেন?</a>
</p>

<div class="footer-buttons">
    <button class="support-btn">SUPPORT!</button>
    <a href="https://wa.me/8801403520600" class="whatsapp-icon" target="_blank">&#x1F4DE;</a> </div>

<script>
// স্লাইডারের জন্য JavaScript
const slider = document.getElementById('mainSlider');
const dotsContainer = document.getElementById('sliderDots');
const slides = slider.querySelectorAll('img');
let currentSlide = 0;

function createDots() {
    slides.forEach((_, index) => {
        const dot = document.createElement('span');
        dot.classList.add('dot');
        if (index === 0) dot.classList.add('active');
        dot.addEventListener('click', () => showSlide(index));
        dotsContainer.appendChild(dot);
    });
}

function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.style.transform = `translateX(-${index * 100}%)`;
    });
    const dots = dotsContainer.querySelectorAll('.dot');
    dots.forEach((dot, i) => {
        dot.classList.toggle('active', i === index);
    });
    currentSlide = index;
}

function nextSlide() {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
}

// Ensure dots are created only once
if (dotsContainer.children.length === 0) {
    createDots();
}

setInterval(nextSlide, 3000); // 3 সেকেন্ড পর পর স্লাইড পরিবর্তন হবে

// অর্ডার বাটনের জন্য JavaScript
document.addEventListener('DOMContentLoaded', () => {
    const orderButtons = document.querySelectorAll('.order-btn');

    orderButtons.forEach(button => {
        // স্টক আউট বাটন নিষ্ক্রিয় থাকলে ইভেন্ট লিসেনার যোগ করবেন না
        if (button.disabled) {
            return;
        }

        button.addEventListener('click', (event) => {
            const itemElement = event.target.closest('.gallery-item');
            const itemName = itemElement.dataset.item;
            const itemPrice = itemElement.dataset.price;

            // নির্বাচিত আইটেমের তথ্য localStorage-এ সংরক্ষণ করুন
            localStorage.setItem('selectedOrderItem', itemName);
            localStorage.setItem('selectedOrderPrice', itemPrice);

            // পেমেন্ট পেজে রিডাইরেক্ট করুন
            window.location.href = 'https://sportsbd7123.blogspot.com/p/payment-page.html'; // <<< এখানে আপনার পেমেন্ট পেজের সঠিক URL বসান
        });
    });
});
</script>
