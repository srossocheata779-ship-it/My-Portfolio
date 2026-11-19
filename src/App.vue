<script setup lang="ts">
import { ref } from 'vue'

const menuOpen = ref(false)

const navigation = [
  { name: 'About', id: 'about' },
  { name: 'Skills', id: 'skills' },
  { name: 'Projects', id: 'projects' },
  { name: 'Cyber Lab', id: 'cyber-lab' },
  { name: 'Learning', id: 'learning' },
  { name: 'Contact', id: 'contact' },
]

const skills = [
  { category: 'Programming', items: ['C++', 'Python', 'JavaScript', 'TypeScript'] },
  { category: 'Frontend', items: ['HTML5', 'CSS3'] },
  { category: 'Frameworks', items: ['Vue 3', 'Next.js', 'Tailwind CSS'] },
  { category: 'Backend', items: ['Node.js', 'Python Flask', 'Prisma', 'REST APIs'] },
  { category: 'Database', items: ['MariaDB', 'MySQL'] },
  { category: 'Cybersecurity', items: ['Security Auditing', 'Kali Linux', 'Penetration Testing', 'Vulnerability Assessment', 'Network Security'] },
  { category: 'Linux', items: ['Kali Linux', 'Linux CLI', 'File & Directory Management', 'Linux Networking'] },
  { category: 'Networking', items: ['TCP/IP', 'Subnetting', 'Cisco Packet Tracer'] },
]

const projects = [
  { number: '01', icon: 'fa-shield', title: 'CyberShield Security Awareness', category: 'CYBERSECURITY', description: 'A practical security awareness project covering phishing recognition, website security awareness, and password strength.', technologies: ['Kali Linux', 'Web Security', 'Security Awareness'], status: 'Final Project' },
  { number: '02', icon: 'fa-users', title: 'Staff Management System', category: 'WEB SECURITY TESTING', description: 'Conducting security assessments on an existing staff management web application to explore potential vulnerabilities, evaluate authentication mechanisms, and understand web application security risks in an authorized testing environment.', technologies: ['Vue 3', 'TypeScript', 'Next.js', 'Prisma', 'MariaDB', 'Kali Linux'], status: 'Security Testing', credit: 'Original developer: Sek Thorn' },
  { number: '03', icon: 'fa-sitemap', title: 'Linux & Networking Lab', category: 'SYSTEMS & NETWORKING', description: 'Hands-on practice with Linux administration, network configuration, IP addressing, and troubleshooting.', technologies: ['Kali Linux', 'Linux', 'TCP/IP'], status: 'Learning' },
  { number: '04', icon: 'fa-code', title: 'Student Management System', category: 'SOFTWARE DEVELOPMENT', description: 'A C++ console-based Student Management System featuring user authentication, CRUD operations, student search, sorting, pagination, statistical summaries, and CSV file handling.', technologies: ['C++', 'OOP', 'Vector', 'File Handling', 'CSV'], status: 'Completed' },
]

const labTopics = [
  { icon: 'fa-terminal', title: 'Linux Administration', description: 'Terminal commands, permissions, processes, and Bash scripting.' },
  { icon: 'fa-exchange', title: 'CCNA (200-3001)', description: 'Learning networking fundamentals, IP addressing, and routing protocols.' },
  { icon: 'fa-shield', title: 'Network Security', description: 'Understanding network protocols, firewalls, and intrusion detection systems.' },
  { icon: 'fa-search', title: 'Security Assessment', description: 'Learning vulnerability assessment and safe security testing methods.' },
  { icon: 'fa-lock', title: 'Security Awareness', description: 'Understanding phishing, passwords, and human-centered security.' },
]

const learningPath = [
  'Computer Fundamentals & Operating Systems',
  'Linux & Networking',
  'Programming & Software Engineering',
  'Cybersecurity Fundamentals',
  'Ethical Hacking & Defensive Security',
  'Cloud Security & Specialization',
]
</script>

<template>
  <div class="site-wrapper">
    <header class="navbar">
      <a href="#home" class="logo" aria-label="Sros Socheata, home">
        <span class="logo-mark">S<span>.</span></span>
        <span class="brand-name">SROS SOCHEATA</span>
      </a>

      <button class="menu-toggle" @click="menuOpen = !menuOpen" :aria-expanded="menuOpen" aria-controls="primary-navigation" :aria-label="menuOpen ? 'Close navigation' : 'Open navigation'">
        <i :class="['fa', menuOpen ? 'fa-times' : 'fa-bars']" aria-hidden="true"></i>
      </button>

      <nav id="primary-navigation" :class="{ 'nav-open': menuOpen }" aria-label="Main navigation">
        <a v-for="item in navigation" :key="item.id" :href="`#${item.id}`" @click="menuOpen = false">{{ item.name }}</a>
      </nav>
    </header>

    <main>
      <section id="home" class="hero section-container">
        <div class="hero-copy">
          <div class="availability"><span class="status-dot"></span> OPEN TO LEARNING OPPORTUNITIES</div>
          <p class="eyebrow">CYBERSECURITY · SOFTWARE · NETWORKS</p>
          <h1>Curious by nature.<br /><em>Building with purpose.</em></h1>
          <p class="hero-description">I’m Sros Socheata, an aspiring cybersecurity specialist with an interest in network engineering. I build applications, explore Linux, and learn how to make technology more secure.</p>
          <div class="hero-actions">
            <a href="#projects" class="button-primary">Explore my work <i class="fa fa-arrow-right" aria-hidden="true"></i></a>
            <a href="#about" class="text-link">A little about me <i class="fa fa-arrow-down" aria-hidden="true"></i></a>
          </div>
          <div class="hero-meta"><span>BASED IN PHNOM PENH, CAMBODIA</span><span><i class="fa fa-asterisk" aria-hidden="true"></i> ALWAYS LEARNING &amp; BUILDING</span></div>
        </div>

        <div class="hero-visual" aria-label="Portrait of Sros Socheata">
          <div class="portrait-frame"><img src="/image/Blue-Lit Professional Portrait.png" alt="Portrait of Sros Socheata" class="hero-portrait" /></div>
          <div class="portrait-caption"><span>THE PERSON BEHIND THE KEYBOARD</span><span class="caption-rule"></span><span>01 — 06</span></div>
          <div class="hero-stamp" aria-hidden="true"><span>LEARN</span><i class="fa fa-asterisk stamp-star"></i><span>BUILD</span><span>SECURE</span></div>
          <span class="hero-index" aria-hidden="true">SC—26</span>
        </div>
        <a href="#about" class="scroll-cue"><span></span> SCROLL TO EXPLORE</a>
      </section>

      <section id="about" class="section-container section-block about-section">
        <div class="section-heading"><p class="eyebrow"><span>01</span> / ABOUT ME</p><span class="heading-note">A PRACTICE OF CURIOSITY</span></div>
        <div class="about-grid">
          <h2>Curiosity is where<br />the work <em>begins.</em></h2>
          <div class="about-copy">
            <p>I'm passionate about software development and cybersecurity. I enjoy understanding how applications work, how systems communicate, and how security weaknesses can be prevented.</p>
            <p>My learning journey combines programming, Linux systems, networking, and practical cybersecurity skills. I believe the best way to learn technology is to build, experiment, and solve real problems.</p>
            <a href="#skills" class="inline-link">Explore my toolkit <i class="fa fa-arrow-right" aria-hidden="true"></i></a>
          </div>
        </div>
        <div class="about-strip"><span>MY APPROACH</span><p>Learn with intention. Build with care. Keep asking better questions.</p><i class="fa fa-asterisk strip-symbol" aria-hidden="true"></i></div>
      </section>

      <section id="skills" class="section-container section-block">
        <div class="section-heading"><p class="eyebrow"><span>02</span> / TECHNICAL SKILLS</p><span class="heading-note">A TOOLKIT IN PROGRESS</span></div>
        <div class="section-intro"><h2>Tools for the<br /><em>curious mind.</em></h2><p class="section-description">Technologies and concepts I have studied or practiced. Skill levels will be updated as I gain experience.</p></div>
        <div class="skills-grid">
          <article v-for="(skill, index) in skills" :key="skill.category" class="skill-card">
            <div class="skill-card-top"><span>0{{ index + 1 }}</span><i class="fa fa-arrow-right skill-mark" aria-hidden="true"></i></div>
            <h3>{{ skill.category }}</h3>
            <div class="skill-tags"><span v-for="item in skill.items" :key="item">{{ item }}</span></div>
          </article>
        </div>
      </section>

      <section id="projects" class="section-container section-block projects-section">
        <div class="section-heading"><p class="eyebrow"><span>03</span> / SELECTED WORK</p><span class="heading-note">BUILT, TESTED, LEARNED</span></div>
        <div class="section-intro"><h2>Work in<br /><em>progress.</em></h2><p class="section-description">Practical projects that demonstrate my development and cybersecurity learning journey.</p></div>
        <div class="projects-grid">
          <article v-for="project in projects" :key="project.number" class="project-card">
            <div class="project-top"><span class="project-number">{{ project.number }}</span><span class="project-category">{{ project.category }}</span></div>
            <div class="project-art" :class="`project-art-${project.number}`" aria-hidden="true"><span class="art-orbit"></span><i :class="['fa', project.icon, 'art-glyph']"></i><span class="art-caption">SROS SOCHEATA · {{ project.number }}</span></div>
            <div class="project-content"><h3>{{ project.title }}</h3><p class="project-description">{{ project.description }}</p>
              <div class="skill-tags"><span v-for="tech in project.technologies" :key="tech">{{ tech }}</span></div>
              <div class="project-bottom"><span class="project-status">{{ project.status }}</span><i class="fa fa-arrow-right project-arrow" aria-hidden="true"></i></div>
              <p v-if="project.credit" class="project-credit">{{ project.credit }}</p>
            </div>
          </article>
        </div>
      </section>

      <section id="cyber-lab" class="section-container section-block">
        <div class="section-heading"><p class="eyebrow"><span>04</span> / CYBER LAB</p><span class="heading-note">PRACTICE WITH PURPOSE</span></div>
        <div class="lab-panel">
          <div class="lab-lead"><p class="eyebrow">PERSONAL LEARNING ENVIRONMENT</p><h2>Learning by<br /><em>doing the work.</em></h2><p>Exploring systems, networks, and security through hands-on practice.</p><i class="fa fa-shield lab-seal" aria-hidden="true"></i></div>
          <div class="lab-topics"><article v-for="(topic, index) in labTopics" :key="topic.title"><i :class="['fa', topic.icon, 'lab-icon']" aria-hidden="true"></i><span class="lab-topic-number">0{{ index + 1 }}</span><div><h3>{{ topic.title }}</h3><p>{{ topic.description }}</p></div></article></div>
          <p class="lab-note">All security testing is performed in authorized learning environments and systems.</p>
        </div>
      </section>

      <section id="learning" class="section-container section-block">
        <div class="section-heading"><p class="eyebrow"><span>05</span> / LEARNING JOURNEY</p><span class="heading-note">FOUNDATIONS TO SPECIALIZATION</span></div>
        <div class="section-intro"><h2>One step<br />at a <em>time.</em></h2><p class="section-description learning-intro">Topics I am working through as I build my foundations. Certifications will be listed here as I earn them.</p></div>
        <ol class="learning-list"><li v-for="(item, index) in learningPath" :key="item"><span class="learning-number">0{{ index + 1 }}</span><p>{{ item }}</p><i class="fa fa-arrow-right learning-arrow" aria-hidden="true"></i></li></ol>
      </section>

      <section id="contact" class="section-container section-block contact-section">
        <p class="eyebrow"><span>06</span> / CONTACT</p>
        <p class="contact-kicker">HAVE A GOOD QUESTION?</p>
        <h2>Let’s make<br /><em>something matter.</em></h2>
        <p class="section-description">I'm interested in connecting with developers, cybersecurity professionals, and people who love technology.</p>
        <div class="contact-actions"><a href="mailto:srossocheata779@gmail.com" class="button-primary">Send me an email <i class="fa fa-arrow-right" aria-hidden="true"></i></a><a href="https://github.com/srossocheata779-ship-it" target="_blank" rel="noopener noreferrer" class="contact-link">GitHub <i class="fa fa-external-link" aria-hidden="true"></i></a><a href="https://www.linkedin.com/in/sros-socheata-8183403b0" target="_blank" rel="noopener noreferrer" class="contact-link">LinkedIn <i class="fa fa-external-link" aria-hidden="true"></i></a></div>
        <p class="contact-note">Open to learning opportunities, collaboration, and professional connections.</p>
      </section>
    </main>

    <footer class="footer"><a href="#home" class="logo" aria-label="Sros Socheata, home"><span class="logo-mark">S<span>.</span></span><span class="brand-name">SROS SOCHEATA</span></a><p>Designed &amp; built by Sros Socheata</p><p>© 2026 · Phnom Penh, Cambodia</p></footer>
  </div>
</template>
