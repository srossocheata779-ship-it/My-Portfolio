<script setup lang="ts">
import { ref } from 'vue';

const menuOpen = ref(false);

const navigation = [
  { name: 'Home', id: 'home' },
  { name: 'About', id: 'about' },
  { name: 'Skills', id: 'skills' },
  { name: 'Projects', id: 'projects' },
  { name: 'Cyber Lab', id: 'cyber-lab' },
  { name: 'Contact', id: 'contact' },
]

const skills = [
  { category: 'Programming', items: ['C++', 'Python', 'JavaScript', 'TypeScript']},
  { category: 'Frontend', items: ['HTML5', 'CSS3', 'Vue 3', 'Tailwind CSS']},
  { category: 'Backend', items: ['Next.js', 'Node.js', 'Python Flask', 'Prisma', 'REST APTs']},
  { category: 'Database', items: ['MariaDB', 'MySQL']},
  { category: 'Cybersecurity', items: ['Security Auditing', 'Kali Linux', 'Penetration Testing', 'Vulnerability Assessment', 'Network Security']},
  { category: 'Linux', items: ['Kali Linux', 'Linux CLI', 'File & Directory Management', 'Linux Networking']},
  { category: 'Networking', items: ['TCP/IP', 'Subnetting', 'Cisco Packet Tracer']}
]

const projects = [
  { number: '01',
    title: 'CyberShield Security Awareness',
    category: 'CYBERSECURITY',
    description: 'A Practical security awareness project covering phashing recognition, website security awareness, and password strength.',
    technologies: ['Kali Linux', 'Web Security', 'Security Awareness'],
    status: 'In Progress', },

  { number:'02',
    title: 'Staff Management System',
    category: 'WEB SECURITY TESTING',
    description: 'Conducting security assessments on an existing staff management web application to explore potential vulnerabilities, evaluate authentication mechanisms, and understand web application security risks in an authorized testing environment.',
    technologies: ['Vue 3', 'TypeScript', 'Next.js', 'Prisma', 'MariaDB', 'Kali Linux'],
    status: 'Security Testing',
    credit: 'Original Developer: [Sek Thorn]'
  },

  { number:'03',
    title: 'Linux & Networking Lab',
    category: 'SYSTEMS & NETWORKING',
    description: 'Hands-on practice with Linux administration, network configuration, IP addressing, and troubleshooting.',
    technologies: ['Kali Linux', 'Linux', 'TCP/IP'],
    status: 'Learning', },

  { number:'04',
    title: 'Student Management System',
    category: 'SOFTWARE DEVELOPMENT',
    description: 'A C++ console-based Student Management System featuring user authentication, CRUD operattions, student search, sorting, pagination, statistical summaries, and CSV file handling.',
    technologies: ['C++', 'OOP', 'Vector', 'File Handling', 'CSV'],
    status: 'Completed', },
]
</script>

<template>
  <div class="site-wrapper">
    <!--navigation-->
    <header class="navbar">
      <a href="#home" class="logo">
        <span class="logo-bracket">&gt;</span>SROS<span class="accent">SOCHEATA</span><span class="logo-bracket">&gt;</span>
      </a>

      <button 
        class="menu-toggle"
        @click="menuOpen = !menuOpen"
        aria-label="Toggle navigation">
        &#9776;
      </button>

      <nav :class="{ 'nav-open' : menuOpen }">
        <a
          v-for="item in navigation"
          :key="item.id"
          :href="`#${item.id}`"
          @click="menuOpen = false">
        {{ item.name }}
        </a>
        <a href="#contact" class="nav-contact" @click="menuOpen = false">
          Let's Talk
        </a>
      </nav>
    </header>

    <main>
      <!--hero section-->
      <section id="home" class="hero section-container">
        <div class="hero-content">
          <div class="availability">
            <span class="status-dot"></span>
            OPEN TO LEARNING & OPPORTUNITIES
          </div>

          <p class="eyebrow">HELLO, WORLD! I'M A TECHNOLOGY ENTHUSIAST</p>

          <h1>
            Building the future.<br />
            <span class="gradient-text">Securing the digital world.</span>
          </h1>

          <p class="hero-description">
            Aspiring Cybersecurity Specialist & Software Developer.
            Passionate about building applications, exploring Linux, understanding networking, and learning how to secure technology.
          </p>

          <div class="hero-tech">
            <span>FOCUS AREA</span>
            <span>Cybersecurity</span>
            <span>Software Development</span>
            <span>Full-Stack Development</span>
            <span>Lunix</span>
            <span>Networking</span>
          </div>
        </div>

        <div class="terminal">
          <div class="terminal-header">
            <div class="terminal-dots">
              <i></i><i></i><i></i>
            </div>
            <span>developer@cyberjourney:~$</span>
          </div>

          <div class="terminal-body">
            <p><span class="terminal-green">#</span>whoami</p>
            <h3>Technology Enthusiast</h3>

            <p><span class="terminal-green">#</span>cat interests.txt</p>
            <p class="terminal-output">
              Cybersecurity<br />
              Software Development<br />
              Linux & Networking<br />
              Continuous Learning
            </p>

            <p><span class="terminal-green">#</span>cat mission.txt</p>
            <p class="terminal-blue">
              Learn. Build. Test. Secure.
            </p>

            <p><span class="terminal-green">#</span> <span class="cursor">_</span></p>
          </div>
        </div>
      </section>

      <!--about section-->
      <section id="about" class="section-container section-block">
        <p class="eyebrow">// 01. ABOUT ME</p>
        <h2>Curiosity drives <span class="gradient-text">my journey.</span></h2>

        <div class="about-grid">
          <div>
            <p class="section-description">
              I'm passionate about software devolopment and cybersecurity.
              I enjoy understanding how applications work, how ssystems communicate, and how security weaknesses can be prevented.
            </p>
            <p class="section-description">
              My learning journey combines programming, Linux systems, networking, and practical cybersecurity skills.
              i believe that the best way to learn technology is to buld, experiment, and solve real problems. 
            </p>
          </div>

          <div class="profile-card">
            <div class="profile-image-wrapper">
              <img src="../public/image/Blue-Lit Professional Portrait.png" alt="My professional profile photo" class="profile-image"/>
            </div>
            <h3>SROS SOCHEATA</h3>
            <p>Aspiring Cybersecurity Specialist & Developer</p>

            <span class="profile-status">
              <span class="status-dot"></span>
              Always Learning & Building
            </span>
          </div>

        </div>
      </section>

      <!--skills section-->
      <section id="skills" class="section-container section-block">
        <p class="eyebrow">// 02. TECHNICAL SKILLS</p>
        <h2>My technical <span class="gradient-text">toolkit.</span></h2>
        <p class="section-description">
          Technologies and concepts I have studied or practiced.
          Skill levels will be updated as I gain experience.
        </p>

        <div class="skills-grid">
          <article v-for="skill in skills" :key="skill.category" class="skill-card">
            <h3>{{ skill.category }}</h3>
            <div class="skill-tags">
              <span v-for="item in skill.items" :key="item">{{ item }}</span>
            </div>
          </article>
        </div>
      </section>

      <!--projects section-->
      <section id="projects" class="section-container section-block">
        <p class="eyebrow">// 03. FEATURED PROJECTS</p>
        <h2>Thing I have <span class="gradient-text">worked on.</span></h2>
        <p class="section-description">
          Practical projects that demostrate my development and cybersecurity learning journey.
        </p>

        <div class="projects-grid">
          <article v-for="project in projects" :key="project.number" class="project-card">
            <div class="project-top">
              <span class="project-number">0{{ project.number }}</span>
              <span class="project-category">{{ project.category }}</span>
            </div>

            <h3>{{ project.title }}</h3>
            <p class="project-description">{{ project.description }}</p>

            <div class="skill-tags">
              <span v-for="tech in project.technologies" :key="tech">{{ tech }}</span>
            </div>

            <div class="project-bottom">
              <span class="project-status">{{ project.status }}</span>
              <span class="project-arrow">↗</span>
            </div>

            <p v-if="project.credit" class="project-credit">
              {{ project.credit }}
            </p>
          </article>
        </div>
      </section>

      <!--Cyber lab-->
      <section id="cyber-lab" class="section-container section-block">
        <p class="eyebrow">// 04. CYBER LAB</p>
        <h2>learning through <span class="gradient-text">practice.</span></h2>

        <div class="lab-panel">
          <div class="lab-header">
            <span class="status-dot"></span>
            PERSONAL LEARNING ENVIRONMENT
          </div>

          <div class="lab-grid">
            <div>
              <span class="lab-icon">&ldquo;</span>
              <h3>Linux Administration</h3>
              <p>Terminal commands, permissions, processes, and Bash scripting.</p>
            </div>
            <div>
              <span class="lab-icon">&#127760;</span>
              <h3>CCNA (200-3001)</h3>
              <p>Learning networking fundamentals, IP addressing, and routing protocols.</p>
            </div>
            <div>
              <span class="lab-icon">&#8961;</span>
              <h3>Network Security</h3>
              <p>Understanding network protocols, firewalls, and intrusion detection systems.</p>
            </div>
            <div>
              <span class="lab-icon">&#8982;</span>
              <h3>Security Assessment</h3>
              <p>Learning vulnerability assessment and safe security testing methods.</p>
            </div>
            <div>
              <span class="lab-icon">&#9672;</span>
              <h3>Security Awareness</h3>
              <p>Understanding phishing, passwords, and human-centered security.</p>
            </div>
          </div>

          <p class="lab-note">
            All security testing is performed in authorized learning environment and systems.
          </p>
        </div>
      </section>

      <!--Learning-->
      <section id="learning" class="section-container section-block">
        <p class="eyebrow">// 05. LEARNING JOURNEY</p>
        <h2>Always <span class="gradient-text">learning.</span></h2>

        <div class="learning-list">
          <div><span>01</span><p>Computer Fundamentals & Operating Systems</p></div>
          <div><span>02</span><p>Linux & Networking</p></div>
          <div><span>03</span><p>Programming & Software Development</p></div>
          <div><span>04</span><p>Cybersecurity Fundamentals</p></div>
          <div><span>05</span><p>Ethical Hacking & Defensive Securirty</p></div>
          <div><span>06</span><p>Cloud Security & Specialization</p></div>
        </div>
      </section>

      <!--Contact-->
      <section id="contact" class="section-container section-block contact-section">
        <p class="eyebrow">// 06. CONTACT</p>
        <h2>Let's build something <span class="gradient-text">meaningful.</span></h2>
        <p class="section-description">
          I'm interested in connecting with developers, cybersecurity professionals, and  people who love technology.
        </p>

        <div class="contact-actions">
          <a href="mailto:srossocheata779@gmail.com" class="button-primary">Send Me an Email</a>
          <a 
            href="https://github.com/srossocheata779-ship-it" 
            target="_blank" rel="noopener noreferrer" 
            class="contact-link">GitHub</a>
          <a 
            href="https://www.linkedin.com/in/sros-socheata-8183403b0" 
            target="_blank" rel="noopener noreferrer" 
            class="contact-link">LinkedIn</a>
        </div>

        <p class="contact-noted">
          Open to learning opportunities, collaboration, and professional connections.
        </p>
      </section>

    </main>

    <!--footer-->
    <footer class="footer">
      <a href="#home" class="logo">&lt;SROS<span class="accent">SOCHEATA</span>/&gt;</a>
      <p>Designed & build BY Sros Socheata</p>
      <p>&copy; 2026 &middot; Learing, building, and securing.</p>
    </footer>

  </div>
</template>