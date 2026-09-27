<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Click With Kindness | A Cyber Peace Project</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;500;600;700;800&family=Poppins:wght@300;400;500;600;700&display=swap');

:root {
    --pink: #ffb7d5;
    --pink-dark: #e978ad;
    --blue: #b9e8ff;
    --blue-dark: #5aaed6;
    --purple: #cdbdff;
    --cream: #fff9fc;
    --ink: #40364d;
    --white: #ffffff;
    --mint: #c9f4df;
    --yellow: #ffe8a8;
    --shadow: 0 12px 30px rgba(104,75,120,.12);
}

* {
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    margin: 0;
    color: var(--ink);
    font-family: Poppins, sans-serif;
    background: linear-gradient(
        135deg,
        #fff8fc 0%,
        #f5fbff 50%,
        #faf7ff 100%
    );
    min-height: 100vh;
}

body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    opacity: .35;

    background-image:
        radial-gradient(#ffb7d5 1px, transparent 1px),
        radial-gradient(#b9e8ff 1px, transparent 1px);

    background-size: 28px 28px;
    background-position: 0 0, 14px 14px;

    z-index: -1;
}

h1,
h2,
h3,
.logo {
    font-family: "Baloo 2", cursive;
}

/* =========================
   NAVIGATION
========================= */

header {
    position: sticky;
    top: 0;
    z-index: 50;

    background: rgba(255,255,255,.88);
    backdrop-filter: blur(15px);

    border-bottom: 1px solid rgba(120,90,140,.1);
}

.nav {
    max-width: 1180px;
    margin: auto;

    padding: 12px 20px;

    display: flex;
    align-items: center;
    gap: 18px;
}

.logo {
    font-size: 1.55rem;
    font-weight: 800;

    color: var(--pink-dark);

    white-space: nowrap;
}

.logo span {
    color: var(--blue-dark);
}

.navlinks {
    display: flex;
    gap: 5px;
    flex-wrap: wrap;
    margin-left: auto;
}

.tab {
    border: 0;
    background: transparent;

    color: var(--ink);

    font: 600 .82rem Poppins;

    padding: 9px 12px;

    border-radius: 20px;

    cursor: pointer;

    transition: .25s;
}

.tab:hover,
.tab.active {
    background: var(--pink);
    color: white;

    box-shadow:
        0 5px 15px rgba(233,120,173,.2);
}

/* =========================
   MAIN
========================= */

main {
    max-width: 1180px;
    margin: auto;

    padding: 30px 20px 70px;
}

.page {
    display: none;

    animation: fade .35s ease;
}

.page.active {
    display: block;
}

@keyframes fade {
    from {
        opacity: 0;
        transform: translateY(8px);
    }

    to {
        opacity: 1;
        transform: none;
    }
}

/* =========================
   HERO
========================= */

.hero {
    min-height: 520px;

    display: grid;
    grid-template-columns: 1.1fr .9fr;

    gap: 35px;

    align-items: center;

    padding: 45px 0;
}

.badge {
    display: inline-flex;
    align-items: center;

    gap: 8px;

    background: white;

    border: 2px solid var(--pink);

    color: var(--pink-dark);

    padding: 8px 15px;

    border-radius: 30px;

    font-weight: 700;
    font-size: .85rem;
}

.hero h1 {
    font-size: clamp(3rem, 7vw, 5.8rem);

    line-height: .9;

    margin: 20px 0 18px;

    color: var(--ink);
}

.hero h1 span {
    color: var(--pink-dark);
}

.hero p {
    font-size: 1.08rem;

    line-height: 1.8;

    max-width: 650px;
}

.buttons {
    display: flex;

    gap: 12px;

    flex-wrap: wrap;

    margin-top: 25px;
}

.btn {
    border: 0;

    border-radius: 30px;

    padding: 12px 20px;

    font: 700 .9rem Poppins;

    cursor: pointer;

    transition: .25s;

    box-shadow: var(--shadow);
}

.btn.primary {
    background: var(--pink-dark);
    color: white;
}

.btn.secondary {
    background: white;

    color: var(--ink);

    border: 2px solid var(--blue);
}

.btn:hover {
    transform: translateY(-3px);
}

/* =========================
   HERO ART
========================= */

.hero-art {
    position: relative;

    height: 430px;

    display: grid;

    place-items: center;
}

.cloud {
    position: absolute;

    background: white;

    border-radius: 100px;

    box-shadow: var(--shadow);
}

.cloud.one {
    width: 280px;
    height: 120px;

    top: 65px;
    left: 20px;
}

.cloud.two {
    width: 220px;
    height: 95px;

    right: 15px;
    bottom: 55px;
}

.phone {
    width: 220px;
    height: 360px;

    border: 9px solid var(--ink);

    border-radius: 32px;

    background: white;

    transform: rotate(7deg);

    box-shadow:
        0 25px 50px rgba(64,54,77,.18);

    position: relative;

    z-index: 2;

    padding: 35px 16px 15px;
}

.phone::before {
    content: "";

    position: absolute;

    top: 12px;
    left: 50%;

    transform: translateX(-50%);

    width: 70px;
    height: 8px;

    background: #40364d;

    border-radius: 20px;
}

.chat {
    padding: 9px 12px;

    border-radius: 16px;

    margin: 9px 0;

    font-size: .7rem;
}

.chat.a {
    background: #f0eaff;
}

.chat.b {
    background: #ffe0ed;

    margin-left: 35px;
}

.heart {
    position: absolute;

    font-size: 3rem;

    z-index: 3;

    animation: float 3s ease-in-out infinite;
}

.heart.a {
    top: 45px;
    right: 75px;
}

.heart.b {
    bottom: 70px;
    left: 40px;

    animation-delay: 1s;
}

@keyframes float {

    50% {
        transform: translateY(-12px) rotate(8deg);
    }
}

/* =========================
   SECTION TITLES
========================= */

.section-title {
    text-align: center;

    margin: 20px 0 35px;
}

.section-title h2 {
    font-size: 2.8rem;

    margin: 0;
}

.section-title p {
    max-width: 700px;

    margin: 8px auto;

    line-height: 1.7;
}

/* =========================
   CARDS
========================= */

.cards {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 20px;
}

.card {
    background: rgba(255,255,255,.9);

    padding: 25px;

    border-radius: 28px;

    box-shadow: var(--shadow);

    border:
        1px solid rgba(200,180,210,.25);

    transition: .25s;
}

.card:hover {
    transform: translateY(-5px);
}

.icon {
    font-size: 2.2rem;
}

.card h3 {
    font-size: 1.45rem;

    margin: 8px 0;
}

.card p,
.card li {
    line-height: 1.7;

    font-size: .93rem;
}

.pill {
    display: inline-block;

    padding: 5px 10px;

    border-radius: 20px;

    background: var(--blue);

    font-size: .75rem;

    font-weight: 700;

    margin: 3px;
}

/* =========================
   QUOTE
========================= */

.quote {
    margin: 25px 0;

    background:
        linear-gradient(
            135deg,
            #fff,
            #fff1f7
        );

    border-left:
        6px solid var(--pink-dark);

    padding: 25px;

    border-radius: 20px;

    font-family: "Baloo 2";

    font-size: 1.5rem;
}

/* =========================
   FLOW
========================= */

.flow {
    display: flex;

    align-items: center;

    justify-content: center;

    gap: 8px;

    flex-wrap: wrap;

    margin: 25px 0;
}

.flow div {
    padding: 15px 18px;

    border-radius: 20px;

    font-weight: 700;

    background: white;

    box-shadow: var(--shadow);
}

.arrow {
    font-size: 1.5rem;

    color: var(--pink-dark);
}

/* =========================
   SCENARIOS
========================= */

.scenario {
    max-width: 800px;

    margin: 0 auto;

    background: white;

    padding: 30px;

    border-radius: 30px;

    box-shadow: var(--shadow);
}

.choice {
    width: 100%;

    text-align: left;

    margin: 9px 0;

    background: #faf7ff;

    border:
        2px solid #eee3f6;

    border-radius: 16px;

    padding: 14px;

    cursor: pointer;

    font: 500 .9rem Poppins;

    transition: .2s;
}

.choice:hover {
    border-color: var(--pink);

    background: #fff4f9;
}

.result {
    margin-top: 18px;

    padding: 18px;

    border-radius: 18px;

    background: var(--mint);

    display: none;

    line-height: 1.7;
}

.result.show {
    display: block;
}

/* =========================
   PLEDGE
========================= */

.pledge {
    max-width: 800px;

    margin: auto;

    background:
        linear-gradient(
            135deg,
            #fff,
            #f3faff
        );

    padding: 35px;

    border-radius: 30px;

    box-shadow: var(--shadow);

    text-align: center;
}

.pledge textarea,
.form input,
.form textarea,
.form select {
    width: 100%;

    padding: 13px 15px;

    border:
        2px solid #eadff0;

    border-radius: 15px;

    font: inherit;

    outline: none;

    background: white;

    margin: 7px 0 15px;
}

.pledge textarea:focus,
.form input:focus,
.form textarea:focus,
.form select:focus {
    border-color: var(--pink);
}

.counter {
    font-family: "Baloo 2";

    font-size: 3rem;

    color: var(--pink-dark);

    font-weight: 800;
}

/* =========================
   KINDNESS WALL
========================= */

.wall {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 15px;

    margin-top: 25px;
}

.note {
    padding: 20px;

    border-radius: 22px;

    min-height: 130px;

    background: #fff5a9;

    box-shadow: var(--shadow);

    transform: rotate(-1deg);
}

.note:nth-child(2n) {
    background: #d9f4ff;

    transform: rotate(1.5deg);
}

.note:nth-child(3n) {
    background: #f3ddff;

    transform: rotate(-2deg);
}

.note strong {
    display: block;

    margin-top: 12px;

    font-size: .8rem;
}

/* =========================
   FORM
========================= */

.form {
    max-width: 760px;

    margin: auto;

    background: white;

    padding: 30px;

    border-radius: 30px;

    box-shadow: var(--shadow);
}

.question {
    padding: 20px 0;

    border-bottom: 1px solid #eee;
}

.question:last-child {
    border: 0;
}

.option {
    display: block;

    margin: 9px 0;

    padding: 10px 14px;

    border-radius: 15px;

    background: #faf7ff;

    cursor: pointer;
}

.option:hover {
    background: #fff0f7;
}

.option input {
    accent-color: var(--pink-dark);

    margin-right: 8px;
}

.survey-result {
    display: none;

    margin-top: 25px;

    background:
        linear-gradient(
            135deg,
            #f0eaff,
            #e4f8ff
        );

    padding: 25px;

    border-radius: 25px;

    text-align: center;
}

.survey-result.show {
    display: block;
}

.big-score {
    font:
        800 3.5rem
        "Baloo 2";

    color: var(--pink-dark);
}

/* =========================
   RESOURCES
========================= */

.resource {
    display: flex;

    gap: 15px;

    align-items: flex-start;

    margin: 15px 0;

    padding: 17px;

    background: white;

    border-radius: 18px;
}

.resource span {
    font-size: 1.7rem;
}

/* =========================
   FOOTER
========================= */

footer {
    text-align: center;

    padding: 25px;

    color: #776c82;

    font-size: .82rem;
}

/* =========================
   MOBILE
========================= */

@media(max-width:850px) {

    .hero {
        grid-template-columns: 1fr;

        text-align: center;
    }

    .hero p {
        margin-left: auto;
        margin-right: auto;
    }

    .hero-art {
        height: 360px;
    }

    .cards {
        grid-template-columns: 1fr;
    }

    .wall {
        grid-template-columns: 1fr;
    }

    .nav {
        align-items: flex-start;

        flex-direction: column;
    }

    .navlinks {
        margin-left: 0;

        width: 100%;

        overflow-x: auto;

        flex-wrap: nowrap;
    }

    .tab {
        white-space: nowrap;
    }

    .flow {
        flex-direction: column;
    }

    .arrow {
        transform: rotate(90deg);
    }
}
</style>
</head>

<body>

<header>

<nav class="nav">

<div class="logo">
    Click <span>♡</span> With Kindness
</div>

<div class="navlinks">

<button class="tab active" data-page="home">
    Home
</button>

<button class="tab" data-page="learn">
    Learn
</button>

<button class="tab" data-page="faith">
    Faith & Peace
</button>

<button class="tab" data-page="scenario">
    Scenarios
</button>

<button class="tab" data-page="action">
    Be a Peacemaker
</button>

<button class="tab" data-page="wall">
    Kindness Wall
</button>

<button class="tab" data-page="survey">
    Survey
</button>

<button class="tab" data-page="resources">
    Resources
</button>

</div>

</nav>

</header>

<main>

<!-- =========================
     HOME
========================= -->

<section id="home" class="page active">

<div class="hero">

<div>

<span class="badge">
    🕊️ A Christian Peacebuilding Initiative
</span>

<h1>
    Think before you
    <span>click.</span>
    <br>
    Choose kindness.
</h1>

<p>

Welcome to <b>Click With Kindness</b>,
a student-friendly campaign about
cyberbullying, Christian compassion,
human dignity, and becoming peacemakers
in the digital world.

</p>

<div class="buttons">

<button
    class="btn primary"
    onclick="showPage('learn')">

    Explore the Campaign ✨

</button>

<button
    class="btn secondary"
    onclick="showPage('survey')">

    Take the Survey 📝

</button>

</div>

</div>


<div class="hero-art">

<div class="cloud one"></div>

<div class="cloud two"></div>

<div class="phone">

<div class="chat a">
    Hey! Are you okay? 💙
</div>

<div class="chat b">
    Thank you for checking on me.
</div>

<div class="chat a">
    You're not alone. 🕊️
</div>

<div class="chat b">
    That means a lot. ♡
</div>

</div>

<div class="heart a">
    💗
</div>

<div class="heart b">
    🕊️
</div>

</div>

</div>


<div class="section-title">

<h2>
    From Faith to Action
</h2>

<p>
    Our goal is to turn Christian values
    into practical choices that help create
    a safer and more peaceful online community.
</p>

</div>


<div class="flow">

<div>
    💻 Cyberbullying
</div>

<span class="arrow">
    →
</span>

<div>
    ✝️ Christian Faith
</div>

<span class="arrow">
    →
</span>

<div>
    🕊️ Peace
</div>

<span class="arrow">
    →
</span>

<div>
    💗 Concrete Action
</div>

</div>

</section>


<!-- =========================
     LEARN
========================= -->

<section id="learn" class="page">

<div class="section-title">

<h2>
    Understanding Cyberbullying 💻
</h2>

<p>
    Learning about the problem is the first step
    toward responding with compassion, justice,
    and respect.
</p>

</div>


<div class="cards">

<article class="card">

<div class="icon">
    📱
</div>

<h3>
    What is it?
</h3>

<p>
Cyberbullying involves harmful behavior
carried out through digital spaces.

It can include repeated hurtful messages,
public humiliation, rumors, exclusion,
threats, or sharing embarrassing content.
</p>

</article>


<article class="card">

<div class="icon">
    👥
</div>

<h3>
    Who is affected?
</h3>

<p>
Targets, friends, classmates, families,
and the wider school community can all
be affected when online conflict damages
trust, relationships, safety, and dignity.
</p>

</article>


<article class="card">

<div class="icon">
    💔
</div>

<h3>
    Why does it matter?
</h3>

<p>
Online cruelty can turn digital spaces
into places of fear and conflict.

Peacebuilding means choosing responses
that protect dignity and rebuild
respectful relationships.
</p>

</article>

</div>


<div class="quote">

“Behind every screen is a real person
with real feelings.”

</div>


<div class="cards">

<article class="card">

<h3>
    Common forms
</h3>

<span class="pill">
    Hurtful comments
</span>

<span class="pill">
    Rumors
</span>

<span class="pill">
    Threats
</span>

<span class="pill">
    Exclusion
</span>

<span class="pill">
    Embarrassing posts
</span>

<span class="pill">
    Harassment
</span>

</article>


<article class="card">

<h3>
    Possible effects
</h3>

<ul>

<li>
    Damaged relationships
</li>

<li>
    Loss of trust and belonging
</li>

<li>
    Fear or insecurity
</li>

<li>
    Harm to human dignity
</li>

<li>
    Conflict within the community
</li>

</ul>

</article>


<article class="card">

<h3>
    Peacebuilding lens
</h3>

<p>
Instead of adding to the conflict,
we can interrupt harmful behavior,
support people who are affected,
report abuse responsibly,
and seek help from trusted adults.
</p>

</article>

</div>

</section>


<!-- =========================
     FAITH
========================= -->

<section id="faith" class="page">

<div class="section-title">

<h2>
    Faith & Peace ✝️🕊️
</h2>

<p>
    Christian faith can guide how we treat
    people—even when we are behind a screen.
</p>

</div>


<div class="card">

<div class="quote">

“Blessed are the peacemakers,
for they shall be called children of God.”

<br>

<small>
    — Matthew 5:9
</small>

</div>

<h3>
    What does this mean for cyberbullying?
</h3>

<p>
Being a peacemaker does not mean ignoring
harmful behavior.

It means responding responsibly,
protecting human dignity, refusing to
participate in cruelty, supporting people
who are hurt, and seeking peaceful ways
to address conflict.
</p>

</div>


<br>


<div class="cards">

<article class="card">

<div class="icon">
    ❤️
</div>

<h3>
    Love of Neighbor
</h3>

<p>
Our online words should reflect care
for other people rather than intentionally
causing harm.
</p>

</article>


<article class="card">

<div class="icon">
    🤍
</div>

<h3>
    Human Dignity
</h3>

<p>
A person's worth should not depend on
popularity, appearance, mistakes,
or what others say online.
</p>

</article>


<article class="card">

<div class="icon">
    🤝
</div>

<h3>
    Compassion & Solidarity
</h3>

<p>
We can stand beside people who are being
targeted instead of becoming silent spectators.
</p>

</article>

</div>


<div
    class="cards"
    style="margin-top:20px">

<article class="card">

<div class="icon">
    ⚖️
</div>

<h3>
    Justice
</h3>

<p>
Responsible action includes reporting
harmful behavior and involving trusted
adults when safety is at risk.
</p>

</article>


<article class="card">

<div class="icon">
    🌱
</div>

<h3>
    Reconciliation
</h3>

<p>
When appropriate and safe, peaceful
communication can help restore
respectful relationships.
</p>

</article>


<article class="card">

<div class="icon">
    🕊️
</div>

<h3>
    Peacemaking
</h3>

<p>
Small choices—kind words, support,
reporting, and refusing to join in—
can change the atmosphere of an
online community.
</p>

</article>

</div>

</section>


<!-- =========================
     SCENARIOS
========================= -->

<section id="scenario" class="page">

<div class="section-title">

<h2>
    Choose Your Response 🎭
</h2>

<p>
    Test how you would respond to
    a cyberbullying situation.
</p>

</div>


<div class="scenario">

<h3>
    Scenario 1
</h3>

<p>

<b>
You see a classmate being mocked
in a group chat.

Several people are laughing and
adding hurtful comments.

What would you do?
</b>

</p>


<button
    class="choice"
    onclick="scenarioAnswer(1)">

A. Join the jokes so I don't feel left out.

</button>


<button
    class="choice"
    onclick="scenarioAnswer(2)">

B. Ignore it completely and hope it stops.

</button>


<button
    class="choice"
    onclick="scenarioAnswer(3)">

C. Don't participate, support the classmate,
and report/seek help if needed.

</button>


<button
    class="choice"
    onclick="scenarioAnswer(4)">

D. Share the screenshots publicly to
embarrass the people involved.

</button>


<div
    id="scenarioResult"
    class="result">
</div>

</div>


<br>


<div class="scenario">

<h3>
    Scenario 2
</h3>

<p>

<b>
A friend sends you an embarrassing photo
of someone and asks you to repost it.

What is a peacebuilding response?
</b>

</p>


<button
    class="choice"
    onclick="scenarioAnswer2(1)">

A. Repost it because my friend asked.

</button>


<button
    class="choice"
    onclick="scenarioAnswer2(2)">

B. Refuse to share it and encourage
my friend to delete it.

</button>


<button
    class="choice"
    onclick="scenarioAnswer2(3)">

C. Add a funny caption.

</button>


<div
    id="scenarioResult2"
    class="result">
</div>

</div>

</section>


<!-- =========================
     ACTION
========================= -->

<section id="action" class="page">

<div class="section-title">

<h2>
    Be a Peacemaker 🕊️
</h2>

<p>
    Use the S.A.F.E. approach when you
    encounter cyberbullying.
</p>

</div>


<div class="cards">

<article class="card">

<div class="icon">
    👀
</div>

<h3>
    S — See
</h3>

<p>
Recognize harmful behavior.

Don't automatically treat online
cruelty as “just a joke.”
</p>

</article>


<article class="card">

<div class="icon">
    🛑
</div>

<h3>
    A — Avoid joining
</h3>

<p>
Don't like, repost, comment on,
or encourage harmful content.
</p>

</article>


<article class="card">

<div class="icon">
    💙
</div>

<h3>
    F — Find support
</h3>

<p>
Check on the person affected and
involve a trusted adult when necessary.
</p>

</article>


<article class="card">

<div class="icon">
    📢
</div>

<h3>
    E — Escalate responsibly
</h3>

<p>
Save evidence and use appropriate
reporting tools when the behavior
is harmful or unsafe.
</p>

</article>

</div>


<div
    class="pledge"
    style="margin-top:25px">

<h2>
    My Peace Pledge
</h2>

<p>

I will use my digital voice to respect
human dignity, encourage others,
and refuse to participate in cyberbullying.

</p>


<input
    id="pledgeName"
    placeholder="Your first name or nickname"
>


<button
    class="btn primary"
    onclick="takePledge()">

I Choose to Be a Peacemaker 💗

</button>


<div
    class="counter"
    id="pledgeCount">

0

</div>


<p>
    peacemakers have taken the pledge
    on this device
</p>

</div>

</section>


<!-- =========================
     KINDNESS WALL
========================= -->

<section id="wall" class="page">

<div class="section-title">

<h2>
    Kindness Wall 💌
</h2>

<p>
    Leave a positive message that someone
    might need to hear today.
</p>

</div>


<div class="form">

<input
    id="wallName"
    placeholder="Your name or nickname (optional)"
>


<textarea
    id="wallMessage"
    rows="4"
    placeholder="Write a kind message..."
></textarea>


<button
    class="btn primary"
    onclick="addNote()">

Post Kindness ✨

</button>

</div>


<div
    class="wall"
    id="wallPosts">

<div class="note">

Your words can make someone's
day brighter. 💗

<strong>
    — Anonymous
</strong>

</div>


<div class="note">

Choose compassion,
even when nobody is watching. 🕊️

<strong>
    — A Peacemaker
</strong>

</div>


<div class="note">

You are worthy of respect
online and offline. 🌷

<strong>
    — Friend
</strong>

</div>

</div>

</section>


<!-- =========================
     SURVEY
========================= -->

<section id="survey" class="page">

<div class="section-title">

<h2>
    Cyber Peace Survey 📝
</h2>

<p>
Your answers are used only to demonstrate
awareness and reflection for our project.

No identifying information is required.
</p>

</div>


<form
    class="form"
    id="surveyForm">


<div class="question">

<b>
1. Before visiting this website,
how familiar were you with cyberbullying?
</b>


<label class="option">

<input
    type="radio"
    name="q1"
    value="1"
    required
>

Not familiar

</label>


<label class="option">

<input
    type="radio"
    name="q1"
    value="2"
>

A little familiar

</label>


<label class="option">

<input
    type="radio"
    name="q1"
    value="3"
>

Familiar

</label>


<label class="option">

<input
    type="radio"
    name="q1"
    value="4"
>

Very familiar

</label>

</div>


<div class="question">

<b>
2. How important is it to avoid
participating in cyberbullying?
</b>


<label class="option">

<input
    type="radio"
    name="q2"
    value="1"
    required
>

Not important

</label>


<label class="option">

<input
    type="radio"
    name="q2"
    value="2"
>

Somewhat important

</label>


<label class="option">

<input
    type="radio"
    name="q2"
    value="3"
>

Important

</label>


<label class="option">

<input
    type="radio"
    name="q2"
    value="4"
>

Very important

</label>

</div>


<div class="question">

<b>
3. If you saw cyberbullying,
how confident are you that you
could respond peacefully?
</b>


<label class="option">

<input
    type="radio"
    name="q3"
    value="1"
    required
>

Not confident

</label>


<label class="option">

<input
    type="radio"
    name="q3"
    value="2"
>

Slightly confident

</label>


<label class="option">

<input
    type="radio"
    name="q3"
    value="3"
>

Confident

</label>


<label class="option">

<input
    type="radio"
    name="q3"
    value="4"
>

Very confident

</label>

</div>


<div class="question">

<b>
4. Which action would you be
most willing to take?
</b>


<label class="option">

<input
    type="radio"
    name="q4"
    value="support"
    required
>

Support the person affected

</label>


<label class="option">

<input
    type="radio"
    name="q4"
    value="report"
>

Report harmful behavior

</label>


<label class="option">

<input
    type="radio"
    name="q4"
    value="refuse"
>

Refuse to join or share
harmful content

</label>


<label class="option">

<input
    type="radio"
    name="q4"
    value="all"
>

All of these

</label>

</div>


<div class="question">

<b>
5. Which Christian value connects
most strongly with being a peacemaker online?
</b>


<label class="option">

<input
    type="radio"
    name="q5"
    value="love"
    required
>

Love of neighbor

</label>


<label class="option">

<input
    type="radio"
    name="q5"
    value="dignity"
>

Human dignity

</label>


<label class="option">

<input
    type="radio"
    name="q5"
    value="compassion"
>

Compassion

</label>


<label class="option">

<input
    type="radio"
    name="q5"
    value="justice"
>

Justice

</label>

</div>


<button
    class="btn primary"
    type="submit">

Submit Survey & See My Reflection 🌸

</button>


<button
    class="btn secondary"
    type="button"
    onclick="clearSurvey()">

Clear Answers

</button>


<div
    id="surveyResult"
    class="survey-result">

</div>

</form>

</section>


<!-- =========================
     RESOURCES
========================= -->

<section id="resources" class="page">

<div class="section-title">

<h2>
    Help & Resources 🌷
</h2>

<p>
If online behavior becomes threatening,
persistent, or unsafe, don't handle it alone.
</p>

</div>


<div class="cards">

<article class="card">

<h3>
    📸 Keep evidence
</h3>

<p>
When appropriate, save screenshots,
usernames, dates, and relevant messages
so a trusted adult or responsible authority
can understand what happened.
</p>

</article>


<article class="card">

<h3>
    🚫 Block & report
</h3>

<p>
Use the safety and reporting tools available
on the platform.

Avoid retaliating or escalating the conflict.
</p>

</article>


<article class="card">

<h3>
    🧑‍🏫 Tell someone
</h3>

<p>
Talk to a parent, teacher, counselor,
school administrator, or another trusted adult,
especially if there are threats or safety concerns.
</p>

</article>

</div>


<div
    class="card"
    style="margin-top:20px">

<h3>
    Remember
</h3>


<div class="resource">

<span>
    💗
</span>

<div>

<b>
    You don't have to face it alone.
</b>

<br>

Seeking help is a responsible
peacebuilding action.

</div>

</div>


<div class="resource">

<span>
    🕊️
</span>

<div>

<b>
    Peacemaking is active.
</b>

<br>

It can mean refusing to join harmful
behavior, supporting someone,
and seeking appropriate help.

</div>

</div>


<div class="resource">

<span>
    ✝️
</span>

<div>

<b>
    Let your faith guide your actions.
</b>

<br>

Christian values can shape how we treat
others in digital spaces.

</div>

</div>

</div>

</section>

</main>


<footer>

<b>
    Click With Kindness
</b>

· A Christian Peacebuilding Initiative
· Made for student awareness and action 💗

</footer>


<script>

/* =========================
   TAB NAVIGATION
========================= */

const tabs =
    document.querySelectorAll('.tab');

const pages =
    document.querySelectorAll('.page');


function showPage(id) {

    pages.forEach(page => {

        page.classList.toggle(
            'active',
            page.id === id
        );

    });


    tabs.forEach(tab => {

        tab.classList.toggle(
            'active',
            tab.dataset.page === id
        );

    });


    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    });
}


tabs.forEach(tab => {

    tab.addEventListener(
        'click',
        () => showPage(tab.dataset.page)
    );

});


/* =========================
   SCENARIO 1
========================= */

function scenarioAnswer(choice) {

    const result =
        document.getElementById(
            'scenarioResult'
        );

    result.classList.add('show');


    if (choice === 3) {

        result.innerHTML = `

        <b>
            🌟 Peacebuilder response!
        </b>

        <br>

        You chose not to participate,
        support the person affected,
        and seek responsible help.

        This reflects compassion,
        human dignity, and peacemaking.

        `;

    } else {

        result.innerHTML = `

        <b>
            💭 Think again.
        </b>

        <br>

        This response can allow harm
        to continue or make the situation worse.

        A peacebuilder avoids joining the harm,
        supports the person affected,
        and seeks appropriate help.

        `;

    }

}


/* =========================
   SCENARIO 2
========================= */

function scenarioAnswer2(choice) {

    const result =
        document.getElementById(
            'scenarioResult2'
        );

    result.classList.add('show');


    if (choice === 2) {

        result.innerHTML = `

        <b>
            🌟 Peacebuilder response!
        </b>

        <br>

        Refusing to share embarrassing content
        protects the person's dignity and prevents
        the harm from spreading.

        `;

    } else {

        result.innerHTML = `

        <b>
            💭 Think again.
        </b>

        <br>

        Sharing embarrassing content can
        spread harm.

        A peaceful response refuses to participate
        and encourages responsible action.

        `;

    }

}


/* =========================
   PEACE PLEDGE
========================= */

let pledges =
    Number(
        localStorage.getItem(
            'kindnessPledges'
        ) || 0
    );


document.getElementById(
    'pledgeCount'
).textContent = pledges;


function takePledge() {

    const name =
        document.getElementById(
            'pledgeName'
        ).value.trim();


    if (!name) {

        alert(
            'Please enter a first name or nickname.'
        );

        return;
    }


    pledges++;


    localStorage.setItem(
        'kindnessPledges',
        pledges
    );


    document.getElementById(
        'pledgeCount'
    ).textContent = pledges;


    document.getElementById(
        'pledgeName'
    ).value = '';


    alert(
        'Thank you, ' +
        name +
        '! 🕊️ You chose to be a peacemaker.'
    );

}


/* =========================
   KINDNESS WALL
========================= */

function addNote() {

    const name =
        document.getElementById(
            'wallName'
        ).value.trim()
        || 'Anonymous';


    const message =
        document.getElementById(
            'wallMessage'
        ).value.trim();


    if (!message) {

        alert(
            'Please write a kind message first.'
        );

        return;
    }


    const note =
        document.createElement('div');


    note.className = 'note';


    note.innerHTML =
        escapeHtml(message) +
        '<strong>— ' +
        escapeHtml(name) +
        '</strong>';


    document
        .getElementById('wallPosts')
        .prepend(note);


    document.getElementById(
        'wallName'
    ).value = '';


    document.getElementById(
        'wallMessage'
    ).value = '';

}


function escapeHtml(str) {

    return str.replace(
        /[&<>"']/g,

        character => ({

            '&': '&amp;',
            '<': '&lt;',
            '>': '&gt;',
            '"': '&quot;',
            "'": '&#039;'

        }[character])

    );

}


/* =========================
   SURVEY
========================= */

document
    .getElementById('surveyForm')
    .addEventListener(
        'submit',
        function(event) {

            event.preventDefault();


            const data =
                new FormData(this);


            let score = 0;


            [
                'q1',
                'q2',
                'q3'
            ].forEach(question => {

                score += Number(
                    data.get(question)
                );

            });


            const q4 =
                data.get('q4');


            const q5 =
                data.get('q5');


            const confidence =
                Math.round(
                    (score / 12) * 100
                );


            const actionText = {

                support:
                    'supporting someone affected',

                report:
                    'reporting harmful behavior',

                refuse:
                    'refusing to join or share harmful content',

                all:
                    'using all of these actions'

            }[q4];


            const valueText = {

                love:
                    'love of neighbor',

                dignity:
                    'human dignity',

                compassion:
                    'compassion',

                justice:
                    'justice'

            }[q5];


            const result =
                document.getElementById(
                    'surveyResult'
                );


            result.classList.add('show');


            result.innerHTML = `

            <div class="big-score">

                ${confidence}%

            </div>

            <h3>
                Your Cyber Peace
                Readiness Reflection
            </h3>

            <p>

            Based on your answers,
            you showed awareness of
            cyberbullying and the importance
            of peaceful action.

            You identified
            <b>${actionText}</b>
            as an action you are willing to take,
            and <b>${valueText}</b>
            as a Christian value connected
            to peacemaking.

            </p>

            <p>

            <b>
                Personal challenge:
            </b>

            What is one specific action
            you can take this week to make
            your online community kinder?

            </p>

            `;

        }
    );


/* =========================
   CLEAR SURVEY
========================= */

function clearSurvey() {

    document
        .getElementById('surveyForm')
        .reset();


    const result =
        document.getElementById(
            'surveyResult'
        );


    result.classList.remove('show');

    result.innerHTML = '';

}

</script>

</body>
</html>
