<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dong Zihan - Personal Homepage</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            border-radius: 15px;
            margin-top: 20px;
            margin-bottom: 20px;
        }
        
        .header {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-radius: 15px;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 25px;
            display: block;
            border: 5px solid #fff;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s ease;
            position: relative;
            z-index: 1;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
        }
        
        h1 {
            margin: 0;
            color: #2c3e50;
            font-size: 2.8em;
            font-weight: 700;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .subtitle {
            color: #5a6c7d;
            font-size: 1.3em;
            margin-top: 10px;
            font-weight: 300;
            position: relative;
            z-index: 1;
        }
        
        .contact-info {
            margin-top: 25px;
            position: relative;
            z-index: 1;
        }
        
        .contact-info a {
            color: #3498db;
            text-decoration: none;
            margin: 0 15px;
            padding: 8px 16px;
            border-radius: 25px;
            transition: all 0.3s ease;
            display: inline-block;
            background: rgba(52, 152, 219, 0.1);
        }
        
        .contact-info a:hover {
            background: #3498db;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
        }
        
        .section {
            margin: 40px 0;
            padding: 30px;
            background: #f8f9fa;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
        }
        
        .section h2 {
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            padding-bottom: 15px;
            margin-bottom: 25px;
            font-size: 1.8em;
            position: relative;
        }
        
        .section h2::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 50px;
            height: 3px;
            background: #e74c3c;
        }
        
        .education-item, .experience-item {
            margin-bottom: 25px;
            padding: 20px;
            background: linear-gradient(135deg, #fff 0%, #f8f9fa 100%);
            border-left: 5px solid #3498db;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .education-item:hover, .experience-item:hover {
            transform: translateX(10px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }
        
        .publication {
            margin-bottom: 20px;
            padding: 20px;
            background: linear-gradient(135deg, #f1f3f4 0%, #e8eaf6 100%);
            border-radius: 8px;
            border-left: 4px solid #9c27b0;
            transition: all 0.3s ease;
        }
        
        .publication:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(156, 39, 176, 0.2);
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .skill-tag {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 0.9em;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .skill-tag:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
        }
        
        .about-text {
            font-size: 1.1em;
            line-height: 1.8;
            color: #555;
            text-align: justify;
        }
        
        .research-list {
            list-style: none;
            padding: 0;
        }
        
        .research-list li {
            padding: 12px 0;
            border-bottom: 1px solid #eee;
            position: relative;
            padding-left: 30px;
        }
        
        .research-list li::before {
            content: '▶';
            position: absolute;
            left: 0;
            color: #3498db;
            font-weight: bold;
        }
        
        .awards-list {
            list-style: none;
            padding: 0;
        }
        
        .awards-list li {
            padding: 15px;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #fff3cd 0%, #ffeaa7 100%);
            border-left: 4px solid #f39c12;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        .awards-list li:hover {
            transform: translateX(10px);
            box-shadow: 0 5px 15px rgba(243, 156, 18, 0.2);
        }
        
        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 30px 0;
            border-top: 2px solid #e9ecef;
            color: #6c757d;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 10px;
        }
        
        .placeholder {
            color: #999;
            font-style: italic;
            background: #f0f0f0;
            padding: 10px;
            border-radius: 5px;
            border: 2px dashed #ccc;
        }
        
        @media (max-width: 768px) {
            .container {
                margin: 10px;
                padding: 15px;
            }
            
            h1 {
                font-size: 2.2em;
            }
            
            .contact-info a {
                margin: 5px;
                display: block;
                text-align: center;
            }
            
            .skills {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <img src="微信图片_20250714182100.jpg" alt="Profile Photo" class="profile-img">
            <h1>Dong Zihan</h1>
            <div class="subtitle">Undergraduate Student | School of Computer Science and Software Engineering, Southwest Petroleum University</div>
            <div class="contact-info">
                <a href="mailto:202231036125@stu.swpu.edu.cn">📧 Email</a>
                <a href="https://github.com/Fly-By-Universe">💻 GitHub</a>
                <a href="#" class="placeholder">💼 LinkedIn (To be added)</a>
                <a href="#" class="placeholder">🎓 Google Scholar (To be added)</a>
            </div>
        </div>

        <!-- About Me Section -->
        <div class="section">
            <h2>About Me</h2>
            <p class="about-text">
                I am Dong Zihan, an undergraduate student at the School of Computer Science and Software Engineering, Southwest Petroleum University. I am currently working and studying at the Sichuan Provincial Engineering Research Center for Intelligent Oil and Gas Exploration and Development and the High-Performance Computing Center for Oil and Gas at Southwest Petroleum University. I was admitted to Southwest Petroleum University in 2022 and began studying Computer Science and Technology in 2024. I have received several provincial awards and scholarships. Currently, I am dedicated to research in semi-supervised clustering algorithms.
            </p>
        </div>

        <!-- Education Section -->
        <div class="section">
            <h2>Education</h2>
            <div class="education-item">
                <strong>Bachelor of Science in Computer Science and Technology</strong><br>
                Southwest Petroleum University, 2022 - Present<br>
                <em>Supervisor: Prof. Xie Wenbo</em><br>
                GPA: 4.00/5.00 | Rank: Top 9%
            </div>
            <div class="education-item">
                <strong>High School</strong><br>
                Fengrun Chezhou Mountain Middle School, Hebei, 2019 - 2022
            </div>
        </div>

        <!-- Research Interests Section -->
        <div class="section">
            <h2>Research Interests</h2>
            <ul class="research-list">
                <li>Semi-supervised Clustering</li>
                <li>Density Peak Clustering</li>
                <li class="placeholder">Additional research areas (To be added)</li>
                <li class="placeholder">Future research directions (To be added)</li>
            </ul>
        </div>

        <!-- Publications Section -->
        <div class="section">
            <h2>Publications</h2>
            <div class="placeholder">
                <p><strong>Publications will be added here as they become available</strong></p>
                <p>This section is reserved for future academic publications, conference papers, and journal articles.</p>
            </div>
        </div>

        <!-- Skills Section -->
        <div class="section">
            <h2>Skills & Expertise</h2>
            <div class="skills">
                <span class="skill-tag">Python</span>
                <span class="skill-tag">Machine Learning</span>
                <span class="skill-tag">Deep Learning</span>
                <span class="skill-tag">TensorFlow</span>
                <span class="skill-tag">PyTorch</span>
                <span class="skill-tag">Mathematical Competitions</span>
            </div>
        </div>

        <!-- Experience Section -->
        <div class="section">
            <h2>Experience</h2>
            <div class="placeholder">
                <p><strong>Professional experience will be added here</strong></p>
                <p>This section is reserved for internships, research positions, and professional work experience.</p>
            </div>
        </div>

        <!-- Awards & Honors Section -->
        <div class="section">
            <h2>Awards & Honors</h2>
            <ul class="awards-list">
                <li><strong>First Prize, National College Mathematics Competition (Provincial Level)</strong><br>
                    Chinese Mathematical Society, 2024</li>
                <li><strong>Second Prize, China Undergraduate Mathematical Contest in Modeling (Provincial Level)</strong><br>
                    China Society for Industrial and Applied Mathematics, 2024</li>
            </ul>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>Last Updated: July 14, 2025 | © Dong Zihan</p>
            <p>This website is designed for academic and professional purposes.</p>
        </div>
    </div>
</body>
</html>
