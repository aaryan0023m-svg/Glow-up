# Glow-up
Glow up means not only applies on face but it also applied on dicipline and other think.In this web page you will get only the checklist of the glow up of your face,hair etc.
!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Glow-Up Checklist</title>
<style>
/* ========== Reset & Base ========== */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
body {
    font-family: 'Poppins', Arial, sans-serif;
    background: linear-gradient(135deg, #e0e7ff, #f0f4f8);
    color: #333;
}

/* ========== Header ========== */
header {
    background: linear-gradient(90deg, #7c3aed, #4f46e5);
    color: white;
    text-align: center;
    padding: 25px 15px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
    box-shadow: 0 6px 12px rgba(0,0,0,0.1);
}
header h1 {
    font-size: 1.7em;
    letter-spacing: 1px;
    text-shadow: 1px 1px 4px rgba(0,0,0,0.2);
}

/* ========== Main Content ========== */
main {
    padding: 20px 15px;
}

/* Cards */
section {
    background: white;
    margin-bottom: 18px;
    padding: 18px 20px;
    border-radius: 20px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.08);
    transition: transform 0.2s, box-shadow 0.2s;
}
section:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 20px rgba(0,0,0,0.15);
}

/* Section Headers */
h2 {
    font-size: 1.3em;
    color: #4f46e5;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
h2::after {
    content: "+";
    font-size: 1.4em;
    transition: transform 0.3s;
}
h2.active::after {
    content: "-";
    transform: rotate(180deg);
}

/* Checklist */
ul {
    padding-left: 20px;
    margin-top: 12px;
}
li {
    margin-bottom: 12px;
    font-size: 1em;
}
input[type="checkbox"] {
    margin-right: 12px;
    transform: scale(1.4);
    cursor: pointer;
}

/* Button */
button {
    width: 100%;
    background: linear-gradient(90deg, #7c3aed, #4f46e5);
    color: white;
    border: none;
    padding: 14px 0;
    border-radius: 15px;
    font-size: 1.1em;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s, transform 0.2s;
    margin-top: 10px;
}
button:hover {
    background: linear-gradient(90deg, #9333ea, #6366f1);
    transform: scale(1.03);
}

/* Footer */
footer {
    text-align: center;
    padding: 20px 10px;
    background: #4f46e5;
    color: white;
    border-top-left-radius: 25px;
    border-top-right-radius: 25px;
    margin-top: 20px;
    box-shadow: 0 -4px 12px rgba(0,0,0,0.1);
}

/* Collapsible content */
.content {
    display: none;
    margin-top: 12px;
    animation: fadeIn 0.3s ease-in-out;
}

/* Smooth fade animation */
@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}
</style>
</head>
<body>

<header>
    <h1>✨ Student Glow-Up Checklist ✨</h1>
</header>

<main>

<section>
    <h2 onclick="toggleSection(this)">Skincare</h2>
    <div class="content">
        <ul>
            <li><input type="checkbox"> Wash face morning & night</li>
            <li><input type="checkbox"> Apply moisturizer</li>
            <li><input type="checkbox"> Apply sunscreen</li>
            <li><input type="checkbox"> Drink 6–8 glasses of water</li>
            <li><input type="checkbox"> Sleep 7–9 hours</li>
        </ul>
    </div>
</section>

<section>
    <h2 onclick="toggleSection(this)">Hair Care</h2>
    <div class="content">
        <ul>
            <li><input type="checkbox"> Wash hair 2–3 times/week</li>
            <li><input type="checkbox"> Brush hair gently</li>
            <li><input type="checkbox"> Keep hairstyle neat</li>
        </ul>
    </div>
</section>

<section>
    <h2 onclick="toggleSection(this)">Fitness & Posture</h2>
    <div class="content">
        <ul>
            <li><input type="checkbox"> Morning stretches (5–10 min)</li>
            <li><input type="checkbox"> Exercise or walk daily</li>
            <li><input type="checkbox"> Sit & stand straight</li>
        </ul>
    </div>
</section>

<section>
    <h2 onclick="toggleSection(this)">Style & Appearance</h2>
    <div class="content">
        <ul>
            <li><input type="checkbox"> Wear clean, ironed clothes</li>
            <li><input type="checkbox"> Pick 2–3 color combos</li>
            <li><input type="checkbox"> Keep shoes & accessories neat</li>
        </ul>
    </div>
</section>

<section>
    <h2 onclick="toggleSection(this)">Mental & Social Glow-Up</h2>
    <div class="content">
        <ul>
            <li><input type="checkbox"> Positive affirmations daily</li>
            <li><input type="checkbox"> Read or learn something new</li>
            <li><input type="checkbox"> Smile and be kind</li>
            <li><input type="checkbox"> Limit phone scrolling</li>
            <li><input type="checkbox"> Keep a gratitude journal</li>
        </ul>
    </div>
</section>

<button onclick="resetChecklist()">Reset Checklist</button>

</main>

<footer>
    &copy; 2026 Student Glow-Up Guide
</footer>

<script>
function toggleSection(el){
    el.classList.toggle('active');
    const content = el.nextElementSibling;
    content.style.display = content.style.display === "block" ? "none" : "block";
}

function resetChecklist(){
    document.querySelectorAll('input[type="checkbox"]').forEach(cb => cb.checked = false);
    alert("Checklist reset!");
}
</script>

</body>
</html>
