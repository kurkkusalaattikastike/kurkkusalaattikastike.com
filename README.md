<!DOCTYPE html>
<html lang="fi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Kurkkusalaattikastike — web developer portfolio">
  <title>kurkkusalaattikastike.com</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    :root {
      --bg: #080808;
      --surface: #0f0f0f;
      --surface-2: #151515;
      --border: #252525;
      --text: #f2f2f2;
      --muted: #858585;
      --green: #b8ff5a;
      --green-dark: #79b52e;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    ::selection {
      background: var(--green);
      color: #000;
    }

    /* NAVBAR */

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
      background: rgba(8, 8, 8, 0.78);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(255,255,255,0.06);
      z-index: 100;
    }

    .logo {
      font-family: monospace;
      font-size: 15px;
      font-weight: bold;
    }

    .logo span {
      color: var(--green);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
      font-size: 14px;
      color: var(--muted);
    }

    .nav-links a {
      transition: color .2s;
    }

    .nav-links a:hover {
      color: var(--green);
    }

    /* GENERAL */

    main {
      max-width: 1100px;
      margin: auto;
      padding: 0 25px;
    }

    section {
      padding: 120px 0;
      border-bottom: 1px solid var(--border);
    }

    .section-label {
      color: var(--green);
      font-family: monospace;
      font-size: 13px;
      margin-bottom: 20px;
    }

    .section-title {
      font-size: clamp(32px, 5vw, 55px);
      letter-spacing: -2px;
      margin-bottom: 45px;
    }

    /* HERO */

    #home {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding-top: 100px;
      position: relative;
      overflow: hidden;
    }

    .hero {
      position: relative;
      z-index: 2;
    }

    .terminal-line {
      color: var(--muted);
      font-family: monospace;
      margin-bottom: 22px;
    }

    .terminal-line span {
      color: var(--green);
    }

    .hero h1 {
      max-width: 850px;
      font-size: clamp(50px, 9vw, 105px);
      line-height: .95;
      letter-spacing: -6px;
      margin-bottom: 30px;
    }

    .hero h1 .accent {
      color: var(--green);
    }

    .hero-description {
      max-width: 600px;
      color: var(--muted);
      font-size: 18px;
      margin-bottom: 38px;
    }

    .buttons {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .button {
      padding: 13px 20px;
      border: 1px solid var(--border);
      border-radius: 8px;
      font-family: monospace;
      font-size: 14px;
      transition: .2s;
    }

    .button.primary {
      background: var(--green);
      color: #000;
      border-color: var(--green);
      font-weight: bold;
    }

    .button:hover {
      transform: translateY(-3px);
      border-color: var(--green);
    }

    .button.primary:hover {
      background: #d0ff91;
    }

    /* BACKGROUND */

    .glow {
      position: absolute;
      width: 500px;
      height: 500px;
      background: var(--green);
      opacity: .06;
      filter: blur(130px);
      border-radius: 50%;
      right: -200px;
      top: 10%;
    }

    /* ABOUT */

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 70px;
    }

    .about-text {
      color: var(--muted);
      font-size: 17px;
    }

    .about-text p + p {
      margin-top: 20px;
    }

    .terminal {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      overflow: hidden;
      font-family: monospace;
      box-shadow: 0 20px 60px rgba(0,0,0,.3);
    }

    .terminal-header {
      height: 38px;
      display: flex;
      align-items: center;
      gap: 7px;
      padding: 0 14px;
      background: var(--surface-2);
      border-bottom: 1px solid var(--border);
    }

    .dot {
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: #444;
    }

    .dot:first-child {
      background: #ff5f57;
    }

    .dot:nth-child(2) {
      background: #ffbd2e;
    }

    .dot:nth-child(3) {
      background: #28c840;
    }

    .terminal-body {
      padding: 22px;
      color: #bbb;
      font-size: 14px;
    }

    .terminal-body .green {
      color: var(--green);
    }

    .terminal-body .blue {
      color: #70b7ff;
    }

    /* SKILLS */

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .skill {
      border: 1px solid var(--border);
      background: var(--surface);
      padding: 12px 17px;
      border-radius: 7px;
      font-family: monospace;
      color: #ccc;
      transition: .2s;
    }

    .skill:hover {
      color: var(--green);
      border-color: var(--green-dark);
      transform: translateY(-3px);
    }

    /* PROJECTS */

    .projects {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .project {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 28px;
      transition: .25s;
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
      font-size: 25px;
      margin: 12px 0;
    }

    .project p {
      color: var(--muted);
      margin-bottom: 22px;
    }

    .project-link {
      color: var(--green);
      font-family: monospace;
      font-size: 13px;
    }

    /* CONTACT */

    .contact {
      text-align: center;
    }

    .contact h2 {
      font-size: clamp(40px, 7vw, 80px);
      letter-spacing: -4px;
      margin-bottom: 20px;
    }

    .contact p {
      color: var(--muted);
      max-width: 500px;
      margin: 0 auto 30px;
    }

    /* FOOTER */

    footer {
      max-width: 1100px;
      margin: auto;
      padding: 30px 25px;
      display: flex;
      justify-content: space-between;
      color: #555;
      font-family: monospace;
      font-size: 12px;
    }

    footer span {
      color: var(--green);
    }

    /* RESPONSIVE */

    @media (max-width: 700px) {
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
        padding: 85px 0;
      }

      .hero h1 {
        letter-spacing: -3px;
      }

      .about-grid,
      .projects {
        grid-template-columns: 1fr;
      }

      .about-grid {
        gap: 35px;
      }

      footer {
        padding: 25px 20px;
        flex-direction: column;
        gap: 10px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <a href="#home" class="logo">
      <span>~/</span>kurkkusalaattikastike
    </a>

    <ul class="nav-links">
      <li><a href="#about">about</a></li>
      <li><a href="#skills">skills</a></li>
      <li><a href="#projects">projects</a></li>
      <li><a href="#contact">contact</a></li>
    </ul>
  </nav>


  <main>

    <!-- HERO -->

    <section id="home">

      <div class="glow"></div>

      <div class="hero">

        <div class="terminal-line">
          <span>~/</span> hello_world
        </div>

        <h1>
          I build<br>
          <span class="accent">things.</span>
        </h1>

        <p class="hero-description">
          I'm a developer who enjoys building websites,
          experimenting with code and turning random ideas
          into something that actually works.
        </p>

        <div class="buttons">
          <a href="#projects" class="button primary">
            &gt; view_projects
          </a>

          <a href="#about" class="button">
            &gt; about_me
          </a>
        </div>

      </div>
    </section>


    <!-- ABOUT -->

    <section id="about">

      <div class="section-label">01 — ABOUT</div>

      <h2 class="section-title">Who am I?</h2>

      <div class="about-grid">

        <div class="about-text">

          <p>
            Hey! I'm <strong>kurkkusalaattikastike</strong>.
            I'm interested in web development, programming
            and building cool stuff on the internet.
          </p>

          <p>
            This website is my little corner of the web where
            I can show what I've been working on and experiment
            with new ideas.
          </p>

          <p>
            I like simple interfaces, clean code and projects
            that are actually fun to build.
          </p>

        </div>


        <div class="terminal">

          <div class="terminal-header">
            <div class="dot"></div>
            <div class="dot"></div>
            <div class="dot"></div>
          </div>

          <div class="terminal-body">

            <div>
              <span class="green">$</span>
              whoami
            </div>

            <br>

            <div>
              > developer
            </div>

            <div>
              > web enthusiast
            </div>

            <div>
              > professional cucumber sauce
            </div>

            <br>

            <div>
              <span class="green">$</span>
              status
            </div>

            <div>
              > <span class="blue">building...</span>
            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- SKILLS -->

    <section id="skills">

      <div class="section-label">02 — SKILLS</div>

      <h2 class="section-title">Stuff I use.</h2>

      <div class="skills">

        <div class="skill">HTML</div>
        <div class="skill">CSS</div>
        <div class="skill">JavaScript</div>
        <div class="skill">Git</div>
        <div class="skill">GitHub</div>
        <div class="skill">VS Code</div>
        <div class="skill">Web Development</div>
        <div class="skill">UI / UX</div>

      </div>

    </section>


    <!-- PROJECTS -->

    <section id="projects">

      <div class="section-label">03 — PROJECTS</div>

      <h2 class="section-title">Things I've built.</h2>

      <div class="projects">

        <article class="project">

          <div class="project-number">01</div>

          <h3>kurkkusalaattikastike.com</h3>

          <p>
            My personal developer website.
            Built from scratch and hosted using GitHub Pages.
          </p>

          <a
            href="https://github.com/"
            target="_blank"
            class="project-link"
          >
            &gt; github →
          </a>

        </article>


        <article class="project">

          <div class="project-number">02</div>

          <h3>Coming soon...</h3>

          <p>
            Something cool is currently being built.
            Check back later.
          </p>

          <a href="#contact" class="project-link">
            &gt; stay tuned →
          </a>

        </article>


        <article class="project">

          <div class="project-number">03</div>

          <h3>Another project</h3>

          <p>
            Add your next project here.
            Replace this text with your own description.
          </p>

          <a href="#" class="project-link">
            &gt; view project →
          </a>

        </article>


        <article class="project">

          <div class="project-number">04</div>

          <h3>Experiment</h3>

          <p>
            Random experiments, websites and
            other things I've made.
          </p>

          <a href="#" class="project-link">
            &gt; explore →
          </a>

        </article>

      </div>

    </section>


    <!-- CONTACT -->

    <section id="contact" class="contact">

      <div class="section-label">04 — CONTACT</div>

      <h2>Let's build.</h2>

      <p>
        Have an idea, project or just want to say hi?
        You can find me online.
      </p>

      <div class="buttons" style="justify-content:center;">

        <a
          href="https://github.com/"
          target="_blank"
          class="button primary"
        >
          GitHub
        </a>

        <a
          href="mailto:your@email.com"
          class="button"
        >
          Email
        </a>

      </div>

    </section>

  </main>


  <footer>
    <div>© 2026 <span>kurkkusalaattikastike</span></div>
    <div>built with &lt;3 and questionable amounts of CSS</div>
  </footer>


  <script>

    // Smooth navigation
    document.querySelectorAll('a[href^="#"]').forEach(link => {

      link.addEventListener("click", function(e) {

        const target = document.querySelector(
          this.getAttribute("href")
        );

        if (target) {
          e.preventDefault();

          target.scrollIntoView({
            behavior: "smooth"
          });
        }

      });

    });


    // Keyboard shortcuts
    document.addEventListener("keydown", (event) => {

      // Don't trigger shortcuts while typing
      if (
        event.target.tagName === "INPUT" ||
        event.target.tagName === "TEXTAREA"
      ) return;

      const keys = {
        "h": "#home",
        "a": "#about",
        "s": "#skills",
        "p": "#projects",
        "c": "#contact"
      };

      const target = keys[event.key.toLowerCase()];

      if (target) {
        document.querySelector(target)?.scrollIntoView({
          behavior: "smooth"
        });
      }

    });


    // Tiny console easter egg
    console.log(
      "%c🥒 kurkkusalaattikastike.com",
      "color:#b8ff5a;font-size:20px;font-weight:bold;"
    );

    console.log(
      "%cWelcome, fellow developer.",
      "color:#aaa;font-size:13px;"
    );

  </script>

</body>
</html>
