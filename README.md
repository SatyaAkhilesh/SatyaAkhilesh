<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Satya P – Senior Cloud & AI Engineer</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Segoe UI', system-ui, sans-serif;
      background: linear-gradient(135deg, #0f0f1a 0%, #1a1a2e 50%, #16213e 100%);
      min-height: 100vh;
      color: #e0e0e0;
      overflow-x: hidden;
    }
    
    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 40px 20px;
      position: relative;
      overflow: hidden;
    }
    
    .hero::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle at 30% 40%, rgba(99, 102, 241, 0.15) 0%, transparent 50%),
                  radial-gradient(circle at 70% 60%, rgba(139, 92, 246, 0.1) 0%, transparent 50%);
      animation: pulse 8s ease-in-out infinite;
    }
    
    @keyframes pulse {
      0%, 100% { transform: scale(1) rotate(0deg); }
      50% { transform: scale(1.1) rotate(5deg); }
    }
    
    .hero-content {
      position: relative;
      z-index: 1;
    }
    
    .avatar {
      width: 140px;
      height: 140px;
      background: linear-gradient(135deg, #6366f1, #8b5cf6, #a855f7);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 48px;
      font-weight: 700;
      color: white;
      margin: 0 auto 30px;
      box-shadow: 0 0 60px rgba(139, 92, 246, 0.4);
      animation: float 6s ease-in-out infinite;
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    
    h1 {
      font-size: 3.5rem;
      font-weight: 800;
      background: linear-gradient(135deg, #fff 0%, #c7d2fe 50%, #a5b4fc 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 15px;
      letter-spacing: -1px;
    }
    
    .tagline {
      font-size: 1.3rem;
      color: #a5b4fc;
      margin-bottom: 25px;
      font-weight: 500;
    }
    
    .badges {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      justify-content: center;
      margin-bottom: 40px;
    }
    
    .badge {
      background: rgba(99, 102, 241, 0.2);
      border: 1px solid rgba(99, 102, 241, 0.4);
      padding: 8px 18px;
      border-radius: 50px;
      font-size: 0.85rem;
      color: #c7d2fe;
      backdrop-filter: blur(10px);
      transition: all 0.3s ease;
    }
    
    .badge:hover {
      background: rgba(99, 102, 241, 0.4);
      transform: translateY(-2px);
    }
    
    .stats-row {
      display: flex;
      gap: 40px;
      justify-content: center;
      flex-wrap: wrap;
    }
    
    .stat {
      text-align: center;
    }
    
    .stat-value {
      font-size: 2.5rem;
      font-weight: 800;
      background: linear-gradient(135deg, #22d3ee, #6366f1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    
    .stat-label {
      font-size: 0.85rem;
      color: #94a3b8;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .section {
      max-width: 1000px;
      margin: 0 auto;
      padding: 80px 20px;
    }
    
    h2 {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 50px;
      color: #fff;
      position: relative;
    }
    
    h2::after {
      content: '';
      display: block;
      width: 60px;
      height: 4px;
      background: linear-gradient(90deg, #6366f1, #a855f7);
      margin: 15px auto 0;
      border-radius: 2px;
    }
    
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }
    
    .skill-card {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 16px;
      padding: 25px;
      backdrop-filter: blur(10px);
      transition: all 0.4s ease;
    }
    
    .skill-card:hover {
      transform: translateY(-5px);
      border-color: rgba(99, 102, 241, 0.5);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    }
    
    .skill-icon {
      font-size: 2rem;
      margin-bottom: 15px;
    }
    
    .skill-card h3 {
      color: #fff;
      margin-bottom: 12px;
      font-size: 1.1rem;
    }
    
    .skill-card p {
      color: #94a3b8;
      font-size: 0.9rem;
      line-height: 1.6;
    }
    
    .timeline {
      position: relative;
      padding-left: 30px;
    }
    
    .timeline::before {
      content: '';
      position: absolute;
      left: 0;
      top: 0;
      bottom: 0;
      width: 2px;
      background: linear-gradient(180deg, #6366f1, #a855f7, #6366f1);
    }
    
    .timeline-item {
      position: relative;
      margin-bottom: 40px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 16px;
      padding: 25px;
      transition: all 0.3s ease;
    }
    
    .timeline-item:hover {
      border-color: rgba(99, 102, 241, 0.4);
      transform: translateX(5px);
    }
    
    .timeline-item::before {
      content: '';
      position: absolute;
      left: -34px;
      top: 30px;
      width: 12px;
      height: 12px;
      background: #6366f1;
      border-radius: 50%;
      box-shadow: 0 0 20px rgba(99, 102, 241, 0.6);
    }
    
    .timeline-date {
      color: #a855f7;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 8px;
    }
    
    .timeline-item h3 {
      color: #fff;
      margin-bottom: 5px;
    }
    
    .timeline-company {
      color: #6366f1;
      font-weight: 500;
      margin-bottom: 15px;
    }
    
    .timeline-item ul {
      list-style: none;
    }
    
    .timeline-item li {
      color: #94a3b8;
      padding: 5px 0;
      padding-left: 20px;
      position: relative;
      font-size: 0.95rem;
    }
    
    .timeline-item li::before {
      content: '→';
      position: absolute;
      left: 0;
      color: #6366f1;
    }
    
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 25px;
    }
    
    .project-card {
      background: linear-gradient(135deg, rgba(99, 102, 241, 0.1), rgba(139, 92, 246, 0.05));
      border: 1px solid rgba(99, 102, 241, 0.2);
      border-radius: 20px;
      padding: 30px;
      transition: all 0.4s ease;
      position: relative;
      overflow: hidden;
    }
    
    .project-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, #6366f1, #a855f7);
    }
    
    .project-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 25px 50px rgba(99, 102, 241, 0.2);
    }
    
    .project-card h3 {
      color: #fff;
      margin-bottom: 15px;
      font-size: 1.2rem;
    }
    
    .project-metrics {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 15px;
    }
    
    .metric {
      background: rgba(99, 102, 241, 0.2);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.8rem;
      color: #c7d2fe;
    }
    
    .project-card p {
      color: #94a3b8;
      font-size: 0.9rem;
      line-height: 1.6;
    }
    
    .education-card {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 16px;
      padding: 30px;
      text-align: center;
      max-width: 600px;
      margin: 0 auto;
    }
    
    .edu-item {
      margin-bottom: 20px;
    }
    
    .edu-item:last-child {
      margin-bottom: 0;
    }
    
    .edu-degree {
      color: #fff;
      font-size: 1.1rem;
      font-weight: 600;
    }
    
    .edu-school {
      color: #a855f7;
    }
    
    .footer {
      text-align: center;
      padding: 60px 20px;
      background: rgba(0, 0, 0, 0.3);
    }
    
    .footer h2 {
      margin-bottom: 30px;
    }
    
    .contact-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }
    
    .contact-link {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(99, 102, 241, 0.2);
      border: 1px solid rgba(99, 102, 241, 0.3);
      padding: 12px 24px;
      border-radius: 50px;
      color: #c7d2fe;
      text-decoration: none;
      transition: all 0.3s ease;
    }
    
    .contact-link:hover {
      background: rgba(99, 102, 241, 0.4);
      transform: translateY(-3px);
    }
  </style>
</head>

<body>
  <section class="hero">
    <div class="hero-content">
      <div class="avatar">SP</div>
      <h1>Satya P</h1>
      <p class="tagline">Senior Cloud & AI Engineer</p>
      <div class="badges">
        <span class="badge">☁️ AWS Certified</span>
        <span class="badge">⚡ Serverless</span>
        <span class="badge">🤖 LLM Integration</span>
        <span class="badge">🔧 DevOps</span>
        <span class="badge">🏗️ Microservices</span>
      </div>
      <div class="stats-row">
        <div class="stat">
          <div class="stat-value">99.99%</div>
          <div class="stat-label">Uptime</div>
        </div>
        <div class="stat">
          <div class="stat-value">28%</div>
          <div class="stat-label">Cost Reduction</div>
        </div>
        <div class="stat">
          <div class="stat-value">10K+</div>
          <div class="stat-label">Concurrent Users</div>
        </div>
        <div class="stat">
          <div class="stat-value">40%</div>
          <div class="stat-label">Faster Deploys</div>
        </div>
      </div>
    </div>
  </section>

  <section class="section">
    <h2>Core Expertise</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-icon">☁️</div>
        <h3>Cloud & Serverless</h3>
        <p>AWS Lambda, API Gateway, DynamoDB, CloudFront, S3 – building scalable, cost-effective infrastructure</p>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🤖</div>
        <h3>AI & LLM Integration</h3>
        <p>OpenAI, AWS Bedrock, RAG Pattern – creating intelligent systems that enhance user experiences</p>
      </div>
      <div class="skill-card">
        <div class="skill-icon">⚛️</div>
        <h3>Frontend Development</h3>
        <p>React, Next.js, TypeScript – crafting responsive, performant user interfaces</p>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🔧</div>
        <h3>Backend Systems</h3>
        <p>Node.js, Java, Python, FastAPI – building robust APIs and services</p>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🐳</div>
        <h3>Microservices</h3>
        <p>Kubernetes, Docker, Kafka – orchestrating distributed systems at scale</p>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🚀</div>
        <h3>DevOps & Security</h3>
        <p>CI/CD, Terraform, OAuth2, JWT, RBAC – automating deployments with security-first mindset</p>
      </div>
    </div>
  </section>

  <section class="section">
    <h2>Experience</h2>
    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-date">2025 – Present</div>
        <h3>Full Stack & AI Engineer</h3>
        <div class="timeline-company">MUNDO Prints</div>
        <ul>
          <li>Architected serverless systems delivering 99.99% uptime and 42% revenue growth</li>
          <li>Integrated LLMs using AWS Bedrock & OpenAI, improving response times by 45%</li>
          <li>Led microservices migration reducing infrastructure costs by 28%</li>
          <li>Built automated CI/CD pipelines reducing release time by 40%</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-date">2022 – 2023</div>
        <h3>Cloud Platform Engineer</h3>
        <div class="timeline-company">Nextrics</div>
        <ul>
          <li>Delivered 99.9% availability for enterprise clients</li>
          <li>Built Kubernetes + Kafka pipelines reducing load time by 40%</li>
          <li>Automated DevOps pipelines reducing release cycles by 50%</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-date">2022</div>
        <h3>Developer</h3>
        <div class="timeline-company">High Radius</div>
        <ul>
          <li>Built PCI-DSS compliant platform processing $1M+ monthly transactions</li>
          <li>Enhanced backend performance by 40% for 5,000+ concurrent users</li>
          <li>Developed real-time analytics dashboard boosting adoption by 20%</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="section">
    <h2>Featured Projects</h2>
    <div class="projects-grid">
      <div class="project-card">
        <h3>Serverless E-commerce Platform</h3>
        <div class="project-metrics">
          <span class="metric">10K+ users</span>
          <span class="metric">4× scaling</span>
          <span class="metric">+42% revenue</span>
        </div>
        <p>Built a fully serverless architecture capable of handling massive traffic spikes while maintaining sub-second response times</p>
      </div>
      <div class="project-card">
        <h3>AI Customer Support System</h3>
        <div class="project-metrics">
          <span class="metric">RAG-based</span>
          <span class="metric">45% faster</span>
          <span class="metric">+30% CSAT</span>
        </div>
        <p>Designed an intelligent chatbot using retrieval-augmented generation for context-aware, accurate customer responses</p>
      </div>
      <div class="project-card">
        <h3>Microservices Migration</h3>
        <div class="project-metrics">
          <span class="metric">35% faster</span>
          <span class="metric">-28% costs</span>
          <span class="metric">K8s + Kafka</span>
        </div>
        <p>Led the transformation from monolith to microservices, dramatically improving system resilience and development velocity</p>
      </div>
    </div>
  </section>

  <section class="section">
    <h2>Education</h2>
    <div class="education-card">
      <div class="edu-item">
        <div class="edu-degree">MS, Information Systems</div>
        <div class="edu-school">Northeastern University</div>
      </div>
      <div class="edu-item">
        <div class="edu-degree">BTech, Electronics & Communication</div>
        <div class="edu-school">SRM University</div>
      </div>
    </div>
  </section>

  <footer class="footer">
    <h2>Let's Connect</h2>
    <div class="contact-links">
      <a href="mailto:satyaakhilesh0402@gmail.com" class="contact-link">
        ✉️ satyaakhilesh0402@gmail.com
      </a>
      <a href="https://linkedin.com/in/satya-akhilesh-pulavarthi" class="contact-link" target="_blank">
        💼 LinkedIn
      </a>
    </div>
  </footer>
</body>
</html>
