# portfolio-website
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd

cat > /var/www/html/index.html << 'EOL'
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rubeena Begum - AWS Portfolio</title>
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:Arial,sans-serif;background:linear-gradient(135deg,#000,#333,#000);color:#fff;animation:bg 8s infinite}
@keyframes bg{0%,100%{background:linear-gradient(135deg,#000,#333,#000)}50%{background:linear-gradient(135deg,#333,#000,#333)}}
.aws-banner{background:linear-gradient(45deg,#FF9900,#FFB366);color:#000;text-align:center;padding:15px;font-weight:bold}
.container{max-width:1000px;margin:0 auto;padding:20px}
.header{text-align:center;padding:40px 0}
.avatar{width:100px;height:100px;background:linear-gradient(45deg,#FFD700,#FFA500);border-radius:50%;margin:0 auto 20px;display:flex;align-items:center;justify-content:center;font-size:2.5em;animation:glow 2s infinite}
@keyframes glow{0%,100%{box-shadow:0 0 20px #FFD700}50%{box-shadow:0 0 40px #FFD700}}
h1{font-size:3em;background:linear-gradient(45deg,#FFD700,#FFFF00);-webkit-background-clip:text;-webkit-text-fill-color:transparent;margin-bottom:20px}
.contact{display:flex;justify-content:center;gap:20px;flex-wrap:wrap;margin-bottom:30px}
.contact-item{background:rgba(255,215,0,0.1);padding:10px 15px;border-radius:20px;border:2px solid #FFD700;display:flex;align-items:center;gap:8px}
.contact-item i{color:#FFD700}
.section{margin:30px 0;padding:25px;background:rgba(255,215,0,0.05);border-radius:15px;border-left:5px solid #FFD700}
.section h2{color:#FFD700;margin-bottom:15px;display:flex;align-items:center;gap:10px;text-transform:uppercase}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px;margin-top:20px}
.card{background:rgba(0,0,0,0.8);padding:20px;border-radius:10px;border:1px solid #FFD700}
.exp-item{margin:20px 0;padding:15px;background:rgba(255,215,0,0.05);border-radius:8px;border-left:3px solid #FFD700}
.exp-title{color:#FFD700;font-weight:bold;margin-bottom:5px;display:flex;align-items:center;gap:8px}
.company-logo{width:25px;height:25px;background:#FFD700;color:#000;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:0.7em;font-weight:bold}
.skills{display:flex;flex-wrap:wrap;gap:10px;margin-top:15px}
.skill{background:linear-gradient(45deg,#FFD700,#FFA500);color:#000;padding:8px 12px;border-radius:20px;font-weight:bold;display:flex;align-items:center;gap:5px}
.achievements li{list-style:none;padding:10px;margin:8px 0;background:rgba(255,215,0,0.1);border-radius:8px;border-left:3px solid #FFD700;padding-left:35px;position:relative}
.achievements li::before{content:'🏆';position:absolute;left:10px}
.lang-item{display:flex;align-items:center;gap:10px;margin:10px 0;padding:10px;background:rgba(255,215,0,0.1);border-radius:8px}
.scroll-btn{position:fixed;bottom:20px;right:20px;width:50px;height:50px;background:linear-gradient(45deg,#FFD700,#FFA500);border-radius:50%;display:flex;align-items:center;justify-content:center;cursor:pointer;color:#000}
@media (max-width:768px){h1{font-size:2em}.contact{flex-direction:column;align-items:center}.grid{grid-template-columns:1fr}}
</style>
</head>
<body>
<div class="aws-banner"><i class="fab fa-aws"></i> 🚀 AWS Cloud Mini Project - EC2 Portfolio | Cloud Computing Class</div>
<div class="container">
<header class="header">
<div class="avatar">👩‍💼</div>
<h1>RUBEENA BEGUM</h1>
<div class="contact">
<div class="contact-item"><i class="fas fa-map-marker-alt"></i><span>Hyderabad, Telangana</span></div>
<div class="contact-item"><i class="fas fa-phone"></i><span>+91 XXXXXXXXXX</span></div>
<div class="contact-item"><i class="fas fa-envelope"></i><span>portfolio.demo@cloudproject.com</span></div>
</div>
</header>

<section class="section">
<h2><i class="fas fa-user-tie"></i> Professional Summary</h2>
<p>MBA (HR) graduate with expertise in administrative and technical roles, including employee management, onboarding, and payroll. Proficient in computer applications and Apache HTTP server configuration. Currently exploring AWS cloud technologies through EC2 deployment projects.</p>
</section>

<section class="section">
<h2><i class="fas fa-briefcase"></i> Work Experience</h2>
<div class="exp-item">
<div class="exp-title"><div class="company-logo">NC</div>HR Admin – Nutrition Center</div>
<div style="color:#ccc;font-style:italic;margin-bottom:10px">Feb 2014 – Sept 2021</div>
<ul><li>Managed HR responsibilities: recruitment, onboarding, payroll</li><li>Maintained consultation calendar and employee data</li></ul>
</div>
<div class="exp-item">
<div class="exp-title"><div class="company-logo">SG</div>Associate – Sutherland Global Services</div>
<div style="color:#ccc;font-style:italic;margin-bottom:10px">Nov 2022 – Dec 2022</div>
<ul><li>Customer interaction and support services</li><li>Backend data entry and client communication</li></ul>
</div>
</section>

<div class="grid">
<div class="card">
<h2><i class="fas fa-graduation-cap"></i> Education</h2>
<div style="margin:10px 0"><strong>🎓 MBA in Human Resources</strong><br><span style="color:#ccc">Hyderabad Presidency College (2019-2021)</span></div>
<div style="margin:10px 0"><strong>💻 B.Com (Computers)</strong><br><span style="color:#ccc">International Degree College (2015-2018)</span></div>
<div style="margin:10px 0"><strong>📊 Intermediate (Accounts)</strong><br><span style="color:#ccc">Froebel Jr. College (2013-2015)</span></div>
</div>
<div class="card">
<h2><i class="fas fa-certificate"></i> Certifications</h2>
<div style="margin:10px 0">💻 <strong>PGDCA</strong> - Computer Applications</div>
<div style="margin:10px 0">💼 <strong>CA Basic Level</strong> - Chartered Accountant</div>
<div style="margin:10px 0">🔬 <strong>MLT</strong> - Medical Lab Technician</div>
</div>
</div>

<section class="section">
<h2><i class="fas fa-code"></i> Technical Skills</h2>
<div class="skills">
<span class="skill"><i class="fab fa-microsoft"></i>MS Office</span>
<span class="skill"><i class="fab fa-linux"></i>Apache HTTP</span>
<span class="skill"><i class="fas fa-database"></i>Data Management</span>
<span class="skill"><i class="fab fa-aws"></i>AWS EC2</span>
</div>
</section>

<section class="section">
<h2><i class="fas fa-users"></i> Interpersonal Skills</h2>
<div class="skills">
<span class="skill"><i class="fas fa-handshake"></i>Teamwork</span>
<span class="skill"><i class="fas fa-calendar-alt"></i>Event Planning</span>
<span class="skill"><i class="fas fa-comments"></i>Communication</span>
<span class="skill"><i class="fas fa-clipboard-list"></i>Organization</span>
</div>
</section>

<section class="section">
<h2><i class="fas fa-trophy"></i> Achievements</h2>
<ul class="achievements">
<li>Organized successful corporate and community events</li>
<li>Volunteered as Treasurer in nonprofit organization</li>
<li>Successfully deployed this portfolio on AWS EC2</li>
</ul>
</section>

<section class="section">
<h2><i class="fas fa-language"></i> Languages</h2>
<div class="lang-item">🇺🇸 <strong>English</strong> - Fluent</div>
<div class="lang-item">🕌 <strong>Urdu</strong> - Native</div>
<div class="lang-item">🇮🇳 <strong>Hindi</strong> - Conversational</div>
</section>

</div>
<div class="scroll-btn" onclick="window.scrollTo({top:0,behavior:'smooth'})"><i class="fas fa-arrow-up"></i></div>
</body>
</html>
EOL

chmod 644 /var/www/html/index.html
chown apache:apache /var/www/html/index.html
systemctl restart httpd
echo "Portfolio deployed successfully" > /var/log/deployment.log
