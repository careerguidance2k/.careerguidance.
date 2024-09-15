
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Career Development & Skill Matching</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            color: #333;
            background-color: #f8f9fa;
        }
        header {
            background-color: #007bff;
            color: #ffffff;
            padding: 30px 20px;
            text-align: center;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        section {
            padding: 20px;
            background-color: #ffffff;
            margin: 20px auto;
            max-width: 800px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        section h2 {
            margin-top: 0;
            border-bottom: 2px solid #007bff;
            padding-bottom: 10px;
            color: #007bff;
        }
        .form-step, .checkbox-group, .recommendations {
            margin-bottom: 20px;
        }
        .form-step label, .checkbox-group label {
            display: block;
            margin-bottom: 10px;
        }
        .form-step input, .form-step select, .checkbox-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .checkbox-group {
            display: flex;
            flex-direction: column; /* Ensures vertical stacking */
        }
        .checkbox-group input[type="checkbox"] {
            appearance: none; /* Remove default styling */
            width: 20px; /* Size of the circle */
            height: 20px; /* Size of the circle */
            border-radius: 50%; /* Makes the checkbox circular */
            border: 2px solid #007bff; /* Border color */
            background-color: #ffffff; /* Background color */
            cursor: pointer;
            position: relative;
            margin-right: 10px; /* Space between checkbox and label text */
        }
        .checkbox-group input[type="checkbox"]:checked::before {
            content: ''; /* Create a pseudo-element for checked state */
            position: absolute;
            top: 50%;
            left: 50%;
            width: 12px; /* Size of the inner dot */
            height: 12px; /* Size of the inner dot */
            background-color: #007bff; /* Dot color */
            border-radius: 50%; /* Makes the dot circular */
            transform: translate(-50%, -50%); /* Center the dot */
        }
        .step-navigation {
            text-align: center;
            margin-top: 20px;
        }
        .step-navigation button {
            background-color: #007bff;
            color: #ffffff;
            padding: 15px;
            font-size: 1.2em;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.3s;
        }
        .step-navigation button:hover {
            background-color: #0056b3;
            transform: translateY(-2px);
        }
        /* Updated styles for Step 3 */
        .recommendations {
            background-color: #e9ecef;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .recommendations h3 {
            font-size: 1.5em;
            color: #007bff;
            margin-bottom: 15px;
        }
        .recommendations ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        .recommendations li {
            background-color: #ffffff;
            border-radius: 5px;
            padding: 15px;
            margin: 10px 0;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, transform 0.3s;
        }
        .recommendations li:hover {
            background-color: #f1f3f5;
            transform: translateY(-2px);
        }
        .recommendations a {
            color: #007bff;
            text-decoration: none;
            font-weight: bold;
        }
        .recommendations a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <header>
        <h1>Career Development & Skill Matching</h1>
    </header>

    <section id="intro-page">
        <h2>Welcome</h2>
        <p>Welcome to your ultimate career advancement tool! Our platform is designed to help you identify your strengths, explore new career paths, and receive personalized recommendations tailored to your aspirations. By starting with some basic information and selecting your skills, you’ll unlock customized job and study suggestions that align with your career goals. Begin your journey today and find the perfect match for your skills and ambitions!</p>
        <div class="step-navigation">
            <button onclick="showSection('basic-info')">Get Started</button>
        </div>
    </section>

    <section id="basic-info" style="display:none;">
        <h2>Step 1: Basic Information</h2>
        <form id="basic-info-form">
            <div class="form-step">
                <label for="name">Full Name: <span style="color: red;">*</span></label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-step">
                <label for="education">Highest Level of Education: <span style="color: red;">*</span></label>
                <select id="education" name="education" required>
                    <option value="">Select</option>
                    <option value="high-school">High School</option>
                    <option value="associate-degree">Associate Degree</option>
                    <option value="bachelor-degree">Bachelor's Degree</option>
                    <option value="master-degree">Master's Degree</option>
                    <option value="doctorate-degree">Doctorate Degree</option>
                    <option value="diploma">Diploma</option>
                    <option value="certificate">Certificate</option>
                    <option value="professional-degree">Professional Degree</option>
                    <option value="postgraduate-diploma">Postgraduate Diploma</option>
                    <option value="foundation-degree">Foundation Degree</option>
                    <option value="vocational-training">Vocational Training</option>
                    <option value="online-courses">Online Courses</option>
                    <option value="part-time-study">Part-Time Study</option>
                    <option value="internship">Internship</option>
                    <option value="advanced-diploma">Advanced Diploma</option>
                    <option value="higher-national-certificate">Higher National Certificate (HNC)</option>
                    <option value="higher-national-diploma">Higher National Diploma (HND)</option>
                    <option value="professional-certification">Professional Certification</option>
                    <option value="technical-diploma">Technical Diploma</option>
                    <option value="graduate-certificate">Graduate Certificate</option>
                </select>
            </div>
            <div class="form-step">
                <label for="year-gap">Do you have any year gaps in your education? <span style="color: red;">*</span></label>
                <select id="year-gap" name="year-gap" onchange="handleYearGapChange()" required>
                    <option value="">Select</option>
                    <option value="none">None</option>
                    <option value="1-year">1 Year</option>
                    <option value="2-years">2 Years</option>
                    <option value="3-years">3 Years</option>
                    <option value="4-years">4 Years</option>
                    <option value="5-years">5 Years</option>
                    <option value="more-than-5-years">More than 5 Years</option>
                </select>
            </div>
            <div id="gap-reason-container" style="display:none;">
                <div class="form-step">
                    <label for="gap-reason">Reason for Year Gap:</label>
                    <textarea id="gap-reason" name="gap-reason" rows="4" placeholder="Please provide a brief explanation if applicable."></textarea>
                </div>
            </div>
            <div class="step-navigation">
                <button type="button" onclick="showSection('skills')">Next Step</button>
            </div>
        </form>
    </section>

    <section id="skills" style="display:none;">
        <h2>Step 2: Select Your Skills</h2>
        <form id="skills-form">
            <div class="checkbox-group">
                <label><input type="checkbox" name="skills" value="Web Development"> Web Development</label>
                <label><input type="checkbox" name="skills" value="Digital Marketing"> Digital Marketing</label>
                <label><input type="checkbox" name="skills" value="Data Analysis"> Data Analysis</label>
                <label><input type="checkbox" name="skills" value="Cloud Computing"> Cloud Computing</label>
                <label><input type="checkbox" name="skills" value="Graphic Design"> Graphic Design</label>
                <label><input type="checkbox" name="skills" value="Networking"> Networking</label>
                <label><input type="checkbox" name="skills" value="Project Management"> Project Management</label>
                <label><input type="checkbox" name="skills" value="Cybersecurity"> Cybersecurity</label>
                <label><input type="checkbox" name="skills" value="Artificial Intelligence"> Artificial Intelligence</label>
                <label><input type="checkbox" name="skills" value="Machine Learning"> Machine Learning</label>
                <label><input type="checkbox" name="skills" value="Software Engineering"> Software Engineering</label>
                <label><input type="checkbox" name="skills" value="Database Management"> Database Management</label>
                <label><input type="checkbox" name="skills" value="User Experience Design"> User Experience Design</label>
                <label><input type="checkbox" name="skills" value="Video Editing"> Video Editing</label>
                <label><input type="checkbox" name="skills" value="Content Writing"> Content Writing</label>
                <label><input type="checkbox" name="skills" value="Business Analysis"> Business Analysis</label>
                <label><input type="checkbox" name="skills" value="Sales Management"> Sales Management</label>
                <label><input type="checkbox" name="skills" value="Customer Service"> Customer Service</label>
                <label><input type="checkbox" name="skills" value="Supply Chain Management"> Supply Chain Management</label>
                <label><input type="checkbox" name="skills" value="Finance Management"> Finance Management</label>
            </div>
            <div class="step-navigation">
                <button type="button" onclick="showSection('recommendations')">Get Recommendations</button>
            </div>
        </form>
    </section>

    <section id="recommendations" style="display:none;">
        <h2>Step 3: Job and Study Recommendations</h2>
        <div id="job-recommendations" class="recommendations">
            <!-- Job Recommendations will be dynamically inserted here -->
        </div>
        <div id="study-recommendations" class="recommendations">
            <!-- Study Recommendations will be dynamically inserted here -->
        </div>
        <div class="step-navigation">
            <button type="button" onclick="showSection('intro-page')">Start Over</button>
        </div>
    </section>

    <script>
        function showSection(sectionId) {
    const sections = document.querySelectorAll('section');
    sections.forEach(section => section.style.display = 'none');
    document.getElementById(sectionId).style.display = 'block';
}

function handleYearGapChange() {
    const yearGap = document.getElementById('year-gap').value;
    const gapReasonContainer = document.getElementById('gap-reason-container');
    const jobRecommendations = document.getElementById('job-recommendations');
    const studyRecommendations = document.getElementById('study-recommendations');
    const education = document.getElementById('education').value;

    // Show or hide the gap reason container
    if (yearGap !== "none") {
        gapReasonContainer.style.display = 'block';
    } else {
        gapReasonContainer.style.display = 'none';
    }

    // Provide recommendations based on year gap and education level
    if (yearGap !== "none") {
        // Show recommendations for users with a gap
        jobRecommendations.innerHTML = `
            <h3>Your Job Recommendations:</h3>
            <ul>
                <li>Freelance Web Developer</li>
                <li>Remote Content Creator</li>
                <li>Part-Time Customer Support</li>
                <li>Freelance Consultant</li>
                <li>Part-Time Project Coordinator</li>
                <li>Virtual Assistant</li>
                <li>Freelance Graphic Designer</li>
                <li>Online Tutor</li>
                <li>Social Media Manager</li>
                <li>Technical Support Specialist</li>
            </ul>`;
        studyRecommendations.innerHTML = `
            <h3>Your Study Recommendations:</h3>
            <ul>
                <li><a href="https://www.coursera.org/specializations/digital-marketing" target="_blank">Online Certification in Digital Marketing</a></li>
                <li><a href="https://www.udacity.com/course/data-analyst-nanodegree--nd002" target="_blank">Part-Time Data Science Course</a></li>
                <li><a href="https://www.edx.org/course/emerging-technologies" target="_blank">Short Courses in Emerging Technologies</a></li>
                <li><a href="https://www.linkedin.com/learning" target="_blank">LinkedIn Learning Courses</a></li>
                <li><a href="https://www.udemy.com" target="_blank">Udemy Courses</a></li>
            </ul>`;
    } else {
        // Show recommendations for users without a gap
        let jobs = '';
        let studies = '';

        if (education === "bachelor-degree" || education === "master-degree") {
            jobs = `
                <li>Software Engineer</li>
                <li>Data Analyst</li>
                <li>Marketing Manager</li>
                <li>Project Manager</li>
                <li>UI/UX Designer</li>
                <li>Business Intelligence Analyst</li>
                <li>Product Manager</li>
                <li>Solutions Architect</li>
                <li>Technical Lead</li>
                <li>Operations Manager</li>
            `;
            studies = `
                <li><a href="https://www.coursera.org/learn/ai-machine-learning" target="_blank">Master's in AI and Machine Learning</a></li>
                <li><a href="https://www.cybrary.it/course/cyber-security-certification/" target="_blank">Certification in Cybersecurity</a></li>
                <li><a href="https://www.datacamp.com/learn/data-science" target="_blank">Advanced Data Science and Analytics Program</a></li>
                <li><a href="https://www.edx.org/course/advanced-project-management" target="_blank">Advanced Project Management</a></li>
                <li><a href="https://www.coursera.org/specializations/data-science" target="_blank">Specialization in Data Science</a></li>
            `;
        } else if (education === "high-school" || education === "associate-degree") {
            jobs = `
                <li>Sales Executive</li>
                <li>Customer Support Specialist</li>
                <li>Junior Web Developer</li>
                <li>Digital Marketing Assistant</li>
                <li>Network Technician</li>
                <li>Administrative Assistant</li>
                <li>Retail Manager</li>
                <li>Help Desk Technician</li>
                <li>Field Service Technician</li>
                <li>Project Assistant</li>
            `;
            studies = `
                <li><a href="https://www.coursera.org/specializations/web-development" target="_blank">Web Development Specialization</a></li>
                <li><a href="https://www.udemy.com/course/digital-marketing/" target="_blank">Digital Marketing Course</a></li>
                <li><a href="https://www.edx.org/course/it-fundamentals-for-business-professionals" target="_blank">IT Fundamentals for Business Professionals</a></li>
                <li><a href="https://www.linkedin.com/learning/tech-skills" target="_blank">LinkedIn Learning Tech Skills</a></li>
                <li><a href="https://www.udacity.com/course/intro-to-computer-science--ud1110" target="_blank">Intro to Computer Science</a></li>
            `;
        } else {
            jobs = `
                <li>Administrative Assistant</li>
                <li>Retail Sales Associate</li>
                <li>Customer Service Representative</li>
                <li>Warehouse Assistant</li>
                <li>Data Entry Clerk</li>
                <li>Receptionist</li>
                <li>Inventory Clerk</li>
                <li>Office Assistant</li>
                <li>Shipping Coordinator</li>
                <li>Junior Sales Representative</li>
            `;
            studies = `
                <li><a href="https://www.coursera.org/learn/essential-management-skills" target="_blank">Essential Management Skills</a></li>
                <li><a href="https://www.edx.org/course/introduction-to-it" target="_blank">Introduction to IT</a></li>
                <li><a href="https://www.udemy.com/course/business-communication/" target="_blank">Business Communication Course</a></li>
                <li><a href="https://www.coursera.org/specializations/operations-management" target="_blank">Operations Management Specialization</a></li>
                <li><a href="https://www.udacity.com/course/intro-to-data-analysis--ud170" target="_blank">Intro to Data Analysis</a></li>
            `;
        }

        jobRecommendations.innerHTML = `
            <h3>Your Job Recommendations:</h3>
            <ul>${jobs}</ul>`;
        studyRecommendations.innerHTML = `
            <h3>Your Study Recommendations:</h3>
            <ul>${studies}</ul>`;
    }
}

    </script>
</body>
</html>
