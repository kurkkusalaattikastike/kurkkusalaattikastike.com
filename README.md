<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>kurkkusalaattikastike</title>

<style>
:root {
    --bg: #0b0b0b;
    --surface: #111111;
    --surface-hover: #151515;

    --text: #e8e8e8;
    --muted: #888;
    --subtle: #555;

    --border: #292929;

    --accent: #d6d6d6;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    background: var(--bg);
    color: var(--text);

    font-family:
        Inter,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;

    line-height: 1.6;
}

a {
    color: inherit;
    text-decoration: none;
}


/* =========================
   NAVIGATION
========================= */

nav {
    position: fixed;

    top: 0;
    left: 0;
    right: 0;

    height: 60px;

    display: flex;
    align-items: center;
    justify-content: space-between;

    padding: 0 6%;

    background: rgba(11,11,11,.9);

    backdrop-filter: blur(12px);

    border-bottom: 1px solid var(--border);

    z-index: 100;
}

.logo {
    font-family: monospace;
    font-size: 14px;
    font-weight: 600;
}

.nav-links {
    display: flex;
    gap: 25px;

    list-style: none;
}

.nav-links a {
    color: var(--muted);

    font-family: monospace;
    font-size: 12px;

    transition: .2s;
}

.nav-links a:hover {
    color: white;
}


/* =========================
   LAYOUT
========================= */

.container {
    width: min(920px, 88%);
    margin: auto;
}

section {
    padding: 115px 0;

    border-bottom: 1px solid var(--border);
}

.section-label {
    color: var(--subtle);

    font-family: monospace;

    font-size: 11px;

    letter-spacing: 1px;

    margin-bottom: 18px;
}

h2 {
    font-size: 42px;

    font-weight: 500;

    letter-spacing: -2px;

    margin-bottom: 45px;
}


/* =========================
   HERO
========================= */

.hero {
    min-height: 100vh;

    display: flex;
    align-items: center;

    padding-top: 60px;
}

.hero-inner {
    width: 100%;
}

.hero small {
    display: block;

    color: var(--muted);

    font-family: monospace;

    font-size: 13px;

    margin-bottom: 20px;
}

.hero h1 {
    font-size: clamp(55px, 9vw, 100px);

    font-weight: 500;

    letter-spacing: -6px;

    line-height: .95;

    margin-bottom: 30px;
}

.hero-description {
    max-width: 560px;

    color: var(--muted);

    font-size: 16px;

    margin-bottom: 30px;
}

.links {
    display: flex;
    gap: 18px;
    flex-wrap: wrap;
}

.simple-link {
    color: #aaa;

    font-family: monospace;

    font-size: 12px;

    border-bottom: 1px solid #444;

    padding-bottom: 3px;

    transition: .2s;
}

.simple-link:hover {
    color: white;
    border-color: white;
}


/* =========================
   ABOUT
========================= */

.about-grid {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 70px;
}

.about-text {
    color: var(--muted);

    font-size: 15px;
}

.about-text p {
    margin-bottom: 18px;
}

.about-text strong {
    color: #ddd;
    font-weight: 500;
}


/* =========================
   INFO LIST
========================= */

.info-list {
    border-top: 1px solid var(--border);
}

.info-row {
    display: flex;

    justify-content: space-between;

    padding: 13px 0;

    border-bottom: 1px solid var(--border);

    font-family: monospace;

    font-size: 12px;
}

.info-row span:first-child {
    color: var(--subtle);
}

.info-row span:last-child {
    color: #aaa;
}


/* =========================
   SKILLS
========================= */

.skill-list {
    display: grid;

    grid-template-columns: repeat(2, 1fr);

    border-top: 1px solid var(--border);
}

.skill {
    padding: 18px 0;

    border-bottom: 1px solid var(--border);

    font-family: monospace;

    font-size: 13px;

    color: #aaa;
}

.skill:nth-child(odd) {
    border-right: 1px solid var(--border);

    padding-right: 30px;
}

.skill:nth-child(even) {
    padding-left: 30px;
}


/* =========================
   LINUX
========================= */

.linux-intro {
    color: var(--muted);

    max-width: 600px;

    margin-top: -25px;

    margin-bottom: 45px;
}

.level {
    margin-bottom: 50px;
}

.level-heading {
    display: flex;

    align-items: baseline;

    gap: 12px;

    margin-bottom: 12px;
}

.level-number {
    color: var(--subtle);

    font-family: monospace;

    font-size: 11px;
}

.level-heading h3 {
    font-size: 17px;

    font-weight: 500;
}

.level-heading small {
    color: var(--subtle);

    font-family: monospace;

    font-size: 10px;
}


/* =========================
   DISTROS
========================= */

.distro {
    display: flex;

    align-items: center;

    gap: 16px;

    padding: 16px 0;

    border-top: 1px solid var(--border);

    transition: .2s;
}

.distro:last-child {
    border-bottom: 1px solid var(--border);
}

.distro:hover {
    padding-left: 8px;
}

.distro-icon {
    width: 38px;
    height: 38px;

    display: flex;
    align-items: center;
    justify-content: center;

    flex-shrink: 0;

    border: 1px solid #333;

    border-radius: 7px;

    color: #bbb;

    font-family: monospace;

    font-size: 11px;
}

.distro-info {
    flex: 1;
}

.distro-name {
    font-size: 14px;

    color: #ddd;
}

.distro-description {
    color: var(--subtle);

    font-size: 12px;
}

.distro-arrow {
    color: #444;

    font-family: monospace;

    transition: .2s;
}

.distro:hover .distro-arrow {
    color: #aaa;
}


/* =========================
   PROJECTS
========================= */

.projects {
    border-top: 1px solid var(--border);
}

.project {
    display: grid;

    grid-template-columns: 60px 1fr auto;

    gap: 20px;

    align-items: center;

    padding: 24px 0;

    border-bottom: 1px solid var(--border);

    transition: .2s;
}

.project:hover {
    padding-left: 8px;
}

.project-number {
    color: var(--subtle);

    font-family: monospace;

    font-size: 11px;
}

.project-name {
    font-size: 15px;

    margin-bottom: 3px;
}

.project-description {
    color: var(--muted);

    font-size: 12px;
}

.project-link {
    color: #777;

    font-family: monospace;

    font-size: 11px;
}

.project:hover .project-link {
    color: white;
}


/* =========================
   CONTACT
========================= */

.contact {
    border-bottom: none;
}

.contact h2 {
    font-size: clamp(45px, 8vw, 80px);

    letter-spacing: -4px;

    margin-bottom: 20px;
}

.contact p {
    color: var(--muted);

    max-width: 500px;

    margin-bottom: 25px;
}


/* =========================
   FOOTER
========================= */

footer {
    width: min(920px, 88%);

    margin: auto;

    padding: 25px 0;

    display: flex;

    justify-content: space-between;

    color: #444;

    font-family: monospace;

    font-size: 10px;
}


/* =========================
   MOBILE
========================= */

@media (max-width: 700px) {

    nav {
        padding: 0 20px;
    }

    .nav-links {
        display: none;
    }

    .container {
        width: 88%;
    }

    section {
        padding: 85px 0;
    }

    .hero h1 {
        letter-spacing: -4px;
    }

    .about-grid {
        grid-template-columns: 1fr;

        gap: 40px;
    }

    .skill-list {
        grid-template-columns: 1fr;
    }

    .skill:nth-child(odd) {
        border-right: none;
        padding-right: 0;
    }

    .skill:nth-child(even) {
        padding-left: 0;
    }

    .project {
        grid-template-columns: 35px 1fr;
    }

    .project-link {
        display: none;
    }

    footer {
        flex-direction: column;

        gap: 8px;
    }
}
</style>
</head>


<body>


<!-- =========================
     NAV
========================= -->

<nav>

    <a href="#home" class="logo">
        kurkkusalaattikastike
    </a>

    <ul class="nav-links">
        <li><a href="#about">about</a></li>
        <li><a href="#skills">skills</a></li>
        <li><a href="#linux">linux</a></li>
        <li><a href="#projects">projects</a></li>
        <li><a href="#contact">contact</a></li>
    </ul>

</nav>


<main>


<!-- =========================
     HERO
========================= -->

<section id="home" class="hero">

<div class="container hero-inner">

    <small>
        / home / kurkkusalaattikastike
    </small>

    <h1>
        kurkkusalaatti<br>
        kastike
    </h1>

    <p class="hero-description">
        Developer interested in web development,
        programming and Linux. I like building things,
        experimenting and learning how systems work.
    </p>

    <div class="links">

        <a
            class="simple-link"
            href="#projects"
        >
            projects →
        </a>

        <a
            class="simple-link"
            href="https://github.com/kurkkusalaattikastike"
            target="_blank"
        >
            github →
        </a>

        <a
            class="simple-link"
            href="#contact"
        >
            contact →
        </a>

    </div>

</div>

</section>


<!-- =========================
     ABOUT
========================= -->

<section id="about">

<div class="container">

    <div class="section-label">
        01 / about
    </div>

    <h2>
        About me
    </h2>

    <div class="about-grid">

        <div class="about-text">

            <p>
                Hi, I'm
                <strong>kurkkusalaattikastike</strong>.
            </p>

            <p>
                I'm learning web development and
                programming while exploring Linux
                and different parts of the computing world.
            </p>

            <p>
                Most of my projects start with a
                random idea and end with me learning
                something I didn't know before.
            </p>

        </div>


        <div class="info-list">

            <div class="info-row">
                <span>focus</span>
                <span>web development</span>
            </div>

            <div class="info-row">
                <span>interest</span>
                <span>Linux</span>
            </div>

            <div class="info-row">
                <span>languages</span>
                <span>HTML / CSS / JS</span>
            </div>

            <div class="info-row">
                <span>editor</span>
                <span>VS Code</span>
            </div>

            <div class="info-row">
                <span>status</span>
                <span>learning</span>
            </div>

        </div>

    </div>

</div>

</section>


<!-- =========================
     SKILLS
========================= -->

<section id="skills">

<div class="container">

    <div class="section-label">
        02 / skills
    </div>

    <h2>
        Technologies
    </h2>

    <div class="skill-list">

        <div class="skill">
            HTML
        </div>

        <div class="skill">
            CSS
        </div>

        <div class="skill">
            JavaScript
        </div>

        <div class="skill">
            Git
        </div>

        <div class="skill">
            GitHub
        </div>

        <div class="skill">
            Linux
        </div>

        <div class="skill">
            Bash
        </div>

        <div class="skill">
            VS Code
        </div>

    </div>

</div>

</section>


<!-- =========================
     LINUX
========================= -->

<section id="linux">

<div class="container">

    <div class="section-label">
        03 / linux
    </div>

    <h2>
        Linux
    </h2>

    <p class="linux-intro">
        Some distributions I've explored or want
        to explore, roughly ordered by how approachable
        they are.
    </p>


    <!-- BEGINNER -->

    <div class="level">

        <div class="level-heading">

            <span class="level-number">
                01
            </span>

            <div>

                <small>BEGINNER</small>

                <h3>
                    Getting started
                </h3>

            </div>

        </div>


        <a
            class="distro"
            href="https://www.linuxmint.com/"
            target="_blank"
        >

            <div class="distro-icon">
                LM
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    Linux Mint
                </div>

                <div class="distro-description">
                    Simple and beginner friendly.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>

    </div>


    <!-- ADVANCED -->

    <div class="level">

        <div class="level-heading">

            <span class="level-number">
                02
            </span>

            <div>

                <small>ADVANCED</small>

                <h3>
                    Going deeper
                </h3>

            </div>

        </div>


        <a
            class="distro"
            href="https://endeavouros.com/"
            target="_blank"
        >

            <div class="distro-icon">
                EOS
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    EndeavourOS
                </div>

                <div class="distro-description">
                    Arch-based and lightweight.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>


        <a
            class="distro"
            href="https://archlinux.org/"
            target="_blank"
        >

            <div class="distro-icon">
                A
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    Arch Linux
                </div>

                <div class="distro-description">
                    Minimal, flexible and configurable.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>

    </div>


    <!-- EXPERT -->

    <div class="level">

        <div class="level-heading">

            <span class="level-number">
                03
            </span>

            <div>

                <small>EXPERT</small>

                <h3>
                    Going way too far
                </h3>

            </div>

        </div>


        <a
            class="distro"
            href="https://www.kisslinux.org/"
            target="_blank"
        >

            <div class="distro-icon">
                K
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    KISS Linux
                </div>

                <div class="distro-description">
                    Minimalism taken seriously.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>


        <a
            class="distro"
            href="https://guix.gnu.org/"
            target="_blank"
        >

            <div class="distro-icon">
                G
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    GNU Guix
                </div>

                <div class="distro-description">
                    Declarative system and package management.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>


        <a
            class="distro"
            href="https://www.gentoo.org/"
            target="_blank"
        >

            <div class="distro-icon">
                GE
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    Gentoo
                </div>

                <div class="distro-description">
                    Source-based and extremely customizable.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>


        <a
            class="distro"
            href="https://www.linuxfromscratch.org/"
            target="_blank"
        >

            <div class="distro-icon">
                LFS
            </div>

            <div class="distro-info">

                <div class="distro-name">
                    Linux From Scratch
                </div>

                <div class="distro-description">
                    Build a Linux system from source.
                </div>

            </div>

            <div class="distro-arrow">
                ↗
            </div>

        </a>

    </div>

</div>

</section>


<!-- =========================
     PROJECTS
========================= -->

<section id="projects">

<div class="container">

    <div class="section-label">
        04 / projects
    </div>

    <h2>
        Projects
    </h2>


    <div class="projects">


        <article class="project">

            <div class="project-number">
                01
            </div>

            <div>

                <div class="project-name">
                    kurkkusalaattikastike.com
                </div>

                <div class="project-description">
                    Personal website and developer portfolio.
                </div>

            </div>

            <a
                class="project-link"
                href="https://github.com/kurkkusalaattikastike/kurkkusalaattikastike.com"
                target="_blank"
            >
                source →
            </a>

        </article>


        <article class="project">

            <div class="project-number">
                02
            </div>

            <div>

                <div class="project-name">
                    Web experiments
                </div>

                <div class="project-description">
                    Small websites and frontend experiments.
                </div>

            </div>

            <span class="project-link">
                soon
            </span>

        </article>


        <article class="project">

            <div class="project-number">
                03
            </div>

            <div>

                <div class="project-name">
                    Linux experiments
                </div>

                <div class="project-description">
                    Learning Linux and experimenting with systems.
                </div>

            </div>

            <span class="project-link">
                soon
            </span>

        </article>


        <article class="project">

            <div class="project-number">
                04
            </div>

            <div>

                <div class="project-name">
                    More projects
                </div>

                <div class="project-description">
                    There is probably something being built.
                </div>

            </div>

            <span class="project-link">
                soon
            </span>

        </article>


    </div>

</div>

</section>


<!-- =========================
     CONTACT
========================= -->

<section id="contact" class="contact">

<div class="container">

    <div class="section-label">
        05 / contact
    </div>

    <h2>
        Get in touch.
    </h2>

    <p>
        Want to talk about programming, Linux,
        web development or a project?
    </p>

    <div class="links">

        <a
            class="simple-link"
            href="mailto:kurkkusalaattikastike@dev.com"
        >
            kurkkusalaattikastike@dev.com →
        </a>

        <a
            class="simple-link"
            href="https://github.com/kurkkusalaattikastike"
            target="_blank"
        >
            github →
        </a>

    </div>

</div>

</section>

</main>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <span>
        © 2026 kurkkusalaattikastike
    </span>

    <span>
        HTML / CSS
    </span>

</footer>


</body>
</html>
