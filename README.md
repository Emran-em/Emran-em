<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>MD Waseem | Senior DevOps Engineer & Cloud Architect</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #050814;
      --bg-alt: #0b1020;
      --card: #111827;
      --accent: #00d8ff;
      --accent2: #f97316;
      --accent3: #22c55e;
      --text: #e5e7eb;
      --muted: #9ca3af;
      --border: #1f2937;
      --shadow: 0 18px 45px rgba(0, 0, 0, 0.55);
      --radius-lg: 18px;
      --radius-xl: 26px;
      --max-width: 1100px;
      --transition: all 0.25s ease-out;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      background: radial-gradient(circle at top, #111827 0, #020617 50%, #000 100%);
      color: var(--text);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: var(--accent);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 40px 16px 80px;
    }

    section {
      margin-bottom: 40px;
    }

    .hero {
      text-align: center;
      margin-bottom: 48px;
    }

    .hero-card {
      background: radial-gradient(circle at top left, #0f172a, #020617);
      border-radius: var(--radius-xl);
      padding: 28px 16px 32px;
      box-shadow: var(--shadow);
      border: 1px solid rgba(148, 163, 184, 0.15);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: -40%;
      background: conic-gradient(
        from 140deg,
        rgba(56, 189, 248, 0.4),
        transparent 35%,
        rgba(251, 146, 60, 0.4),
        transparent 65%,
        rgba(52, 211, 153, 0.4)
      );
      opacity: 0.25;
      filter: blur(36px);
      z-index: -1;
      animation: spin 30s linear infinite;
    }

    .hero h1 {
      font-size: clamp(2rem, 3vw, 2.6rem);
      margin-bottom: 4px;
    }

    .hero h1 span {
      background: linear-gradient(90deg, #22c55e, #0ea5e9, #f97316);
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero h2 {
      font-weight: 500;
      font-size: 1.1rem;
      color: var(--muted);
      margin-bottom: 20px;
    }

    .hero img.hero-typing {
      max-width: 100%;
      margin-bottom: 18px;
    }

    .hero img.hero-gif {
      max-width: min(100%, 900px);
      border-radius: 20px;
      border: 1px solid rgba(148, 163, 184, 0.3);
      box-shadow: var(--shadow);
    }

    /* ABOUT */

    .about {
      display: grid;
      grid-template-columns: minmax(0, 2fr) minmax(0, 1.4fr);
      gap: 24px;
      align-items: center;
    }

    .about-text {
      background: var(--card);
      border-radius: var(--radius-lg);
      padding: 22px 20px;
      border: 1px solid var(--border);
      box-shadow: 0 16px 35px rgba(15, 23, 42, 0.75);
    }

    .section-title {
      font-size: 1.35rem;
      margin-bottom: 10px;
    }

    .section-subtitle {
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.22em;
      color: var(--muted);
      margin-bottom: 6px;
    }

    .about-text p + p {
      margin-top: 10px;
    }

    .about-gif {
      text-align: center;
    }

    .about-gif img {
      max-width: 100%;
      border-radius: var(--radius-lg);
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
    }

    /* MISSION */

    .mission-card {
      background: #020617;
      border-radius: var(--radius-lg);
      border: 1px solid var(--border);
      padding: 18px 20px 14px;
      box-shadow: 0 16px 40px rgba(15, 23, 42, 0.9);
      font-family: "JetBrains Mono", ui-monospace, SFMono-Regular, Menlo,
        Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      font-size: 0.85rem;
      overflow-x: auto;
    }

    .mission-card pre {
      margin: 0;
      white-space: pre;
    }

    .mission-card code {
      color: #e5e7eb;
    }

    /* TECH STACK MARQUEE */

    .tech-section {
      background: var(--card);
      border-radius: var(--radius-lg);
      padding: 20px 18px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
    }

    .tech-marquee-wrapper {
      overflow: hidden;
      position: relative;
      margin-top: 14px;
    }

    .tech-marquee-track {
      display: flex;
      width: max-content;
      animation: marquee 26s linear infinite;
      gap: 32px;
      align-items: center;
    }

    .tech-marquee-track img {
      height: 54px;
      filter: drop-shadow(0 10px 18px rgba(0, 0, 0, 0.7));
      transition: transform 0.23s ease-out, filter 0.23s ease-out;
    }

    .tech-marquee-track img:hover {
      transform: translateY(-4px) scale(1.06);
      filter: drop-shadow(0 14px 26px rgba(56, 189, 248, 0.55));
    }

    /* HIGHLIGHTS */

    .highlights-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 18px;
    }

    .card {
      background: var(--card);
      border-radius: var(--radius-lg);
      padding: 18px 18px 16px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top, rgba(56, 189, 248, 0.15), transparent 60%);
      opacity: 0;
      transition: opacity 0.25s ease-out;
      z-index: -1;
    }

    .card:hover::before {
      opacity: 1;
    }

    .card h3 {
      font-size: 1rem;
      margin-bottom: 6px;
    }

    .metric {
      font-size: 0.85rem;
      color: var(--accent2);
      margin-bottom: 6px;
    }

    .card ul {
      padding-left: 18px;
      font-size: 0.9rem;
      color: var(--muted);
    }

    .card ul li + li {
      margin-top: 4px;
    }

    /* COMPETENCIES */

    .table-like {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 14px;
      margin-top: 14px;
    }

    .table-col {
      background: var(--card);
      border-radius: var(--radius-lg);
      padding: 12px 12px 10px;
      border: 1px solid var(--border);
      font-size: 0.88rem;
    }

    .table-col h4 {
      font-size: 0.9rem;
      margin-bottom: 6px;
      color: var(--accent);
    }

    .table-col ul {
      padding-left: 16px;
      color: var(--muted);
    }

    .table-col ul li + li {
      margin-top: 2px;
    }

    /* STATS */

    .center {
      text-align: center;
    }

    .stats img {
      max-width: 100%;
      margin: 4px;
    }

    .snake img {
      max-width: 100%;
      border-radius: var(--radius-lg);
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
    }

    /* CONTACT */

    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 16px;
      flex-wrap: wrap;
      margin-top: 12px;
    }

    .btn-pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 16px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      background: linear-gradient(135deg, #020617, #111827);
      color: var(--text);
      font-size: 0.9rem;
      font-weight: 500;
      box-shadow: 0 10px 25px rgba(15, 23, 42, 0.8);
      transition: var(--transition);
      text-decoration: none;
    }

    .btn-pill span.icon {
      font-size: 1.05rem;
    }

    .btn-pill:hover {
      transform: translateY(-2px);
      border-color: var(--accent);
      box-shadow: 0 14px 30px rgba(56, 189, 248, 0.55);
    }

    /* UTIL */

    .muted {
      color: var(--muted);
    }

    blockquote {
      border-left: 3px solid var(--accent);
      padding-left: 12px;
      color: var(--muted);
      font-style: italic;
    }

    hr {
      border: none;
      border-top: 1px solid rgba(31, 41, 55, 0.9);
      margin: 22px 0;
    }

    /* RESPONSIVE */

    @media (max-width: 800px) {
      main {
        padding-top: 26px;
      }
      .about {
        grid-template-columns: minmax(0, 1fr);
      }
      .about-gif {
        order: -1;
      }
      .hero-card {
        padding-inline: 10px;
      }
    }

    /* ANIMATIONS */

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }

    @keyframes marquee {
      from {
        transform: translateX(0);
      }
      to {
        transform: translateX(-50%);
      }
    }
  </style>
</head>
<body>
  <main>
    <!-- HERO -->
    <section class="hero">
      <div class="hero-card">
        <h1>🚀 Hey there! I'm <span>MD Waseem</span></h1>
        <h2>Senior DevOps Engineer &amp; Cloud Architect ⚡</h2>

        <img
          class="hero-typing"
          src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=22&duration=3000&pause=1000&color=00D8FF&center=true&vCenter=true&width=700&lines=🔥+Transforming+Infrastructure+Dreams+into+Reality;⚡+Building+Bulletproof+CI%2FCD+Pipelines;☁️+Architecting+Scalable+Cloud+Solutions;🛡️+Security-First+DevOps+Practices;🎯+Zero-Downtime+Deployment+Expert"
          alt="Typing introduction"
        />

        <img
          class="hero-gif"
          src="https://user-images.githubusercontent.com/74038190/213910845-af37a709-8995-40d6-be59-724526e3c3d7.gif"
          alt="DevOps animation"
        />
      </div>
    </section>

    <!-- ABOUT -->
    <section>
      <div class="section-subtitle">ABOUT</div>
      <div class="section-title">🌟 About Me</div>

      <div class="about">
        <div class="about-text">
          <p>
            I'm <strong>MD Waseem</strong>, a <strong>Senior DevOps &amp; Cloud Engineer</strong> based in
            <strong>Hyderabad, India</strong>, with <strong>5+ years</strong> of hands-on experience designing
            and operating scalable, resilient cloud-native platforms.
          </p>
          <p>
            I specialize in <strong>production-grade Kubernetes environments</strong>, <strong>battle-tested
            CI/CD pipelines</strong>, and <strong>observability-driven infrastructure</strong> that lets
            engineering teams ship fast without sacrificing stability or security.
          </p>
          <p>
            My focus is on <strong>automation, reliability, cost optimization, and security-first design</strong>.
            I enjoy taking messy legacy deployments and turning them into clean, repeatable, and fully automated
            systems that don’t wake you up at 3 AM.
          </p>
          <p>
            When I'm not optimising pipelines or clouds, I'm usually experimenting with new DevOps patterns,
            refining IaC modules, or sharpening monitoring strategies to squeeze more signal out of noisy systems.
          </p>
        </div>

        <div class="about-gif">
          <img
            src="https://user-images.githubusercontent.com/74038190/229223263-cf2e4b07-2615-4f87-9c38-e37600f8381a.gif"
            alt="Coding animation"
          />
        </div>
      </div>
    </section>

    <!-- MISSION -->
    <section>
      <div class="section-subtitle">MINDSET</div>
      <div class="section-title">🎯 Mission &amp; Philosophy</div>

      <div class="mission-card">
<pre><code>const myMission = {
  identity: "DevOps engineer obsessed with reliability &amp; automation",
  passion: "Turning chaos into orchestrated harmony",
  focus: ["Automation", "Scalability", "Security", "Observability"],
  achievements: [
    "Deployment time: hours ➜ minutes",
    "100+ microservices orchestrated in production",
    "40% infrastructure cost optimization",
    "60% MTTR reduction with proactive monitoring"
  ],
  belief: "If it's not automated, it's technical debt",
  motto: "Automate Everything. Monitor Everything. Secure Everything."
};</code></pre>
      </div>
    </section>

    <!-- TECH STACK -->
    <section>
      <div class="section-subtitle">STACK</div>
      <div class="section-title">🛠 Tech Stack – Full Arsenal</div>

      <div class="tech-section">
        <p class="muted">
          Tools I regularly use to architect, automate and operate production systems:
          AWS · Terraform · Jenkins · ArgoCD · Docker · Kubernetes · Ansible · Linux · Git · GitHub · Jira ·
          Bash · Python · Prometheus · Grafana · SonarQube · Nexus · Maven · NGINX · Cloudflare and more.
        </p>

        <div class="tech-marquee-wrapper">
          <div class="tech-marquee-track">
            <img
              src="https://skillicons.dev/icons?i=aws,terraform,jenkins,argo,kubernetes,docker,ansible,linux,git,github,jira,python,bash,prometheus,grafana,sonarqube,nexus,maven,nginx,cloudflare"
              alt="Tech icons strip"
            />
            <!-- duplicate for seamless loop -->
            <img
              src="https://skillicons.dev/icons?i=aws,terraform,jenkins,argo,kubernetes,docker,ansible,linux,git,github,jira,python,bash,prometheus,grafana,sonarqube,nexus,maven,nginx,cloudflare"
              alt="Tech icons strip duplicate"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- HIGHLIGHTS -->
    <section>
      <div class="section-subtitle">HIGHLIGHTS</div>
      <div class="section-title">🏆 What I’ve Delivered</div>

      <div class="highlights-grid">
        <div class="card">
          <h3>🚀 CI/CD Engineering</h3>
          <div class="metric">95%+ deployment success rate</div>
          <ul>
            <li>Designed multi-stage CI/CD pipelines using Jenkins &amp; GitOps workflows.</li>
            <li>Integrated automated testing, security scanning and quality gates.</li>
            <li>Rollback-ready deployments with minimal human intervention.</li>
          </ul>
        </div>

        <div class="card">
          <h3>☁️ Cloud Infrastructure</h3>
          <div class="metric">40% infrastructure cost optimization</div>
          <ul>
            <li>Built highly available cloud architectures with autoscaling &amp; load balancing.</li>
            <li>Used Infrastructure as Code to deliver consistent environments.</li>
            <li>Implemented strong IAM, network segmentation and guardrails.</li>
          </ul>
        </div>

        <div class="card">
          <h3>🐳 Kubernetes Orchestration</h3>
          <div class="metric">100+ microservices in production</div>
          <ul>
            <li>Managed production-grade Kubernetes clusters with Helm &amp; Ingress.</li>
            <li>Implemented blue-green &amp; canary deployments for zero downtime.</li>
            <li>Optimised resource utilisation with HPA and right-sized workloads.</li>
          </ul>
        </div>

        <div class="card">
          <h3>📊 Observability &amp; Reliability</h3>
          <div class="metric">60% MTTR reduction</div>
          <ul>
            <li>Built complete monitoring stacks with Prometheus, Grafana &amp; CloudWatch.</li>
            <li>Created actionable alerts instead of noisy dashboards.</li>
            <li>Used tracing &amp; metrics to find bottlenecks before users feel them.</li>
          </ul>
        </div>

        <div class="card">
          <h3>⚙️ Automation &amp; Scripting</h3>
          <div class="metric">80% manual ops eliminated</div>
          <ul>
            <li>Automated provisioning &amp; configuration with Ansible &amp; IaC.</li>
            <li>Wrote reusable Bash/Python tooling for repetitive workflows.</li>
            <li>Reduced human error and improved deployment consistency.</li>
          </ul>
        </div>

        <div class="card">
          <h3>🔐 Security &amp; Compliance</h3>
          <div class="metric">Security-first DevOps mindset</div>
          <ul>
            <li>Shift-left security with SAST/DAST integrated into pipelines.</li>
            <li>Secure secret management and policy-driven access control.</li>
            <li>Regular hardening, patching and audit-friendly configurations.</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- CORE COMPETENCIES -->
    <section>
      <div class="section-subtitle">SKILLS</div>
      <div class="section-title">💼 Core Competencies</div>

      <div class="table-like">
        <div class="table-col">
          <h4>DevOps Practices</h4>
          <ul>
            <li>CI/CD pipeline design</li>
            <li>GitOps workflows</li>
            <li>Release &amp; environment management</li>
            <li>Blue-green &amp; canary deployments</li>
          </ul>
        </div>
        <div class="table-col">
          <h4>Cloud &amp; Infrastructure</h4>
          <ul>
            <li>AWS architecture &amp; networking</li>
            <li>High availability &amp; DR strategies</li>
            <li>Cost optimization &amp; FinOps thinking</li>
          </ul>
        </div>
        <div class="table-col">
          <h4>IaC &amp; Automation</h4>
          <ul>
            <li>Terraform modules &amp; patterns</li>
            <li>Ansible configuration management</li>
            <li>Bash/Python automation tooling</li>
          </ul>
        </div>
        <div class="table-col">
          <h4>Observability &amp; Security</h4>
          <ul>
            <li>Prometheus, Grafana, CloudWatch</li>
            <li>Alert design &amp; MTTR reduction</li>
            <li>SAST/DAST integration &amp; hardening</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- GITHUB STATS -->
    <section class="stats center">
      <div class="section-subtitle">GITHUB</div>
      <div class="section-title">📊 GitHub Analytics</div>
      <br />
      <img
        src="https://github-readme-stats.vercel.app/api?username=MD-Waseem&show_icons=true&theme=radical"
        alt="GitHub stats"
        height="160"
      />
      <img
        src="https://github-readme-streak-stats.herokuapp.com/?user=MD-Waseem&theme=radical"
        alt="GitHub streak"
        height="160"
      />
    </section>

    <!-- SNAKE -->
    <section class="snake center">
      <div class="section-subtitle">CONTRIBUTIONS</div>
      <div class="section-title">🐍 Contribution Snake</div>
      <p class="muted" style="margin-bottom:8px;">
        Because even my commits like to travel in formation.
      </p>
      <img
        src="https://raw.githubusercontent.com/MD-Waseem/MD-Waseem/output/github-contribution-grid-snake.svg"
        alt="GitHub contribution snake"
      />
    </section>

    <!-- PHILOSOPHY & CONTACT -->
    <section>
      <div class="section-subtitle">PHILOSOPHY</div>
      <div class="section-title">💬 How I Think About DevOps</div>
      <blockquote>
        “In DevOps, we don't just build systems — we build the confidence that lets teams
        ship without fear.”
      </blockquote>

      <p class="muted" style="margin-top:10px;">
        Automate the repetitive. Monitor the critical. Secure everything. Optimize continuously.
        That’s the operating system I bring to every team and platform I work with.
      </p>

      <hr />

      <div class="section-subtitle">CONTACT</div>
      <div class="section-title">🤝 Let’s Connect &amp; Collaborate</div>
      <p class="muted">
        Open to discussions around DevOps transformations, cloud architecture, reliability
        engineering and mentorship.
      </p>

      <div class="contact-buttons">
        <a
          class="btn-pill"
          href="https://www.linkedin.com/in/md-waseem-0b432238b/"
          target="_blank"
          rel="noreferrer"
        >
          <span class="icon">💼</span>
          <span>Connect on LinkedIn</span>
        </a>
        <a class="btn-pill" href="mailto:mdwaseem.cloudops@gmail.com">
          <span class="icon">📧</span>
          <span>Email Me</span>
        </a>
        <a
          class="btn-pill"
          href="https://github.com/MD-Waseem"
          target="_blank"
          rel="noreferrer"
        >
          <span class="icon">🐙</span>
          <span>View My GitHub</span>
        </a>
      </div>
    </section>
  </main>
</body>
</html>
