<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>St. Xavier's English Medium School - Ambikapur</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Great+Vibes&family=Inter:wght@400;500;600&family=Manrope:wght@400;500;600;700&family=Outfit:wght@400;600;700;800&family=Playfair+Display:ital,wght@0,700;1,600&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
    /* =========================================
       1. GLOBAL VARIABLES
       ========================================= */
    :root {
        --xavier-navy: #002147;
        --xavier-gold: #d4af37;
        --xavier-gold-light: #ffdb58;
        --xavier-red: #c8102e;
        --xavier-teal: #037e73;
        --text-dark: #1e293b;
        --text-gray: #475569;
        --bg-color: #f8fafc;
        --white: #ffffff;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
        margin: 0;
        font-family: 'Outfit', sans-serif;
        background-color: var(--bg-color);
        min-height: 100vh;
        overflow-x: hidden;
        color: var(--text-dark);
    }

    a { text-decoration: none; }
    ul { list-style: none; }

    /* =========================================
       2. ALERT BAR
       ========================================= */
    .xavier-alert-bar {
        position: relative; width: 100%; height: 50px;
        background: linear-gradient(270deg, #001a38, #003366, #001a38);
        background-size: 200% 200%;
        animation: oceanFlow 10s ease infinite;
        display: flex; align-items: center;
        border-bottom: 3px solid var(--xavier-gold);
        z-index: 1000;
    }
    @keyframes oceanFlow { 0% {background-position:0% 50%} 50% {background-position:100% 50%} 100% {background-position:0% 50%} }

    .alert-badge {
        background: var(--xavier-gold); color: var(--xavier-navy); height: 100%;
        display: flex; align-items: center; padding: 0 20px;
        font-weight: 700; font-size: 13px; text-transform: uppercase;
        clip-path: polygon(0 0, 100% 0, 90% 100%, 0 100%); padding-right: 35px;
    }
    .live-dot { width: 8px; height: 8px; background: var(--xavier-red); border-radius: 50%; margin-right: 8px; animation: blink 1.5s infinite; }
    @keyframes blink { 0%, 100% {opacity:1} 50% {opacity:0.4} }

    .marquee-wrapper { flex: 1; overflow: hidden; height: 100%; display: flex; align-items: center; }
    .marquee-content { color: white; white-space: nowrap; animation: marquee 25s linear infinite; padding-left: 100%; }
    @keyframes marquee { 100% {transform: translateX(-100%);} }

    .action-btn-wrapper { background: rgba(0,33,71,0.9); height: 100%; display: flex; align-items: center; padding: 0 15px; }
    .apply-btn { border: 1px solid var(--xavier-gold); color: var(--xavier-gold); padding: 5px 15px; border-radius: 20px; font-size: 11px; font-weight: 700; text-transform: uppercase; transition: 0.3s; }
    .apply-btn:hover { background: var(--xavier-gold); color: var(--xavier-navy); }

    /* =========================================
       3. HERO HEADER
       ========================================= */
    .hero-container { padding: 40px 20px 20px; display: flex; justify-content: center; }
    .header-card {
        background: rgba(255,255,255,0.95); width: 100%; max-width: 1100px;
        border-radius: 20px; box-shadow: 0 20px 50px rgba(0,33,71,0.15);
        border: 1px solid white; overflow: hidden; animation: slideUp 0.8s ease-out;
    }
    .info-strip { background: var(--xavier-navy); color: var(--xavier-gold); padding: 8px 30px; display: flex; justify-content: space-between; font-size: 12px; font-weight: 700; text-transform: uppercase; }
    .header-content { padding: 40px; display: flex; align-items: center; gap: 40px; flex-wrap: wrap; justify-content: center; }
    .logo-wrapper { width: 130px; height: 130px; }
    .logo-wrapper img { width: 100%; height: 100%; object-fit: contain; }
    .text-content { text-align: center; flex: 1; min-width: 300px; }
    .hero-badge { display: inline-block; background: #fff8e1; color: var(--xavier-navy); font-size: 11px; font-weight: 700; padding: 5px 15px; border-radius: 20px; border: 1px solid var(--xavier-gold); margin-bottom: 10px; text-transform: uppercase; }
    h1 { font-family: 'Cinzel', serif; font-size: clamp(28px, 4vw, 42px); color: var(--xavier-navy); margin: 0 0 10px; line-height: 1.1; }
    .address { color: var(--xavier-red); font-weight: 700; margin-bottom: 15px; }
    .tagline { font-family: 'Great Vibes', cursive; font-size: 32px; color: var(--text-dark); }
    
    /* =========================================
       4. QUICK LINKS
       ========================================= */
    .card-row-container { display: flex; justify-content: center; gap: 20px; padding: 20px; flex-wrap: wrap; max-width: 1200px; margin: 0 auto; }
    .quick-card {
        flex: 1 1 200px; max-width: 250px; height: 280px; background: #fff;
        border-radius: 20px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.05);
        display: flex; flex-direction: column; transition: 0.3s; border: 1px solid #eee;
    }
    .quick-card:hover { transform: translateY(-10px); box-shadow: 0 20px 40px rgba(0,0,0,0.1); }
    .qc-img-box { height: 45%; }
    .qc-img-box img { width: 100%; height: 100%; object-fit: cover; }
    .qc-content { padding: 20px; flex: 1; display: flex; flex-direction: column; justify-content: space-between; }
    .qc-title { font-weight: 800; color: #111; font-size: 18px; }
    .qc-desc { font-size: 12px; color: #666; margin-top: 5px; }
    .qc-footer { display: flex; justify-content: space-between; align-items: center; margin-top: 10px; }
    .qc-action { font-size: 11px; font-weight: 700; color: var(--xavier-teal); text-transform: uppercase; }
    .qc-icon { width: 30px; height: 30px; background: #FFD000; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; }

    /* =========================================
       5. WELCOME SECTION (Fixed Image)
       ========================================= */
    .section-wrapper { padding: 60px 20px; }
    .container { max-width: 1100px; margin: 0 auto; }
    .welcome-wrapper {
        display: flex; gap: 50px; background: white; padding: 50px; border-radius: 24px;
        box-shadow: 0 20px 50px rgba(0,0,0,0.05); align-items: center; flex-wrap: wrap;
        border-top: 5px solid var(--xavier-navy);
    }
    .text-column { flex: 1; min-width: 300px; }
    .text-column h2 { font-family: 'Cinzel', serif; font-size: 40px; color: var(--xavier-navy); margin-bottom: 20px; }
    .description { font-size: 16px; color: var(--text-gray); line-height: 1.8; margin-bottom: 30px; text-align: justify; }
    .btn-learn { background: var(--xavier-navy); color: white; padding: 12px 30px; border-radius: 50px; font-weight: 700; display: inline-flex; align-items: center; gap: 10px; transition: 0.3s; }
    .btn-learn:hover { background: #001a38; transform: translateY(-3px); }
    
    .image-column { flex: 1; min-width: 300px; display: flex; justify-content: center; }
    .img-frame { 
        width: 100%; max-width: 450px; height: 350px; border-radius: 20px; 
        overflow: hidden; box-shadow: 15px 15px 0 var(--xavier-gold); 
        border: 2px solid white;
    }
    .img-frame img { width: 100%; height: 100%; object-fit: cover; }

    /* =========================================
       6. FACILITIES (Fixed Visibility)
       ========================================= */
    .bg-light { background: #f1f5f9; }
    .sec-header { text-align: center; margin-bottom: 50px; }
    .badge { background: var(--xavier-navy); color: var(--xavier-gold); padding: 5px 15px; border-radius: 50px; font-size: 12px; font-weight: 700; text-transform: uppercase; }
    .sec-title { font-family: 'Cinzel', serif; font-size: 36px; color: var(--xavier-navy); margin-top: 10px; }
    
    .facilities-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; }
    .facility-card { background: white; padding: 30px; border-radius: 20px; transition: 0.3s; box-shadow: 0 5px 15px rgba(0,0,0,0.03); }
    .facility-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.1); }
    .icon-sq { width: 50px; height: 50px; background: #e0e7ff; color: var(--xavier-navy); display: flex; align-items: center; justify-content: center; border-radius: 12px; margin-bottom: 20px; font-size: 24px; }
    .f-title { font-weight: 700; font-size: 18px; margin-bottom: 10px; color: var(--xavier-navy); }
    .f-desc { font-size: 14px; color: #666; line-height: 1.5; }

    /* Toggle Button */
    .more-facilities { display: none; } /* Hidden by default */
    .more-facilities.show { display: grid; } /* Shown via JS */
    .toggle-btn { margin-top: 40px; padding: 12px 30px; background: transparent; border: 2px solid var(--xavier-navy); color: var(--xavier-navy); border-radius: 50px; font-weight: 700; cursor: pointer; transition: 0.3s; }
    .toggle-btn:hover { background: var(--xavier-navy); color: white; }

    /* =========================================
       7. STATS (Why Choose Us)
       ========================================= */
    .stats-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 30px; }
    .stat-card { background: white; padding: 40px 20px; border-radius: 24px; text-align: center; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
    .stat-num { font-size: 48px; font-weight: 800; color: var(--xavier-navy); margin-bottom: 5px; }
    .stat-label { font-size: 14px; font-weight: 700; color: #666; text-transform: uppercase; }

    /* =========================================
       8. FOOTER (Fixed)
       ========================================= */
    .footer { background: white; border-top: 5px solid var(--xavier-teal); margin-top: 60px; }
    .map-box { height: 350px; position: relative; background: #ddd; }
    .map-box iframe { width: 100%; height: 100%; border: 0; filter: grayscale(100%); }
    .map-card { position: absolute; bottom: 20px; left: 50%; transform: translateX(-50%); background: white; padding: 20px; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.1); text-align: center; min-width: 280px; }
    
    .footer-content { max-width: 1200px; margin: 0 auto; padding: 50px 20px; display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; }
    .ft-col h3 { font-family: 'Playfair Display', serif; margin-bottom: 20px; color: var(--xavier-navy); }
    .ft-links li { margin-bottom: 10px; }
    .ft-links a { color: #555; font-size: 14px; transition: 0.2s; }
    .ft-links a:hover { color: var(--xavier-teal); padding-left: 5px; }
    .copyright { text-align: center; padding: 20px; border-top: 1px solid #eee; font-size: 13px; color: #888; }

    /* Mobile Tweaks */
    @media (max-width: 768px) {
        .header-content { flex-direction: column; text-align: center; }
        .welcome-wrapper { flex-direction: column-reverse; }
        .alert-badge span { display: none; }
        h1 { font-size: 28px; }
    }
    @keyframes slideUp { from {opacity:0; transform:translateY(30px)} to {opacity:1; transform:translateY(0)} }
</style>
</head>
<body>

<div class="xavier-alert-bar">
    <div class="alert-badge">
        <div class="live-dot"></div><span>Important</span>
    </div>
    <div class="marquee-wrapper">
        <div class="marquee-content">
            Registration Open for Academic Session 2026-27 • Entrance Exam Dates Announced • Contact: 07774-223117
        </div>
    </div>
    <div class="action-btn-wrapper">
        <a href="#" class="apply-btn">Apply Now</a>
    </div>
</div>

<div class="hero-container">
    <div class="header-card">
        <div class="info-strip">
            <span>Estd: 2013</span><span>UDISE: 22020110888</span>
        </div>
        <div class="header-content">
            <div class="logo-wrapper">
                <img src="https://i.ibb.co/x8g8QN5G/IMG-20251216-214627-347.webp" onerror="this.src='https://cdn-icons-png.flaticon.com/512/3203/3203383.png'" alt="SXS Logo">
            </div>
            <div class="text-content">
                <span class="hero-badge">Jesuit Education</span>
                <h1>St. Xavier’s English Medium School</h1>
                <div class="address">Ambikapur, Surguja (C.G.) - 497001</div>
                <div class="tagline">Education For A Hope Filled Future</div>
            </div>
        </div>
    </div>
</div>

<div class="card-row-container">
    <a href="https://sites.google.com/view/sxssurguja/appointment?authuser=0" class="quick-card">
        <div class="qc-img-box"><img src="https://images.unsplash.com/photo-1517486808906-6ca8b3f04846?auto=format&fit=crop&w=400&q=80"></div>
        <div class="qc-content">
            <div><div class="qc-title">Appointment</div><div class="qc-desc">Faculty consultation</div></div>
            <div class="qc-footer"><span class="qc-action">Book Now</span><div class="qc-icon"><i class="fa-solid fa-chevron-right"></i></div></div>
        </div>
    </a>
    <a href="https://sites.google.com/view/sxssurguja/rules/addmission-rule?authuser=0" class="quick-card">
        <div class="qc-img-box"><img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?auto=format&fit=crop&w=400&q=80"></div>
        <div class="qc-content">
            <div><div class="qc-title">Admission</div><div class="qc-desc">2026 Guidelines</div></div>
            <div class="qc-footer"><span class="qc-action">Details</span><div class="qc-icon"><i class="fa-solid fa-chevron-right"></i></div></div>
        </div>
    </a>
    <a href="https://sites.google.com/view/sxssurguja/online-registration?authuser=0" class="quick-card">
        <div class="qc-img-box"><img src="https://images.unsplash.com/photo-1587614382346-4ec70e388b28?auto=format&fit=crop&w=400&q=80"></div>
        <div class="qc-content">
            <div><div class="qc-title">Register</div><div class="qc-desc">Online Application</div></div>
            <div class="qc-footer"><span class="qc-action">Apply</span><div class="qc-icon"><i class="fa-solid fa-chevron-right"></i></div></div>
        </div>
    </a>
    <a href="https://play.google.com/store/apps/details?id=com.tvashtr.schoolcircle.android" class="quick-card">
        <div class="qc-img-box"><img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?auto=format&fit=crop&w=400&q=80"></div>
        <div class="qc-content">
            <div><div class="qc-title">Student App</div><div class="qc-desc">Live Updates</div></div>
            <div class="qc-footer"><span class="qc-action">Download</span><div class="qc-icon"><i class="fa-solid fa-chevron-right"></i></div></div>
        </div>
    </a>
</div>

<div class="section-wrapper">
    <div class="container">
        <div class="welcome-wrapper">
            <div class="text-column">
                <h2>Welcome to <br>St. Xavier's School</h2>
                <p class="description">
                    Founded with a vision to nurture young minds, we aim to create confident and ethical citizens. 
                    Our holistic approach ensures that every child finds the scope to grow and the stimuli to be the best version of themselves.
                </p>
                <a href="#" class="btn-learn">Learn More <i class="fa-solid fa-arrow-right"></i></a>
            </div>
            <div class="image-column">
                <div class="img-frame">
                    <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Students">
                </div>
            </div>
        </div>
    </div>
</div>

<div class="section-wrapper bg-light">
    <div class="container">
        <div class="sec-header">
            <span class="badge">Infrastructure</span>
            <h2 class="sec-title">World-Class Facilities</h2>
        </div>

        <div class="facilities-grid">
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-book-open"></i></div>
                <div class="f-title">Academic Excellence</div>
                <div class="f-desc">Comprehensive curriculum designed to foster critical thinking.</div>
            </div>
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-futbol"></i></div>
                <div class="f-title">Sports Complex</div>
                <div class="f-desc">Expansive grounds for cricket, football, and athletics.</div>
            </div>
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-flask"></i></div>
                <div class="f-title">Science Labs</div>
                <div class="f-desc">Fully equipped Physics, Chemistry, and Biology labs.</div>
            </div>
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-landmark"></i></div>
                <div class="f-title">Modern Library</div>
                <div class="f-desc">Housing over 10,000 books and digital resources.</div>
            </div>
        </div>

        <div class="facilities-grid more-facilities" id="moreFacilities" style="margin-top:30px;">
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-bus"></i></div>
                <div class="f-title">Safe Transport</div>
                <div class="f-desc">GPS-enabled bus fleet covering all major routes.</div>
            </div>
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-chalkboard-user"></i></div>
                <div class="f-title">Smart Classrooms</div>
                <div class="f-desc">Digital interactive boards for visual learning.</div>
            </div>
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-bed"></i></div>
                <div class="f-title">Boarding House</div>
                <div class="f-desc">Secure, hygienic, and caring hostel facilities.</div>
            </div>
            <div class="facility-card">
                <div class="icon-sq"><i class="fa-solid fa-shield-halved"></i></div>
                <div class="f-title">24x7 Security</div>
                <div class="f-desc">CCTV surveillance and trained security personnel.</div>
            </div>
        </div>

        <div style="text-align:center;">
            <button class="toggle-btn" onclick="toggleFacilities()">View All Facilities</button>
        </div>
    </div>
</div>

<div class="section-wrapper">
    <div class="container">
        <div class="sec-header">
            <span class="badge">At A Glance</span>
            <h2 class="sec-title">Why Choose SXS?</h2>
        </div>
        <div class="stats-grid" id="statsSection">
            <div class="stat-card">
                <div class="stat-num" data-target="8">0+</div>
                <div class="stat-label">Acres Campus</div>
            </div>
            <div class="stat-card">
                <div class="stat-num" data-target="45">0+</div>
                <div class="stat-label">Years History</div>
            </div>
            <div class="stat-card">
                <div class="stat-num" data-target="200">0+</div>
                <div class="stat-label">Expert Faculty</div>
            </div>
            <div class="stat-card">
                <div class="stat-num" data-target="2000">0+</div>
                <div class="stat-label">Happy Studen
