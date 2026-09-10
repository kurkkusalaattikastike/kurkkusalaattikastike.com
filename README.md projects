<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <meta
    name="description"
    content="kurkkusalaattikastike — developer, web developer and Linux enthusiast."
  >

  <title>kurkkusalaattikastike</title>

  <style>
    /* =========================================================
       RESET
    ========================================================= */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: #070707;
      color: #eeeeee;
      font-family:
        Inter,
        ui-sans-serif,
        system-ui,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;

      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font: inherit;
    }

    ::selection {
      background: #b8ff5a;
      color: #000;
    }


    /* =========================================================
       VARIABLES
    ========================================================= */

    :root {
      --bg: #070707;
      --surface: #0d0d0d;
      --surface2: #121212;

      --border: #242424;
      --border-light: #303030;

      --text: #eeeeee;
      --muted: #858585;
      --muted2: #555555;

      --green: #b8ff5a;
      --green-dark: #7fb638;

      --blue: #58b8ff;
      --purple: #a77bff;
      --orange: #ffb84d;
    }


    /* =========================================================
       BACKGROUND
    ========================================================= */

    .background-glow {
      position: fixed;

      width: 600px;
      height: 600px;

      top: -250px;
      right: -200px;

      background: #b8ff5a;

      opacity: 0.035;

      filter: blur(150px);

      border-radius: 50%;

      pointer-events: none;

      z-index: -1;
    }

    .grid {
      position: fixed;

      inset: 0;

      background-image:
        linear-gradient(
          rgba(255,255,255,0.025) 1px,
          transparent 1px
        ),
        linear-gradient(
          90deg,
          rgba(255,255,255,0.025) 1px,
          transparent 1px
        );

      background-size: 50px 50px;

      mask-image:
        linear-gradient(
          to bottom,
          black,
          transparent 75%
        );

      pointer-events: none;

      z-index: -2;
    }


    /* =========================================================
       NAVIGATION
    ========================================================= */

    nav {
      position: fixed;

      top: 0;
      left: 0;

      width: 100%;
      height: 70px;

      display: flex;
      align-items: center;
      justify-content: space-between;

      padding: 0 7%;

      background: rgba(7,7,7,0.75);

      backdrop-filter: blur(18px);

      border-bottom: 1px solid rgba(255,255,255,0.06);

      z-index: 1000;
    }

    .logo {
      font-family: monospace;
      font-size: 14px;
      font-weight: 700;
    }

    .logo-symbol {
      color: var(--green);
    }

    .nav-links {
      display: flex;
      gap: 28px;

      list-style: none;

      color: var(--muted);

      font-family: monospace;
      font-size: 13px;
    }

    .nav-links a {
      transition: 0.2s;
    }

    .nav-links a:hover {
      color: var(--green);
    }

    .shortcut {
      color: #444;
      margin-left: 5px;
    }


    /* =========================================================
       MAIN
    ========================================================= */

    main {
      max-width: 1100px;

      margin: auto;

      padding: 0 25px;
    }

    section {
      padding: 130px 0;

      border-bottom: 1px solid var(--border);
    }

    .section-label {
      color: var(--green);

      font-family: monospace;

      font-size: 12px;

      letter-spacing: 1px;

      margin-bottom: 18px;
    }

    .section-title {
      font-size: clamp(40px, 6vw, 65px);

      line-height: 1;

      letter-spacing: -3px;

      margin-bottom: 45px;
    }


    /* =========================================================
       HERO
    ========================================================= */

    #home {
      min-height: 100vh;

      display: flex;
      align-items: center;

      padding-top: 120px;

      position: relative;
    }

    .hero {
      max-width: 900px;
    }

    .terminal-command {
      font-family: monospace;

      color: var(--muted);

      margin-bottom: 25px;
    }

    .terminal-command span {
      color: var(--green);
    }

    .hero h1 {
      font-size: clamp(55px, 10vw, 115px);

      line-height: 0.9;

      letter-spacing: -7px;

      margin-bottom: 35px;
    }

    .hero h1 .green {
      color: var(--green);
    }

    .hero-description {
      max-width: 650px;

      color: var(--muted);

      font-size: 18px;

      margin-bottom: 35px;
    }

    .buttons {
      display: flex;

      gap: 12px;

      flex-wrap: wrap;
    }

    .button {
      padding: 12px 18px;

      border: 1px solid var(--border-light);

      background: var(--surface);

      border-radius: 7px;

      font-family: monospace;

      font-size: 13px;

      transition: 0.2s;
    }

    .button:hover {
      border-color: var(--green);

      transform: translateY(-3px);
    }

    .button.primary {
      background: var(--green);

      color: #000;

      border-color: var(--green);

      font-weight: bold;
    }

    .button.primary:hover {
      background: #d0ff91;
    }


    /* =========================================================
       ABOUT
    ========================================================= */

    .about-grid {
      display: grid;

      grid-template-columns: 1fr 1fr;

      gap: 70px;
    }

    .about-text {
      color: var(--muted);

      font-size: 17px;
    }

    .about-text p {
      margin-bottom: 20px;
    }

    .about-text strong {
      color: white;
    }


    /* TERMINAL */

    .terminal {
      background: #0b0b0b;

      border: 1px solid var(--border);

      border-radius: 10px;

      overflow: hidden;

      box-shadow:
        0 30px 80px rgba(0,0,0,0.35);
    }

    .terminal-header {
      height: 38px;

      display: flex;
      align-items: center;

      gap: 7px;

      padding: 0 14px;

      background: #111;

      border-bottom: 1px solid var(--border);
    }

    .terminal-dot {
      width: 9px;
      height: 9px;

      border-radius: 50%;
    }

    .terminal-dot.red {
      background: #ff5f57;
    }

    .terminal-dot.yellow {
      background: #ffbd2e;
    }

    .terminal-dot.green {
      background: #28c840;
    }

    .terminal-body {
      padding: 25px;

      font-family: monospace;

      font-size: 13px;

      color: #aaa;
    }

    .terminal-green {
      color: var(--green);
    }

    .terminal-blue {
      color: var(--blue);
    }

    .terminal-purple {
      color: var(--purple);
    }

    .terminal-line {
      margin-bottom: 7px;
    }


    /* =========================================================
       SKILLS
    ========================================================= */

    .skills {
      display: flex;

      flex-wrap: wrap;

      gap: 10px;
    }

    .skill {
      padding: 11px 16px;

      background: var(--surface);

      border: 1px solid var(--border);

      border-radius: 7px;

      font-family: monospace;

      font-size: 13px;

      color: #ccc;

      transition: 0.2s;
    }

    .skill:hover {
      color: var(--green);

      border-color: var(--green-dark);

      transform: translateY(-3px);
    }


    /* =========================================================
       LINUX
    ========================================================= */

    .linux-description {
      color: var(--muted);

      margin-top: -25px;

      margin-bottom: 55px;

      font-size: 17px;
    }

    .linux-level {
      margin-bottom: 70px;
    }

    .level-header {
      display: flex;

      align-items: center;

      gap: 18px;

      margin-bottom: 18px;
    }

    .level-number {
      color: var(--green);

      font-family: monospace;

      font-size: 13px;
    }

    .level-tag {
      color: #555;

      font-family: monospace;

      font-size: 10px;

      letter-spacing: 2px;
    }

    .level-header h3 {
      font-size: 25px;
    }


    /* LINUX CARDS */

    .linux-card {
      display: flex;

      align-items: center;

      gap: 20px;

      padding: 18px;

      margin-bottom: 10px;

      background: var(--surface);

      border: 1px solid var(--border);

      border-radius: 10px;

      transition:
        transform 0.2s,
        border-color 0.2s,
        background 0.2s;
    }

    .linux-card:hover {
      transform: translateX(7px);

      background: #111;

      border-color: #444;
    }


    /* LOGOS */

    .distro-logo {
      width: 58px;
      height: 58px;

      flex-shrink: 0;

      display: flex;

      align-items: center;
      justify-content: center;

      border-radius: 14px;

      font-family: monospace;

      font-weight: bold;

      overflow: hidden;
    }

    .distro-logo svg {
      width: 42px;
      height: 42px;
    }


    /* MINT */

    .mint-logo {
      background: #87cf3e;

      border-radius: 50%;
    }

    .mint-logo svg {
      fill: white;
    }


    /* ENDEAVOUR */

    .endeavour-logo {
      background: #282039;
    }

    .endeavour-logo svg {
      stroke: #a78bfa;
      fill: none;
    }


    /* ARCH */

    .arch-logo {
      background: #102d3c;
    }

    .arch-logo svg {
      fill: #1793d1;
    }


    /* KISS */

    .kiss-logo {
      background: #eeeeee;

      color: #111;

      font-size: 23px;
    }


    /* GUIX */

    .guix-logo {
      background: #e9a800;

      color: #111;

      font-size: 23px;
    }


    /* GENTOO */

    .gentoo-logo {
      background: #3e365a;
    }

    .gentoo-logo svg {
      fill: #b7a5df;
    }


    /* LFS */

    .lfs-logo {
      background: #151515;

      border: 1px solid #3a3a3a;

      color: var(--green);

      font-size: 12px;
    }


    .distro-info {
      flex: 1;
    }

    .distro-info h4 {
      font-size: 18px;

      margin-bottom: 3px;
    }

    .distro-info p {
      color: var(--muted);

      font-size: 13px;
    }

    .arrow {
      color: #444;

      font-size: 20px;

      transition: 0.2s;
    }

    .linux-card:hover .arrow {
      color: var(--green);

      transform:
        translate(3px,-3px);
    }


    /* =========================================================
       PROJECTS
    ========================================================= */

    .projects {
      display: grid;

      grid-template-columns:
        repeat(2, 1fr);

      gap: 15px;
    }

    .project {
      padding: 28px;

      background: var(--surface);

      border: 1px solid var(--border);

      border-radius: 10px;

      transition: 0.2s;
    }

    .project:hover {
      transform: translateY(-5px);

      border-color: #444;
    }

    .project-number {
      color: var(--green);

      font-family: monospace;

      font-size: 12px;
    }

    .project h3 {
      font-size: 23px;

      margin: 12px 0;
    }

    .project p {
      color: var(--muted);

      margin-bottom: 20px;
    }

    .project-link {
      color: var(--green);

      font-family: monospace;

      font-size: 13px;
    }


    /* =========================================================
       CONTACT
    ========================================================= */

    .contact {
      text-align: center;

      border-bottom: none;
    }

    .contact h2 {
      font-size: clamp(50px, 9vw, 95px);

      letter-spacing: -5px;

      line-height: 1;

      margin-bottom: 25px;
    }

    .contact h2 span {
      color: var(--green);
    }

    .contact-description {
      max-width: 500px;

      margin: auto;

      color: var(--muted);

      margin-bottom: 30px;
    }

    .contact .buttons {
      justify-content: center;
    }


    /* =========================================================
       FOOTER
    ========================================================= */

    footer {
      max-width: 1100px;

      margin: auto;

      padding: 30px 25px;

      display: flex;

      justify-content: space-between;

      color: #444;

      font-family: monospace;

      font-size: 11px;
    }

    footer .green {
      color: var(--green);
    }


    /* =========================================================
       SCROLL ANIMATION
    ========================================================= */

    .reveal {
      opacity: 0;

      transform: translateY(25px);

      transition:
        opacity 0.7s ease,
        transform 0.7s ease;
    }

    .reveal.visible {
      opacity: 1;

      transform: translateY(0);
    }


    /* =========================================================
       MOBILE
    ========================================================= */

    @media (max-width: 750px) {

      nav {
        padding: 0 20px;
      }

      .nav-links {
        display: none;
      }

      main {
        padding: 0 20px;
      }

      section {
        padding: 90px 0;
      }

      .hero h1 {
        letter-spacing: -4px;
      }

      .about-grid {
        grid-template-columns: 1fr;

        gap: 35px;
      }

      .projects {
        grid-template-columns: 1fr;
      }

      .linux-card {
        padding: 14px;
      }

      .distro-logo {
        width: 48px;
        height: 48px;
      }

      .distro-info p {
        font-size: 12px;
      }

      footer {
        flex-direction: column;

        gap: 10px;
      }
    }


    @media (max-width: 450px) {

      .hero h1 {
        font-size: 58px;
      }

      .distro-info h4 {
        font-size: 16px;
      }

      .distro-info p {
        display: none;
      }

      .section-title {
        letter-spacing: -2px;
      }
    }

  </style>
</head>


<body>

  <div class="background-glow"></div>

  <div class="grid"></div>


  <!-- =======================================================
       NAV
  ======================================================== -->

  <nav>

    <a href="#home" class="logo">
      <span class="logo-symbol">~/</span>
      kurkkusalaattikastike
    </a>

    <ul class="nav-links">

      <li>
        <a href="#about">
          about
          <span class="shortcut">A</span>
        </a>
      </li>

      <li>
        <a href="#skills">
          skills
          <span class="shortcut">S</span>
        </a>
      </li>

      <li>
        <a href="#linux">
          linux
          <span class="shortcut">L</span>
        </a>
      </li>

      <li>
        <a href="#projects">
          projects
          <span class="shortcut">P</span>
        </a>
      </li>

      <li>
        <a href="#contact">
          contact
          <span class="shortcut">C</span>
        </a>
      </li>

    </ul>

  </nav>


  <main>


    <!-- =====================================================
         HERO
    ====================================================== -->

    <section id="home">

      <div class="hero">

        <div class="terminal-command">
          <span>$</span> whoami
        </div>

        <h1>
          I build<br>
          <span class="green">things.</span>
        </h1>

        <p class="hero-description">
          Web developer, programmer and Linux enthusiast.
          I enjoy building websites, experimenting with code
          and breaking things just to figure out how they work.
        </p>

        <div class="buttons">

          <a
            href="#projects"
            class="button primary"
          >
            &gt; view_projects
          </a>

          <a
            href="#about"
            class="button"
          >
            &gt; about_me
          </a>

        </div>

      </div>

    </section>



    <!-- =====================================================
         ABOUT
    ====================================================== -->

    <section id="about">

      <div class="section-label">
        01 — ABOUT
      </div>

      <h2 class="section-title">
        Who am I?
      </h2>

      <div class="about-grid reveal">


        <div class="about-text">

          <p>
            Hey! I'm
            <strong>kurkkusalaattikastike</strong>.
          </p>

          <p>
            I'm interested in web development,
            programming, Linux and everything
            happening behind the scenes of modern
            computers.
          </p>

          <p>
            I like building things from scratch,
            learning how systems work and
            experimenting with new technologies.
          </p>

          <p>
            This website is my little corner
            of the internet.
          </p>

        </div>


        <!-- TERMINAL -->

        <div class="terminal">

          <div class="terminal-header">

            <div class="terminal-dot red"></div>
            <div class="terminal-dot yellow"></div>
            <div class="terminal-dot green"></div>

          </div>


          <div class="terminal-body">

            <div class="terminal-line">
              <span class="terminal-green">$</span>
              neofetch
            </div>

            <br>

            <div class="terminal-line">
              user:
              <span class="terminal-green">
                kurkkusalaattikastike
              </span>
            </div>

            <div class="terminal-line">
              role:
              <span class="terminal-blue">
                web developer
              </span>
            </div>

            <div class="terminal-line">
              os:
              <span class="terminal-purple">
                Linux
              </span>
            </div>

            <div class="terminal-line">
              shell:
              <span class="terminal-green">
                bash / zsh
              </span>
            </div>

            <div class="terminal-line">
              status:
              <span class="terminal-green">
                building...
              </span>
            </div>

            <br>

            <div class="terminal-line">
              <span class="terminal-green">$</span>
              echo "hello world"
            </div>

            <div class="terminal-line">
              hello world 👋
            </div>

          </div>

        </div>

      </div>

    </section>



    <!-- =====================================================
         SKILLS
    ====================================================== -->

    <section id="skills">

      <div class="section-label">
        02 — SKILLS
      </div>

      <h2 class="section-title">
        What I use.
      </h2>


      <div class="skills reveal">

        <div class="skill">HTML</div>

        <div class="skill">CSS</div>

        <div class="skill">JavaScript</div>

        <div class="skill">Git</div>

        <div class="skill">GitHub</div>

        <div class="skill">Linux</div>

        <div class="skill">Bash</div>

        <div class="skill">Terminal</div>

        <div class="skill">VS Code</div>

        <div class="skill">Web Development</div>

        <div class="skill">UI / UX</div>

      </div>

    </section>



    <!-- =====================================================
         LINUX
    ====================================================== -->

    <section id="linux">

      <div class="section-label">
        03 — LINUX
      </div>

      <h2 class="section-title">
        Linux journey.
      </h2>

      <p class="linux-description">
        From beginner-friendly distributions to
        building a complete system from source.
      </p>



      <!-- BEGINNER -->

      <div class="linux-level reveal">

        <div class="level-header">

          <span class="level-number">
            01
          </span>

          <div>

            <span class="level-tag">
              BEGINNER
            </span>

            <h3>
              Getting started
            </h3>

          </div>

        </div>


        <!-- MINT -->

        <a
          class="linux-card"
          href="https://www.linuxmint.com/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo mint-logo">

            <svg
              viewBox="0 0 100 100"
              xmlns="http://www.w3.org/2000/svg"
            >

              <path d="
                M28 70
                V42
                C28 27 39 20 50 20
                C61 20 72 27 72 42
                V70
                H62
                V43
                C62 35 58 31 52 31
                H48
                C42 31 38 35 38 43
                V70
                Z
              "/>

            </svg>

          </div>


          <div class="distro-info">

            <h4>
              Linux Mint
            </h4>

            <p>
              Friendly, comfortable and easy to get started with.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>

      </div>



      <!-- ADVANCED -->

      <div class="linux-level reveal">

        <div class="level-header">

          <span class="level-number">
            02
          </span>

          <div>

            <span class="level-tag">
              ADVANCED
            </span>

            <h3>
              Going deeper
            </h3>

          </div>

        </div>


        <!-- ENDEAVOUR -->

        <a
          class="linux-card"
          href="https://endeavouros.com/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo endeavour-logo">

            <svg
              viewBox="0 0 100 100"
              xmlns="http://www.w3.org/2000/svg"
            >

              <circle
                cx="50"
                cy="50"
                r="34"
                stroke-width="5"
              />

              <path
                d="M32 67 L50 30 L68 67"
                stroke-width="6"
              />

              <path
                d="M39 55 H61"
                stroke-width="5"
              />

            </svg>

          </div>


          <div class="distro-info">

            <h4>
              EndeavourOS
            </h4>

            <p>
              An Arch-based, terminal-centric Linux experience.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>



        <!-- ARCH -->

        <a
          class="linux-card"
          href="https://archlinux.org/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo arch-logo">

            <svg
              viewBox="0 0 100 100"
              xmlns="http://www.w3.org/2000/svg"
            >

              <path
                d="
                  M50 10
                  L20 75
                  L50 60
                  L80 90
                  L50 10
                  Z
                "
              />

              <path
                d="
                  M50 38
                  L42 58
                  L50 54
                  L58 66
                  Z
                "
              />

            </svg>

          </div>


          <div class="distro-info">

            <h4>
              Arch Linux
            </h4>

            <p>
              Minimal, flexible and built around user configuration.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>

      </div>



      <!-- EXPERT -->

      <div class="linux-level reveal">

        <div class="level-header">

          <span class="level-number">
            03
          </span>

          <div>

            <span class="level-tag">
              EXPERT
            </span>

            <h3>
              Into the source
            </h3>

          </div>

        </div>



        <!-- KISS -->

        <a
          class="linux-card"
          href="https://kisslinux.org/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo kiss-logo">
            K
          </div>


          <div class="distro-info">

            <h4>
              KISS Linux
            </h4>

            <p>
              Simple, minimal and extremely hands-on.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>



        <!-- GUIX -->

        <a
          class="linux-card"
          href="https://guix.gnu.org/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo guix-logo">
            G
          </div>


          <div class="distro-info">

            <h4>
              GNU Guix
            </h4>

            <p>
              Declarative and reproducible system management.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>



        <!-- GENTOO -->

        <a
          class="linux-card"
          href="https://www.gentoo.org/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo gentoo-logo">

            <svg
              viewBox="0 0 100 100"
              xmlns="http://www.w3.org/2000/svg"
            >

              <path
                d="
                  M20 50
                  L55 15
                  L80 35
                  L45 85
                  L20 65
                  Z
                "
              />

            </svg>

          </div>


          <div class="distro-info">

            <h4>
              Gentoo
            </h4>

            <p>
              Highly customizable Linux with a source-based ecosystem.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>



        <!-- LFS -->

        <a
          class="linux-card"
          href="https://www.linuxfromscratch.org/"
          target="_blank"
          rel="noopener"
        >

          <div class="distro-logo lfs-logo">
            LFS
          </div>


          <div class="distro-info">

            <h4>
              Linux From Scratch
            </h4>

            <p>
              Build your own Linux system from source, step by step.
            </p>

          </div>


          <span class="arrow">
            ↗
          </span>

        </a>

      </div>

    </section>



    <!-- =====================================================
         PROJECTS
    ====================================================== -->

    <section id="projects">

      <div class="section-label">
        04 — PROJECTS
      </div>

      <h2 class="section-title">
        Things I've built.
      </h2>


      <div class="projects reveal">


        <article class="project">

          <div class="project-number">
            01
          </div>

          <h3>
            kurkkusalaattikastike.com
          </h3>

          <p>
            My personal developer portfolio,
            built from scratch with HTML, CSS and JavaScript.
          </p>

          <a
            href="https://kurkkusalaattikastike.com"
            class="project-link"
          >
            &gt; open website →
          </a>

        </article>



        <article class="project">

          <div class="project-number">
            02
          </div>

          <h3>
            Linux experiments
          </h3>

          <p>
            Experiments with Linux distributions,
            terminals, shells and system configuration.
          </p>

          <a
            href="#linux"
            class="project-link"
          >
            &gt; explore linux →
          </a>

        </article>



        <article class="project">

          <div class="project-number">
            03
          </div>

          <h3>
            Web experiments
          </h3>

          <p>
            Random websites, interfaces and
            programming experiments.
          </p>

          <a
            href="#contact"
            class="project-link"
          >
            &gt; more soon →
          </a>

        </article>



        <article class="project">

          <div class="project-number">
            04
          </div>

          <h3>
            Coming soon...
          </h3>

          <p>
            Something new is currently being built.
          </p>

          <a
            href="#contact"
            class="project-link"
          >
            &gt; stay tuned →
          </a>

        </article>

      </div>

    </section>



    <!-- =====================================================
         CONTACT
    ====================================================== -->

    <section id="contact" class="contact">

      <div class="section-label">
        05 — CONTACT
      </div>

      <h2>
        Let's <span>build.</span>
      </h2>

      <p class="contact-description">
        Got an idea, project or just want to say hello?
        Send me an email or find me online.
      </p>


      <div class="buttons">

        <a
          href="mailto:kurkkusalaattikastike@dev.com"
          class="button primary"
        >
          &gt; email_me
        </a>


        <a
          href="https://github.com/"
          target="_blank"
          rel="noopener"
          class="button"
        >
          GitHub ↗
        </a>

      </div>

    </section>

  </main>



  <!-- =======================================================
       FOOTER
  ======================================================== -->

  <footer>

    <div>
      © 2026
      <span class="green">
        kurkkusalaattikastike
      </span>
    </div>

    <div>
      built with &lt;3 and questionable amounts of CSS
    </div>

  </footer>



  <!-- =======================================================
       JAVASCRIPT
  ======================================================== -->

  <script>

    /*
      Smooth scrolling
    */

    document
      .querySelectorAll('a[href^="#"]')
      .forEach(link => {

        link.addEventListener("click", event => {

          const target =
            document.querySelector(
              link.getAttribute("href")
            );

          if (!target) return;

          event.preventDefault();

          target.scrollIntoView({
            behavior: "smooth"
          });

        });

      });



    /*
      Scroll reveal animation
    */

    const observer =
      new IntersectionObserver(
        entries => {

          entries.forEach(entry => {

            if (entry.isIntersecting) {

              entry.target.classList.add("visible");

            }

          });

        },

        {
          threshold: 0.12
        }

      );


    document
      .querySelectorAll(".reveal")
      .forEach(element => {

        observer.observe(element);

      });



    /*
      Keyboard navigation

      A = About
      S = Skills
      L = Linux
      P = Projects
      C = Contact
      H = Home
    */

    const shortcuts = {

      h: "#home",
      a: "#about",
      s: "#skills",
      l: "#linux",
      p: "#projects",
      c: "#contact"

    };


    document.addEventListener(
      "keydown",
      event => {

        if (
          event.target.tagName === "INPUT" ||
          event.target.tagName === "TEXTAREA"
        ) {
          return;
        }


        const target =
          shortcuts[
            event.key.toLowerCase()
          ];


        if (!target) return;


        document
          .querySelector(target)
          ?.scrollIntoView({
            behavior: "smooth"
          });

      }
    );



    /*
      Console easter egg
    */

    console.log(
      "%c🥒 kurkkusalaattikastike.com",
      `
        color:#b8ff5a;
        font-size:20px;
        font-weight:bold;
      `
    );

    console.log(
      "%cWelcome, fellow developer.",
      `
        color:#888;
        font-size:13px;
      `
    );

  </script>

</body>
</html>
