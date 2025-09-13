<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kenzy Elmoataz Bden Allah | Data Analyst Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6366F1;
            --secondary: #8B5CF6;
            --accent: #EC4899;
            --teal: #14B8A6;
            --yellow: #F59E0B;
            --light: #F9FAFB;
            --dark: #111827;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: white;
            scroll-behavior: smooth;
        }

        .gradient-text {
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .gradient-bg {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
        }

        .profile-section {
            background: linear-gradient(to bottom, #ffffff 0%, #f9fafb 100%);
        }

        .profile-pic {
            border: 8px solid rgba(255, 255, 255, 0.9);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .section-title {
            position: relative;
            display: inline-block;
        }

        .section-title:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 4px;
            bottom: -8px;
            left: 0;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            border-radius: 2px;
        }

        .card {
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            backface-visibility: hidden;
        }

        .card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
        }

        .skill-meter {
            height: 8px;
            background-color: #E5E7EB;
            border-radius: 4px;
        }

        .skill-level {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            border-radius: 4px;
        }

        .timeline-item:not(:last-child):after {
            content: '';
            position: absolute;
            left: 28px;
            top: 40px;
            height: calc(100% - 40px);
            width: 2px;
            background: var(--primary);
            opacity: 0.2;
        }

        .timeline-dot {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            border: 4px solid white;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .nav-link {
            position: relative;
        }

        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            transition: width 0.3s ease;
        }

        .nav-link:hover:after {
            width: 100%;
        }

        .blob {
            position: absolute;
            border-radius: 50%;
            filter: blur(60px);
            opacity: 0.1;
            z-index: -1;
        }

        .project-tag {
            transition: all 0.3s ease;
        }

        .project-card:hover .project-tag {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }

        .contact-card {
            transition: all 0.3s ease;
        }

        .contact-card:hover {
            transform: translateY(-5px);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="fixed w-full bg-white shadow-sm z-50">
        <div class="max-w-7xl mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <div class="text-2xl font-bold gradient-text">Kenzy Elmoataz Bden Allah</div>
                
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="nav-link text-gray-700 hover:text-gray-900">Home</a>
                    <a href="#about" class="nav-link text-gray-700 hover:text-gray-900">About</a>
                    <a href="#skills" class="nav-link text-gray-700 hover:text-gray-900">Skills</a>
                    <a href="#experience" class="nav-link text-gray-700 hover:text-gray-900">Experience</a>
                    <a href="#projects" class="nav-link text-gray-700 hover:text-gray-900">Projects</a>
                    <a href="#contact" class="nav-link text-gray-700 hover:text-gray-900">Contact</a>
                </div>
                
                <button id="menu-toggle" class="md:hidden text-gray-700">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
        </div>
    </nav>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="hidden md:hidden fixed inset-0 bg-white/95 backdrop-blur-lg z-40 pt-20 px-6">
        <div class="flex flex-col space-y-6 text-lg">
            <a href="#home" class="py-3 text-gray-700 hover:text-gray-900 border-b border-gray-100">Home</a>
            <a href="#about" class="py-3 text-gray-700 hover:text-gray-900 border-b border-gray-100">About</a>
            <a href="#skills" class="py-3 text-gray-700 hover:text-gray-900 border-b border-gray-100">Skills</a>
            <a href="#experience" class="py-3 text-gray-700 hover:text-gray-900 border-b border-gray-100">Experience</a>
            <a href="#projects" class="py-3 text-gray-700 hover:text-gray-900 border-b border-gray-100">Projects</a>
            <a href="#contact" class="py-3 text-gray-700 hover:text-gray-900 border-b border-gray-100">Contact</a>
        </div>
    </div>

    <!-- Profile Section -->
  <section id="home" class="profile-section pt-32 pb-20 relative overflow-hidden">
    <!-- Background Blobs -->
    <div class="blob w-96 h-96 bg-purple-300 -top-20 -left-20"></div>
    <div class="blob w-80 h-80 bg-pink-300 top-1/3 right-10"></div>
    <div class="blob w-64 h-64 bg-blue-300 bottom-1/4 left-1/3"></div>
    
    <div class="max-w-7xl mx-auto px-6">
        <div class="flex flex-col lg:flex-row items-center">
            
            <!-- Profile Picture -->
            <div class="lg:w-2/5 mb-12 lg:mb-0 flex justify-center">
                <div class="relative">
                    <div class="absolute -inset-4 bg-gradient-to-r from-indigo-200 to-pink-200 rounded-full rotate-3 animate-pulse"></div>
                    <img src="https://kenzy-moataz.static.domains/professional%20photo.jpg" 
                         alt="Professional photo of Kenzy Elmoataz Bden Allah" 
                         class="relative rounded-full w-85 h-85 object-cover profile-pic">
                </div>
            </div>
            
            <!-- Profile Content -->
            <div class="lg:w-3/5 lg:pl-12">
                <h1 class="text-4xl md:text-5xl font-bold text-gray-900 leading-tight mb-4">
                    Hi, I'm <span class="gradient-text">Kenzy Elmoataz Bden Allah</span>
                </h1>
                <h2 class="text-2xl md:text-3xl font-semibold text-gray-700 mb-6">
                    Data Analyst | Transforming Data Into Strategic Insights
                </h2>
                <p class="text-lg text-gray-600 mb-8 max-w-2xl">
                    I specialize in transforming complex datasets into clear, actionable business insights. With a passion for data storytelling and a commitment to accuracy, I help organizations make informed decisions that drive growth and efficiency.
                </p>
                
                <!-- Contact Information -->
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mb-10">
                    
                    <!-- Email -->
                    <a href="mailto:kenzymoataz11@gmail.com" class="contact-card bg-white p-4 rounded-xl shadow-sm border-l-4 border-indigo-500 block hover:shadow-md transition">
                        <div class="flex items-center">
                            <div class="bg-indigo-100 p-3 rounded-full mr-4">
                                <i class="fas fa-envelope text-indigo-600"></i>
                            </div>
                            <div>
                                <h4 class="text-sm text-gray-500">Email</h4>
                                <p class="font-medium text-gray-800">kenzymoataz11@gmail.com</p>
                            </div>
                        </div>
                    </a>
                    
                    <!-- Phone -->
                    <a href="tel:+201278777555" class="contact-card bg-white p-4 rounded-xl shadow-sm border-l-4 border-pink-500 block hover:shadow-md transition">
                        <div class="flex items-center">
                            <div class="bg-pink-100 p-3 rounded-full mr-4">
                                <i class="fas fa-phone-alt text-pink-600"></i>
                            </div>
                            <div>
                                <h4 class="text-sm text-gray-500">Phone</h4>
                                <p class="font-medium text-gray-800">01278777555</p>
                            </div>
                        </div>
                    </a>
                    
                    <!-- Location -->
                    <a href="https://www.google.com/maps/place/6th+October+City,+Giza,+Egypt" target="_blank" class="contact-card bg-white p-4 rounded-xl shadow-sm border-l-4 border-purple-500 block hover:shadow-md transition">
                        <div class="flex items-center">
                            <div class="bg-purple-100 p-3 rounded-full mr-4">
                                <i class="fas fa-map-marker-alt text-purple-600"></i>
                            </div>
                            <div>
                                <h4 class="text-sm text-gray-500">Location</h4>
                                <p class="font-medium text-gray-800">6th October, Giza, Egypt</p>
                            </div>
                        </div>
                    </a>
                    
                    <!-- Resume -->
                    <a href="https://drive.google.com/file/d/1f4nDSMcWp1RrdQzd6QAr6qazknY4N_ZL/view?usp=sharing" target="_blank" class="contact-card bg-white p-4 rounded-xl shadow-sm border-l-4 border-teal-500 block hover:shadow-md transition">
                        <div class="flex items-center">
                            <div class="bg-teal-100 p-3 rounded-full mr-4">
                                <i class="fas fa-file-alt text-teal-600"></i>
                            </div>
                            <div>
                                <h4 class="text-sm text-gray-500">Resume</h4>
                                <p class="font-medium text-blue-600">View My CV</p>
                            </div>
                        </div>
                    </a>
                </div>
                
                <!-- Social Links -->
                <div class="flex space-x-4 mb-8">
                    <a href="https://www.linkedin.com/in/kenzy-moataz/" target="_blank" class="bg-indigo-100 p-3 rounded-full text-indigo-600 hover:bg-indigo-200 transition">
                        <i class="fab fa-linkedin-in text-xl"></i>
                    </a>
                    <a href="https://wa.me/201278777555" target="_blank" class="bg-indigo-100 p-3 rounded-full text-green-600 hover:bg-green-200 transition">
                        <i class="fab fa-whatsapp text-xl"></i>
                    </a>
                </div>
                
                <!-- Call-to-action buttons -->
                <div class="flex flex-wrap gap-4">
                    <a href="#projects" class="gradient-bg text-white px-6 py-3 rounded-lg font-medium hover:shadow-lg transition">
                        View My Projects
                    </a>
                    <a href="#contact" class="border-2 border-gray-300 text-gray-700 px-6 py-3 rounded-lg font-medium hover:bg-gray-50 transition">
                        Contact Me
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>

   <!-- About Section -->
<section id="about" class="py-20 bg-white">
  <div class="max-w-5xl mx-auto px-6 text-center">
    <!-- Title -->
    <div class="mb-16">
      <h2 class="text-3xl font-bold text-gray-900 mb-4">
        <span class="section-title">About Me</span>
      </h2>
      <p class="text-gray-600 max-w-2xl mx-auto">
        I am Kenzy Elmoataz Bden Allah, a Business Administration student at Misr University For Science and Technology, 
        and Data Analyst transforming complex datasets into actionable insights with high-quality, accuracy and clarity. 
        I help organizations make informed decisions in the right way to stay developed.
      </p>
    </div>

    <!-- Content -->
    <div class="max-w-3xl mx-auto">
      <h3 class="text-2xl font-semibold text-gray-900 mb-6">
        Transforming Data Into Business Value
      </h3>
      <p class="text-gray-600 mb-6">
        I am a data analyst specializing in transforming complex datasets into actionable insights with a commitment to 
        high quality, accuracy, and clarity. I help organizations make informed decisions the right way, enabling them 
        to stay competitive and develop effectively.
      </p>
      <p class="text-gray-600 mb-10">
        With expertise in Power BI and data visualization tools, I bridge the gap between raw data and strategic business decisions. 
        My approach combines technical skills with clear communication to deliver insights that stakeholders can understand and act upon.
      </p>

      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-left">
        <div class="flex items-start space-x-4">
          <div class="flex-shrink-0 bg-indigo-100 p-3 rounded-full text-indigo-600">
            <i class="fas fa-chart-line text-xl"></i>
          </div>
          <div>
            <h4 class="font-semibold text-gray-900 mb-2">Data-Driven Decisions</h4>
            <p class="text-gray-600">Every recommendation backed by thorough analysis and validation</p>
          </div>
        </div>
        <div class="flex items-start space-x-4">
          <div class="flex-shrink-0 bg-pink-100 p-3 rounded-full text-pink-600">
            <i class="fas fa-shield-alt text-xl"></i>
          </div>
          <div>
            <h4 class="font-semibold text-gray-900 mb-2">Quality Focus</h4>
            <p class="text-gray-600">Rigorous verification processes ensure accurate outputs</p>
          </div>
        </div>
        <div class="flex items-start space-x-4">
          <div class="flex-shrink-0 bg-purple-100 p-3 rounded-full text-purple-600">
            <i class="fas fa-comments text-xl"></i>
          </div>
          <div>
            <h4 class="font-semibold text-gray-900 mb-2">Clear Communication</h4>
            <p class="text-gray-600">Technical findings translated into business recommendations</p>
          </div>
        </div>
        <div class="flex items-start space-x-4">
          <div class="flex-shrink-0 bg-teal-100 p-3 rounded-full text-teal-600">
            <i class="fas fa-tools text-xl"></i>
          </div>
          <div>
            <h4 class="font-semibold text-gray-900 mb-2">Tool Proficiency</h4>
            <p class="text-gray-600">Skilled in Power BI</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Skills Section -->
<section id="skills" class="py-20 bg-gray-50">
  <div class="max-w-5xl mx-auto px-6 text-center">
    <div class="mb-16">
      <h2 class="text-3xl font-bold text-gray-900 mb-4">
        <span class="section-title">Skills & Expertise</span>
      </h2>
      <p class="text-gray-600 max-w-2xl mx-auto">
        Technical and Personal skills I've developed through experience
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 text-left">
      <!-- Technical Skills -->
      <div>
        <h3 class="text-xl font-semibold text-gray-900 border-b pb-2 mb-6">Technical Skills</h3>
        <div class="space-y-6">
          <div>
            <div class="flex justify-between mb-2">
              <span class="font-medium text-gray-700">Database Management</span>
              <span class="text-indigo-600 font-medium">90%</span>
            </div>
            <div class="skill-meter"><div class="skill-level" style="width: 90%"></div></div>
          </div>
          <div>
            <div class="flex justify-between mb-2">
              <span class="font-medium text-gray-700">Power Query</span>
              <span class="text-indigo-600 font-medium">90%</span>
            </div>
            <div class="skill-meter"><div class="skill-level" style="width: 90%"></div></div>
          </div>
          <div>
            <div class="flex justify-between mb-2">
              <span class="font-medium text-gray-700">Data Visualization (Power BI)</span>
              <span class="text-indigo-600 font-medium">92%</span>
            </div>
            <div class="skill-meter"><div class="skill-level" style="width: 92%"></div></div>
          </div>
        </div>
      </div>

      <!-- Personal Skills -->
      <div>
        <h3 class="text-xl font-semibold text-gray-900 border-b pb-2 mb-6">Personal Skills</h3>
        <div class="space-y-6">
          <div>
            <div class="flex justify-between mb-2">
              <span class="font-medium text-gray-700">Communication</span>
              <span class="text-indigo-600 font-medium">93%</span>
            </div>
            <div class="skill-meter"><div class="skill-level" style="width: 93%"></div></div>
          </div>
          <div>
            <div class="flex justify-between mb-2">
              <span class="font-medium text-gray-700">Teamwork</span>
              <span class="text-indigo-600 font-medium">90%</span>
            </div>
            <div class="skill-meter"><div class="skill-level" style="width: 90%"></div></div>
          </div>
          <div>
            <div class="flex justify-between mb-2">
              <span class="font-medium text-gray-700">Time Management</span>
              <span class="text-indigo-600 font-medium">90%</span>
            </div>
            <div class="skill-meter"><div class="skill-level" style="width: 90%"></div></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Call to action -->
    <div class="mt-16 text-center">
      <a href="#experience" class="inline-flex items-center text-indigo-600 hover:text-indigo-800 font-medium">
        <span>View My Experience</span>
        <i class="fas fa-arrow-right ml-2"></i>
      </a>
    </div>
  </div>
</section>


    <!-- Experience Section -->
    <section id="experience" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-4">
                    <span class="section-title">Work Experience</span>
                </h2>
                <p class="text-gray-600 max-w-2xl mx-auto">
                    My professional journey 
                </p>
            </div>
            
            <div class="max-w-3xl mx-auto space-y-10">
                <div class="card bg-white p-8 rounded-xl shadow-sm relative pl-14 timeline-item">
                    <div class="timeline-dot absolute left-8 top-8"></div>
                    
                    <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-2">
                        <div>
                            <h3 class="text-xl font-semibold text-gray-900">Microsoft Power Bi</h3>
                            <p class="text-gray-600">Digital Egypt Initiative (DEPI)</p>
                        </div>
                        <div class="text-indigo-600 font-medium">June 2025 - Present</div>
                    </div>
                    <p class="text-gray-500 text-sm mb-4"></p>
                    <ul class="text-gray-600 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-indigo-500 mt-1 mr-2 text-xs"></i>
                            <span>Cleaning and Analysis Data</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-indigo-500 mt-1 mr-2 text-xs"></i>
                            <span>Data Visualization </span>
                        </li>
                                            </ul>
                </div>
                
                <div class="card bg-white p-8 rounded-xl shadow-sm relative pl-14 timeline-item">
                    <div class="timeline-dot absolute left-8 top-8"></div>
                    
                    <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-2">
                        <div>
                            <h3 class="text-xl font-semibold text-gray-900">Internship</h3>
                            <p class="text-gray-600">Commercial International Bank (CIB)</p>
                        </div>
                        <div class="text-indigo-600 font-medium">July 2025 - Aug.2025</div>
                    </div>
                    <p class="text-gray-500 text-sm mb-4">Egypt</p>
                    <ul class="text-gray-600 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-indigo-500 mt-1 mr-2 text-xs"></i>
                            <span>Sustainability and its importance in banking</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-indigo-500 mt-1 mr-2 text-xs"></i>
                            <span>AI uses in banking</span>
                        </li>
                                            </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-900 mb-4">
                    <span class="section-title">Featured Projects</span>
                </h2>
                <p class="text-gray-600 max-w-2xl mx-auto">
                    Selected data analysis projects demonstrating my skills
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="project-card card bg-white rounded-xl shadow-sm overflow-hidden">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://kenzy-moataz.static.domains/Screenshot%202025-08-20%20171027.png" alt="Data Analysis dashboard showing Layoffs Data" class="w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/30 to-transparent"></div>
                    </div>
                    <div class="p-6">
                        <span class="project-tag inline-block px-3 py-1 text-xs font-semibold bg-indigo-100 text-indigo-800 rounded-full mb-3">Data Analysis</span>
                        <h3 class="text-xl font-semibold text-gray-900 mb-3">Layoffs Data Dashboard</h3>
                        <p class="text-gray-600 mb-4">
                            Interactive dashboard analyzing layoffs data to understand trends, patterns, and impacts of layoffs on various sectors.
                        </p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-indigo-100 text-indigo-800 text-xs px-2 py-1 rounded">Power Bi</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs px-2 py-1 rounded">SQL</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs px-2 py-1 rounded">Power Query</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card card bg-white rounded-xl shadow-sm overflow-hidden">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://kenzy-moataz.static.domains/Screenshot%202025-08-20%20173626.png" alt="Data Analysis for titanic data" class="w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/30 to-transparent"></div>
                    </div>
                    <div class="p-6">
                        <span class="project-tag inline-block px-3 py-1 text-xs font-semibold bg-pink-100 text-pink-800 rounded-full mb-3">Data Analysis</span>
                        <h3 class="text-xl font-semibold text-gray-900 mb-3">Titanic Passengers</h3>
                        <p class="text-gray-600 mb-4">
                    This project aims to analyze the survival rates of Titanic passengers based on their ticket categories (classes) and their family or partner relationships.
                        </p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-pink-100 text-pink-800 text-xs px-2 py-1 rounded">Power Bi</span>
                            <span class="bg-pink-100 text-pink-800 text-xs px-2 py-1 rounded">SQL</span>
                            <span class="bg-pink-100 text-pink-800 text-xs px-2 py-1 rounded">Power Query</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card card bg-white rounded-xl shadow-sm overflow-hidden">
                    <div class="h-48 overflow-hidden relative">
                        <img src="https://kenzy-moataz.static.domains/Screenshot%202025-08-20%20171323.png" alt="Analysis of banking customer data" class="w-full h-full object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/30 to-transparent"></div>
                    </div>
                    <div class="p-6">
                        <span class="project-tag inline-block px-3 py-1 text-xs font-semibold bg-purple-100 text-purple-800 rounded-full mb-3">Data Analysis</span>
                        <h3 class="text-xl font-semibold text-gray-900 mb-3">Banking customer data</h3>
                        <p class="text-gray-600 mb-4">
                           Overview of the bank customer data analysis,understanding customer demographics and financial behavior.
                        </p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-purple-100 text-purple-800 text-xs px-2 py-1 rounded">Excel</span>
                            <span class="bg-purple-100 text-purple-800 text-xs px-2 py-1 rounded">Power Query</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 text-center">
                <a href="#contact" class="inline-flex items-center text-indigo-600 hover:text-indigo-800 font-medium">
                    <span>Ready to discuss your project?</span>
                    <i class="fas fa-arrow-right ml-2"></i>
                </a>
            </div>
        </div>
    </section>

   <!-- Contact Section -->
<section id="contact" class="py-20 bg-gradient-to-r from-indigo-500 to-purple-600 text-white">
  <div class="max-w-5xl mx-auto px-6 text-center">
    <!-- Section Title -->
    <div class="mb-16">
      <h2 class="text-3xl font-bold mb-4">
        Get In <span class="text-white">Touch</span>
      </h2>
      <p class="text-indigo-100 max-w-2xl mx-auto">
        Have a data challenge? I'd love to hear about your project.
      </p>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 text-left">
      <!-- Contact Form -->
      <div>
        <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-6">
          <div>
            <label for="name" class="block text-gray-200 mb-2">Your Name</label>
            <input type="text" id="name" name="name" required
              class="w-full px-4 py-3 bg-white/10 backdrop-blur-sm border border-white/20 rounded-lg 
              focus:ring-2 focus:ring-white focus:border-white text-white placeholder-gray-300">
          </div>
          <div>
            <label for="email" class="block text-gray-200 mb-2">Email Address</label>
            <input type="email" id="email" name="_replyto" required
              class="w-full px-4 py-3 bg-white/10 backdrop-blur-sm border border-white/20 rounded-lg 
              focus:ring-2 focus:ring-white focus:border-white text-white placeholder-gray-300">
          </div>
          <div>
            <label for="subject" class="block text-gray-200 mb-2">Subject</label>
            <input type="text" id="subject" name="subject"
              class="w-full px-4 py-3 bg-white/10 backdrop-blur-sm border border-white/20 rounded-lg 
              focus:ring-2 focus:ring-white focus:border-white text-white placeholder-gray-300">
          </div>
          <div>
            <label for="message" class="block text-gray-200 mb-2">Message</label>
            <textarea id="message" name="message" rows="5" required
              class="w-full px-4 py-3 bg-white/10 backdrop-blur-sm border border-white/20 rounded-lg 
              focus:ring-2 focus:ring-white focus:border-white text-white placeholder-gray-300"></textarea>
          </div>
          <button type="submit"
            class="w-full bg-white text-indigo-600 py-3 px-6 rounded-lg font-medium hover:bg-gray-100 transition">
            Send Message
          </button>
        </form>
      </div>

      <!-- Contact Info -->
      <div class="flex flex-col justify-between">
        <div>
          <h3 class="text-xl font-semibold mb-6">Contact Information</h3>
          <div class="space-y-6">
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 bg-white/10 p-3 rounded-lg text-white">
                <i class="fas fa-envelope"></i>
              </div>
              <div>
                <h4 class="font-medium text-white">Email</h4>
                <a href="mailto:kenzymoataz11@gmail.com" class="text-indigo-100 hover:underline">
                  kenzymoataz11@gmail.com
                </a>
              </div>
            </div>
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 bg-white/10 p-3 rounded-lg text-white">
                <i class="fas fa-phone-alt"></i>
              </div>
              <div>
                <h4 class="font-medium text-white">Phone</h4>
                <a href="tel:+201278777555" class="text-indigo-100 hover:underline">01278777555</a>
              </div>
            </div>
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 bg-white/10 p-3 rounded-lg text-white">
                <i class="fas fa-map-marker-alt"></i>
              </div>
              <div>
                <h4 class="font-medium text-white">Location</h4>
                <a href="https://maps.google.com/?q=6th+October,Giza,Egypt" target="_blank"
                   class="text-indigo-100 hover:underline">
                  6th October, Giza
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- Availability + Social -->
        <div class="mt-12">
          <h3 class="text-xl font-semibold mb-6">Availability</h3>
          <p class="text-indigo-100 mb-4">
            I'm currently available for freelance projects and full-time positions. Feel free to reach out!
          </p>
          <div class="flex space-x-4">
            <a href="https://www.linkedin.com/in/kenzy-moataz/" target="_blank"
               class="bg-white/10 p-3 rounded-lg text-white hover:bg-white/20 transition">
              <i class="fab fa-linkedin text-xl"></i>
            </a>
            <a href="https://wa.me/201278777555" target="_blank"
               class="bg-white/10 p-3 rounded-lg text-white hover:bg-white/20 transition">
              <i class="fab fa-whatsapp text-xl"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
