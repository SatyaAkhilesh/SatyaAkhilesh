import { useState } from 'react';

export default function Portfolio() {
  const [activeTab, setActiveTab] = useState('overview');
  
  const tabs = ['overview', 'experience', 'projects', 'skills'];
  
  const skills = [
    { name: 'AWS', level: 95 },
    { name: 'React/Next.js', level: 90 },
    { name: 'Node.js', level: 88 },
    { name: 'Python', level: 85 },
    { name: 'Kubernetes', level: 82 },
    { name: 'AI/LLMs', level: 80 },
  ];

  const experience = [
    {
      role: 'Full Stack & AI Engineer',
      company: 'MUNDO Prints',
      period: '2025 – Present',
      highlights: ['99.99% uptime', '42% revenue growth', '28% cost reduction']
    },
    {
      role: 'Cloud Platform Engineer',
      company: 'Nextrics',
      period: '2022 – 2023',
      highlights: ['99.9% availability', '40% faster load times', '50% faster releases']
    },
    {
      role: 'Developer',
      company: 'High Radius',
      period: '2022',
      highlights: ['$1M+ transactions/mo', '5,000+ concurrent users', 'PCI-DSS compliant']
    }
  ];

  const projects = [
    { name: 'serverless-ecommerce', desc: 'Serverless platform for 10K+ users', lang: 'TypeScript', stars: 42 },
    { name: 'ai-support-bot', desc: 'RAG-based customer support chatbot', lang: 'Python', stars: 38 },
    { name: 'microservices-framework', desc: 'K8s + Kafka migration toolkit', lang: 'Java', stars: 27 },
  ];

  const langColors = {
    TypeScript: '#3178c6',
    Python: '#3572A5',
    Java: '#b07219'
  };

  return (
    <div style={{ background: '#0d1117', minHeight: '100vh', color: '#e6edf3', fontFamily: '-apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif', padding: '20px' }}>
      
      {/* Header */}
      <div style={{ maxWidth: '900px', margin: '0 auto' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: '20px', marginBottom: '20px', flexWrap: 'wrap' }}>
          <div style={{ width: '80px', height: '80px', borderRadius: '50%', background: 'linear-gradient(135deg, #238636, #1f6feb)', display: 'flex', alignItems: 'center', justifyContent: 'center', fontSize: '28px', fontWeight: 'bold', border: '2px solid #30363d' }}>
            SP
          </div>
          <div>
            <h1 style={{ margin: 0, fontSize: '24px', fontWeight: 600 }}>Satya P</h1>
            <p style={{ margin: '4px 0', color: '#8b949e', fontSize: '14px' }}>@satya-akhilesh</p>
            <p style={{ margin: 0, color: '#8b949e', fontSize: '14px' }}>Senior Cloud & AI Engineer</p>
          </div>
        </div>
        
        <p style={{ color: '#8b949e', marginBottom: '15px', lineHeight: 1.5, fontSize: '14px' }}>
          AWS Certified • Building scalable serverless systems & AI integrations • MS @ Northeastern
        </p>
        
        <div style={{ display: 'flex', gap: '15px', flexWrap: 'wrap', marginBottom: '25px', fontSize: '13px', color: '#8b949e' }}>
          <span>📍 Boston, MA</span>
          <span>🏢 MUNDO Prints</span>
          <a href="mailto:satyaakhilesh0402@gmail.com" style={{ color: '#58a6ff', textDecoration: 'none' }}>✉️ Email</a>
          <a href="https://linkedin.com/in/satya-akhilesh-pulavarthi" style={{ color: '#58a6ff', textDecoration: 'none' }}>💼 LinkedIn</a>
        </div>

        {/* Tabs */}
        <div style={{ display: 'flex', gap: '0', borderBottom: '1px solid #30363d', marginBottom: '20px' }}>
          {tabs.map(tab => (
            <button
              key={tab}
              onClick={() => setActiveTab(tab)}
              style={{
                background: 'none',
                border: 'none',
                padding: '10px 16px',
                color: activeTab === tab ? '#e6edf3' : '#8b949e',
                cursor: 'pointer',
                fontSize: '14px',
                textTransform: 'capitalize',
                borderBottom: activeTab === tab ? '2px solid #f78166' : '2px solid transparent',
                marginBottom: '-1px'
              }}
            >
              {tab}
            </button>
          ))}
        </div>

        {/* Overview Tab */}
        {activeTab === 'overview' && (
          <div>
            <div style={{ display: 'grid', gridTemplateColumns: 'repeat(auto-fit, minmax(120px, 1fr))', gap: '15px', marginBottom: '25px' }}>
              {[
                { label: 'Uptime', value: '99.99%' },
                { label: 'Cost Saved', value: '28%' },
                { label: 'Users', value: '10K+' },
                { label: 'Deploy Speed', value: '+40%' }
              ].map(stat => (
                <div key={stat.label} style={{ background: '#161b22', border: '1px solid #30363d', borderRadius: '6px', padding: '15px', textAlign: 'center' }}>
                  <div style={{ fontSize: '22px', fontWeight: 'bold', color: '#58a6ff' }}>{stat.value}</div>
                  <div style={{ fontSize: '12px', color: '#8b949e' }}>{stat.label}</div>
                </div>
              ))}
            </div>
            
            <h3 style={{ fontSize: '14px', fontWeight: 600, marginBottom: '12px' }}>Pinned Repositories</h3>
            <div style={{ display: 'grid', gap: '12px' }}>
              {projects.map(p => (
                <div key={p.name} style={{ background: '#161b22', border: '1px solid #30363d', borderRadius: '6px', padding: '15px' }}>
                  <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'start' }}>
                    <div>
                      <span style={{ color: '#58a6ff', fontWeight: 600, fontSize: '14px' }}>📁 {p.name}</span>
                      <p style={{ color: '#8b949e', fontSize: '12px', margin: '6px 0' }}>{p.desc}</p>
                    </div>
                  </div>
                  <div style={{ display: 'flex', gap: '12px', fontSize: '12px', color: '#8b949e' }}>
                    <span><span style={{ display: 'inline-block', width: '10px', height: '10px', borderRadius: '50%', background: langColors[p.lang], marginRight: '4px' }}></span>{p.lang}</span>
                    <span>⭐ {p.stars}</span>
                  </div>
                </div>
              ))}
            </div>
          </div>
        )}

        {/* Experience Tab */}
        {activeTab === 'experience' && (
          <div style={{ display: 'grid', gap: '15px' }}>
            {experience.map((exp, i) => (
              <div key={i} style={{ background: '#161b22', border: '1px solid #30363d', borderRadius: '6px', padding: '20px' }}>
                <div style={{ display: 'flex', justifyContent: 'space-between', flexWrap: 'wrap', gap: '10px', marginBottom: '10px' }}>
                  <div>
                    <h3 style={{ margin: 0, fontSize: '16px', fontWeight: 600 }}>{exp.role}</h3>
                    <p style={{ margin: '4px 0 0', color: '#58a6ff', fontSize: '14px' }}>{exp.company}</p>
                  </div>
                  <span style={{ color: '#8b949e', fontSize: '13px' }}>{exp.period}</span>
                </div>
                <div style={{ display: 'flex', gap: '8px', flexWrap: 'wrap' }}>
                  {exp.highlights.map((h, j) => (
                    <span key={j} style={{ background: '#238636', color: '#fff', padding: '3px 10px', borderRadius: '20px', fontSize: '11px' }}>{h}</span>
                  ))}
                </div>
              </div>
            ))}
            
            <div style={{ background: '#161b22', border: '1px solid #30363d', borderRadius: '6px', padding: '20px' }}>
              <h3 style={{ margin: '0 0 10px', fontSize: '16px', fontWeight: 600 }}>Education</h3>
              <p style={{ margin: '0 0 5px', fontSize: '14px' }}>🎓 MS, Information Systems – <span style={{ color: '#58a6ff' }}>Northeastern University</span></p>
              <p style={{ margin: 0, fontSize: '14px' }}>🎓 BTech, ECE – <span style={{ color: '#58a6ff' }}>SRM University</span></p>
            </div>
          </div>
        )}

        {/* Projects Tab */}
        {activeTab === 'projects' && (
          <div style={{ display: 'grid', gap: '15px' }}>
            {[
              { name: 'serverless-ecommerce', desc: 'Full serverless e-commerce platform handling 10K+ concurrent users with 4× traffic scaling capability', lang: 'TypeScript', stars: 42, forks: 12 },
              { name: 'ai-support-bot', desc: 'RAG-based chatbot using AWS Bedrock & OpenAI for 45% faster responses and 30% higher satisfaction', lang: 'Python', stars: 38, forks: 8 },
              { name: 'microservices-framework', desc: 'Kubernetes + Kafka migration toolkit achieving 35% faster processing and 28% cost reduction', lang: 'Java', stars: 27, forks: 5 },
            ].map(p => (
              <div key={p.name} style={{ background: '#161b22', border: '1px solid #30363d', borderRadius: '6px', padding: '20px' }}>
                <h3 style={{ margin: '0 0 8px', fontSize: '16px' }}>
                  <span style={{ color: '#58a6ff' }}>📁 {p.name}</span>
                </h3>
                <p style={{ color: '#8b949e', fontSize: '13px', margin: '0 0 12px', lineHeight: 1.5 }}>{p.desc}</p>
                <div style={{ display: 'flex', gap: '15px', fontSize: '12px', color: '#8b949e' }}>
                  <span><span style={{ display: 'inline-block', width: '10px', height: '10px', borderRadius: '50%', background: langColors[p.lang], marginRight: '4px' }}></span>{p.lang}</span>
                  <span>⭐ {p.stars}</span>
                  <span>🍴 {p.forks}</span>
                </div>
              </div>
            ))}
          </div>
        )}

        {/* Skills Tab */}
        {activeTab === 'skills' && (
          <div>
            <div style={{ background: '#161b22', border: '1px solid #30363d', borderRadius: '6px', padding: '20px' }}>
              {skills.map(skill => (
                <div key={skill.name} style={{ marginBottom: '15px' }}>
                  <div style={{ display: 'flex', justifyContent: 'space-between', marginBottom: '5px', fontSize: '13px' }}>
                    <span>{skill.name}</span>
                    <span style={{ color: '#8b949e' }}>{skill.level}%</span>
                  </div>
                  <div style={{ background: '#30363d', borderRadius: '3px', height: '8px', overflow: 'hidden' }}>
                    <div style={{ width: `${skill.level}%`, height: '100%', background: 'linear-gradient(90deg, #238636, #2ea043)', borderRadius: '3px', transition: 'width 0.5s ease' }}></div>
                  </div>
                </div>
              ))}
            </div>
            
            <h3 style={{ fontSize: '14px', fontWeight: 600, margin: '25px 0 12px' }}>Tech Stack</h3>
            <div style={{ display: 'flex', flexWrap: 'wrap', gap: '8px' }}>
              {['AWS Lambda', 'API Gateway', 'DynamoDB', 'React', 'Next.js', 'Node.js', 'Python', 'FastAPI', 'Kubernetes', 'Docker', 'Kafka', 'Terraform', 'OpenAI', 'AWS Bedrock'].map(tech => (
                <span key={tech} style={{ background: '#30363d', padding: '5px 12px', borderRadius: '20px', fontSize: '12px' }}>{tech}</span>
              ))}
            </div>
          </div>
        )}
      </div>
    </div>
  );
}
