<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meet Jain - Contact Links</title>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
      font-family: 'Orbitron', monospace;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes neonPulse {
      0%, 100% { 
        text-shadow: 0 0 20px rgba(0, 255, 255, 1),
                     0 0 40px rgba(0, 255, 255, 0.8),
                     0 0 60px rgba(0, 255, 255, 0.6),
                     0 0 80px rgba(0, 255, 255, 0.4),
                     0 0 100px rgba(0, 255, 255, 0.2);
      }
      50% { 
        text-shadow: 0 0 30px rgba(0, 255, 255, 1),
                     0 0 60px rgba(0, 255, 255, 1),
                     0 0 90px rgba(0, 255, 255, 0.8),
                     0 0 120px rgba(0, 255, 255, 0.6),
                     0 0 150px rgba(0, 255, 255, 0.4);
      }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      25% { transform: translateY(-15px) rotate(2deg); }
      75% { transform: translateY(-10px) rotate(-2deg); }
    }

    @keyframes glowRing {
      0%, 100% { 
        box-shadow: 0 0 20px rgba(0, 255, 255, 0.5),
                    0 0 40px rgba(255, 0, 255, 0.3),
                    inset 0 0 20px rgba(0, 255, 255, 0.2);
      }
      50% { 
        box-shadow: 0 0 40px rgba(0, 255, 255, 0.8),
                    0 0 60px rgba(255, 0, 255, 0.6),
                    inset 0 0 30px rgba(0, 255, 255, 0.4);
      }
    }

    @keyframes slideInUp {
      from {
        opacity: 0;
        transform: translateY(40px) scale(0.9);
      }
      to {
        opacity: 1;
        transform: translateY(0) scale(1);
      }
    }

    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.3; }
    }

    @keyframes shimmer {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }

    .gradient-bg {
      background: linear-gradient(135deg, #0a0a0a 0%, #1a0a2e 25%, #16213e 50%, #0f3460 75%, #0a0a0a 100%);
      background-size: 400% 400%;
      animation: gradientShift 15s ease infinite;
    }

    .neon-text {
      animation: neonPulse 2s ease-in-out infinite;
    }

    .profile-container {
      animation: float 6s ease-in-out infinite;
    }

    .avatar-container {
      animation: glowRing 3s ease-in-out infinite;
    }

    .slide-in {
      animation: slideInUp 0.8s cubic-bezier(0.34, 1.56, 0.64, 1) forwards;
    }

    .link-button {
      position: relative;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
    }

    .link-button::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
      transition: left 0.6s;
    }

    .link-button:hover::before {
      left: 100%;
    }

    .link-button:hover {
      transform: translateY(-8px) scale(1.05);
      box-shadow: 0 10px 40px rgba(0, 255, 255, 0.6),
                  0 0 30px rgba(255, 0, 255, 0.5),
                  0 0 60px rgba(0, 255, 255, 0.4),
                  0 0 80px rgba(255, 0, 255, 0.3);
    }

    .link-button:active {
      transform: translateY(-4px) scale(1.02);
    }

    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }

    .particle {
      position: absolute;
      width: 4px;
      height: 4px;
      background: rgba(0, 255, 255, 0.6);
      border-radius: 50%;
      animation: float 6s ease-in-out infinite;
      box-shadow: 0 0 10px rgba(0, 255, 255, 0.8);
    }

    @keyframes eyeBlink {
      0%, 96%, 100% { transform: scaleY(1); }
      98% { transform: scaleY(0.1); }
    }

    .blink-eye {
      animation: eyeBlink 4s ease-in-out infinite;
      transform-origin: center;
    }

    .neon-border {
      border: 3px solid rgba(0, 255, 255, 0.6);
      box-shadow: 0 0 15px rgba(0, 255, 255, 0.6),
                  0 0 30px rgba(255, 0, 255, 0.4),
                  inset 0 0 15px rgba(0, 255, 255, 0.3);
    }

    @keyframes wave {
      0% { transform: rotate(0deg); }
      10% { transform: rotate(14deg); }
      20% { transform: rotate(-8deg); }
      30% { transform: rotate(14deg); }
      40% { transform: rotate(-4deg); }
      50% { transform: rotate(10deg); }
      60% { transform: rotate(0deg); }
      100% { transform: rotate(0deg); }
    }

    .wave-hand {
      animation: wave 2.5s ease-in-out infinite;
      transform-origin: 70% 70%;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }

    .bounce-shoes {
      animation: bounce 1s ease-in-out infinite;
    }

    @keyframes colorShift {
      0%, 100% { filter: hue-rotate(0deg); }
      50% { filter: hue-rotate(30deg); }
    }

    .color-shift {
      animation: colorShift 4s ease-in-out infinite;
    }

    @keyframes borderGlow {
      0%, 100% { 
        border-color: rgba(0, 255, 255, 0.6);
        box-shadow: 0 0 15px rgba(0, 255, 255, 0.6),
                    0 0 30px rgba(255, 0, 255, 0.4),
                    inset 0 0 15px rgba(0, 255, 255, 0.3);
      }
      50% { 
        border-color: rgba(255, 0, 255, 0.8);
        box-shadow: 0 0 25px rgba(255, 0, 255, 0.8),
                    0 0 50px rgba(0, 255, 255, 0.6),
                    inset 0 0 25px rgba(255, 0, 255, 0.4);
      }
    }

    .neon-border {
      animation: borderGlow 3s ease-in-out infinite;
    }

    @keyframes particleFloat {
      0% { 
        transform: translateY(100%) scale(0);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% { 
        transform: translateY(-100%) scale(1);
        opacity: 0;
      }
    }

    .particle-float {
      animation: particleFloat 8s ease-in-out infinite;
    }

    @keyframes rotateHue {
      0% { filter: hue-rotate(0deg) brightness(1); }
      50% { filter: hue-rotate(20deg) brightness(1.2); }
      100% { filter: hue-rotate(0deg) brightness(1); }
    }

    .button-glow {
      animation: rotateHue 3s ease-in-out infinite;
    }

    /* Tech Grid Background */
    .tech-grid {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      background-image: 
        linear-gradient(rgba(0, 255, 255, 0.1) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0, 255, 255, 0.1) 1px, transparent 1px),
        linear-gradient(rgba(255, 0, 255, 0.05) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255, 0, 255, 0.05) 1px, transparent 1px);
      background-size: 100px 100px, 100px 100px, 20px 20px, 20px 20px;
      background-position: -1px -1px, -1px -1px, -1px -1px, -1px -1px;
      animation: gridScroll 20s linear infinite;
    }

    @keyframes gridScroll {
      0% {
        background-position: 0 0, 0 0, 0 0, 0 0;
      }
      100% {
        background-position: 100px 100px, 100px 100px, 20px 20px, 20px 20px;
      }
    }

    /* Animated lines */
    .tech-grid::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: 
        repeating-linear-gradient(
          0deg,
          transparent,
          transparent 2px,
          rgba(0, 255, 255, 0.03) 2px,
          rgba(0, 255, 255, 0.03) 4px
        );
      animation: scanlines 8s linear infinite;
    }

    @keyframes scanlines {
      0% {
        transform: translateY(0);
      }
      100% {
        transform: translateY(50px);
      }
    }

    /* Glowing corner accents */
    .tech-grid::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(circle at 10% 20%, rgba(0, 255, 255, 0.15) 0%, transparent 50%),
        radial-gradient(circle at 90% 80%, rgba(255, 0, 255, 0.15) 0%, transparent 50%),
        radial-gradient(circle at 50% 50%, rgba(0, 255, 255, 0.05) 0%, transparent 70%);
      animation: glowPulse 6s ease-in-out infinite;
    }

    @keyframes glowPulse {
      0%, 100% {
        opacity: 0.5;
      }
      50% {
        opacity: 1;
      }
    }

    /* Circuit Board Pattern */
    .circuit-pattern {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      pointer-events: none;
      opacity: 0.3;
    }

    /* Hexagon Pattern */
    .hexagon-pattern {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      pointer-events: none;
      opacity: 0.15;
    }

    .hexagon {
      position: absolute;
      width: 60px;
      height: 35px;
      background: rgba(0, 255, 255, 0.1);
      margin: 17.5px 0;
      border-left: 1px solid rgba(0, 255, 255, 0.3);
      border-right: 1px solid rgba(0, 255, 255, 0.3);
      animation: hexPulse 8s ease-in-out infinite;
    }

    .hexagon::before,
    .hexagon::after {
      content: "";
      position: absolute;
      width: 0;
      border-left: 30px solid transparent;
      border-right: 30px solid transparent;
      left: 0;
    }

    .hexagon::before {
      bottom: 100%;
      border-bottom: 17.5px solid rgba(0, 255, 255, 0.1);
      border-top: 1px solid rgba(0, 255, 255, 0.3);
    }

    .hexagon::after {
      top: 100%;
      border-top: 17.5px solid rgba(0, 255, 255, 0.1);
      border-bottom: 1px solid rgba(0, 255, 255, 0.3);
    }

    @keyframes hexPulse {
      0%, 100% {
        opacity: 0.3;
      }
      50% {
        opacity: 0.8;
      }
    }

    /* Data Stream Lines */
    .data-stream {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      pointer-events: none;
      overflow: hidden;
    }

    .stream-line {
      position: absolute;
      width: 2px;
      height: 100px;
      background: linear-gradient(to bottom, transparent, rgba(0, 255, 255, 0.8), transparent);
      animation: streamFlow 3s linear infinite;
    }

    @keyframes streamFlow {
      0% {
        transform: translateY(-100%);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% {
        transform: translateY(calc(100vh + 100px));
        opacity: 0;
      }
    }

    .stream-line-horizontal {
      position: absolute;
      width: 100px;
      height: 2px;
      background: linear-gradient(to right, transparent, rgba(255, 0, 255, 0.8), transparent);
      animation: streamFlowH 4s linear infinite;
    }

    @keyframes streamFlowH {
      0% {
        transform: translateX(-100%);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% {
        transform: translateX(calc(100vw + 100px));
        opacity: 0;
      }
    }

    /* Tech Icons Container */
    .tech-icons {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      pointer-events: none;
      overflow: hidden;
    }

    .tech-icon {
      position: absolute;
      opacity: 0.15;
      animation: floatTech 20s ease-in-out infinite;
    }

    @keyframes floatTech {
      0%, 100% {
        transform: translateY(0) translateX(0) rotate(0deg);
      }
      25% {
        transform: translateY(-30px) translateX(20px) rotate(5deg);
      }
      50% {
        transform: translateY(-15px) translateX(-20px) rotate(-5deg);
      }
      75% {
        transform: translateY(-40px) translateX(10px) rotate(3deg);
      }
    }

    @keyframes rotateTech {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    .rotate-slow {
      animation: rotateTech 30s linear infinite;
    }

    @keyframes pulseTech {
      0%, 100% {
        opacity: 0.1;
        transform: scale(1);
      }
      50% {
        opacity: 0.25;
        transform: scale(1.1);
      }
    }

    .pulse-tech {
      animation: pulseTech 4s ease-in-out infinite;
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full"><!-- Tech Grid Background -->
  <div class="tech-grid"></div><!-- Circuit Pattern -->
  <div class="circuit-pattern" id="circuit-pattern"></div><!-- Hexagon Pattern -->
  <div class="hexagon-pattern" id="hexagon-pattern"></div><!-- Data Stream -->
  <div class="data-stream" id="data-stream"></div><!-- Tech Icons Background -->
  <div class="tech-icons" id="tech-icons"></div><!-- Floating Particles Background -->
  <div class="particles" id="particles"></div>
  <div id="app" class="w-full h-full overflow-auto gradient-bg relative z-10">
   <div class="min-h-full flex items-center justify-center px-4 py-12">
    <div class="w-full max-w-md"><!-- Profile Section -->
     <div class="profile-container text-center mb-8 slide-in">
      <h1 id="name" class="text-5xl font-bold text-cyan-400 mb-3 neon-text" style="font-weight: 900;">KAI</h1>
      <p id="tagline" class="text-xl text-purple-300" style="text-shadow: 0 0 15px rgba(255, 0, 255, 0.8), 0 0 30px rgba(255, 0, 255, 0.5);">Connect with me! 🚀</p>
     </div><!-- Links Section -->
     <div class="space-y-4" id="links-container"><!-- Instagram --> <a href="https://www.instagram.com/kannu_2497?igsh=MXZneWtiM3Rkd216Nw==" target="_blank" rel="noopener noreferrer" class="link-button button-glow slide-in w-full flex items-center justify-center gap-3 px-6 py-4 rounded-2xl text-white font-bold text-lg" style="animation-delay: 0.1s; background: linear-gradient(135deg, #833ab4 0%, #fd1d1d 50%, #fcb045 100%);">
       <svg class="w-6 h-6" fill="currentColor" viewbox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
       </svg><span id="instagram_label">Instagram</span> </a> <!-- LinkedIn --> <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" class="link-button button-glow slide-in w-full flex items-center justify-center gap-3 px-6 py-4 rounded-2xl text-white font-bold text-lg" style="animation-delay: 0.2s; background: linear-gradient(135deg, #0077b5 0%, #00a0dc 100%);">
       <svg class="w-6 h-6" fill="currentColor" viewbox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" />
       </svg><span id="linkedin_label">LinkedIn</span> </a> <!-- Twitter --> <a href="https://twitter.com" target="_blank" rel="noopener noreferrer" class="link-button button-glow slide-in w-full flex items-center justify-center gap-3 px-6 py-4 rounded-2xl text-white font-bold text-lg" style="animation-delay: 0.3s; background: linear-gradient(135deg, #1da1f2 0%, #0d8bd9 100%);">
       <svg class="w-6 h-6" fill="currentColor" viewbox="0 0 24 24"><path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
       </svg><span id="twitter_label">Twitter</span> </a> <!-- Email --> <a href="mailto:mjjain231@gmail.com" target="_blank" rel="noopener noreferrer" class="link-button button-glow slide-in w-full flex items-center justify-center gap-3 px-6 py-4 rounded-2xl text-white font-bold text-lg" style="animation-delay: 0.4s; background: linear-gradient(135deg, #ea4335 0%, #ff6b6b 100%);">
       <svg class="w-6 h-6" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
       </svg><span id="email_label">Email Me</span> </a>
     </div>
     <p class="text-center text-cyan-300 mt-8 slide-in font-semibold" style="animation-delay: 0.5s; text-shadow: 0 0 10px rgba(0, 255, 255, 0.5);">⚡ Let's create something amazing! ⚡</p>
    </div>
   </div>
  </div>
  <script>
    // Create circuit board pattern with SVG
    const circuitContainer = document.getElementById('circuit-pattern');
    const circuitSVG = `
      <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <pattern id="circuit" x="0" y="0" width="200" height="200" patternUnits="userSpaceOnUse">
            <!-- Horizontal lines -->
            <line x1="0" y1="50" x2="100" y2="50" stroke="rgba(0, 255, 255, 0.3)" stroke-width="2"/>
            <line x1="100" y1="100" x2="200" y2="100" stroke="rgba(255, 0, 255, 0.3)" stroke-width="2"/>
            <line x1="50" y1="150" x2="150" y2="150" stroke="rgba(0, 255, 255, 0.3)" stroke-width="2"/>
            
            <!-- Vertical lines -->
            <line x1="50" y1="0" x2="50" y2="100" stroke="rgba(0, 255, 255, 0.3)" stroke-width="2"/>
            <line x1="150" y1="50" x2="150" y2="200" stroke="rgba(255, 0, 255, 0.3)" stroke-width="2"/>
            <line x1="100" y1="100" x2="100" y2="150" stroke="rgba(0, 255, 255, 0.3)" stroke-width="2"/>
            
            <!-- Connection points -->
            <circle cx="50" cy="50" r="4" fill="rgba(0, 255, 255, 0.6)"/>
            <circle cx="100" cy="100" r="4" fill="rgba(255, 0, 255, 0.6)"/>
            <circle cx="150" cy="150" r="4" fill="rgba(0, 255, 255, 0.6)"/>
            <circle cx="100" cy="50" r="3" fill="rgba(255, 0, 255, 0.5)"/>
            <circle cx="150" cy="100" r="3" fill="rgba(0, 255, 255, 0.5)"/>
            
            <!-- Small chips -->
            <rect x="95" y="95" width="10" height="10" fill="none" stroke="rgba(0, 255, 255, 0.4)" stroke-width="1"/>
            <rect x="145" y="145" width="10" height="10" fill="none" stroke="rgba(255, 0, 255, 0.4)" stroke-width="1"/>
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#circuit)"/>
      </svg>
    `;
    circuitContainer.innerHTML = circuitSVG;

    // Create hexagon pattern
    const hexagonContainer = document.getElementById('hexagon-pattern');
    for (let row = 0; row < 8; row++) {
      for (let col = 0; col < 15; col++) {
        const hex = document.createElement('div');
        hex.className = 'hexagon';
        const offsetX = col * 90 + (row % 2) * 45;
        const offsetY = row * 52;
        hex.style.left = offsetX + 'px';
        hex.style.top = offsetY + 'px';
        hex.style.animationDelay = (Math.random() * 8) + 's';
        
        if (Math.random() > 0.5) {
          hex.style.background = 'rgba(255, 0, 255, 0.1)';
          hex.style.borderColor = 'rgba(255, 0, 255, 0.3)';
        }
        
        hexagonContainer.appendChild(hex);
      }
    }

    // Create data stream lines
    const dataStreamContainer = document.getElementById('data-stream');
    
    // Vertical streams
    for (let i = 0; i < 8; i++) {
      const stream = document.createElement('div');
      stream.className = 'stream-line';
      stream.style.left = (10 + i * 12) + '%';
      stream.style.animationDelay = (i * 0.4) + 's';
      stream.style.animationDuration = (2 + Math.random() * 2) + 's';
      dataStreamContainer.appendChild(stream);
    }
    
    // Horizontal streams
    for (let i = 0; i < 5; i++) {
      const stream = document.createElement('div');
      stream.className = 'stream-line-horizontal';
      stream.style.top = (15 + i * 18) + '%';
      stream.style.animationDelay = (i * 0.6) + 's';
      stream.style.animationDuration = (3 + Math.random() * 2) + 's';
      dataStreamContainer.appendChild(stream);
    }

    // Create floating particles with better animation
    const particlesContainer = document.getElementById('particles');
    for (let i = 0; i < 50; i++) {
      const particle = document.createElement('div');
      particle.className = 'particle';
      particle.style.left = Math.random() * 100 + '%';
      particle.style.top = Math.random() * 100 + '%';
      particle.style.animationDelay = Math.random() * 8 + 's';
      particle.style.animationDuration = (Math.random() * 6 + 6) + 's';
      
      // Vary particle sizes
      const size = Math.random() * 3 + 2;
      particle.style.width = size + 'px';
      particle.style.height = size + 'px';
      
      // Random colors between cyan and magenta
      const isBlue = Math.random() > 0.5;
      if (isBlue) {
        particle.style.background = 'rgba(0, 255, 255, 0.8)';
        particle.style.boxShadow = '0 0 15px rgba(0, 255, 255, 1), 0 0 30px rgba(0, 255, 255, 0.6)';
      } else {
        particle.style.background = 'rgba(255, 0, 255, 0.8)';
        particle.style.boxShadow = '0 0 15px rgba(255, 0, 255, 1), 0 0 30px rgba(255, 0, 255, 0.6)';
      }
      
      particlesContainer.appendChild(particle);
    }

    // Create tech icons in background
    const techIconsContainer = document.getElementById('tech-icons');
    const techIcons = [
      // CPU/Chip
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="9" y="9" width="6" height="6" rx="1"/><path d="M8 9H4M20 9h-4M8 15H4M20 15h-4M9 8V4M9 20v-4M15 8V4M15 20v-4"/></svg>',
      // Code brackets
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M16 18l6-6-6-6M8 6l-6 6 6 6"/></svg>',
      // Terminal
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M7 8l4 4-4 4M13 16h4"/></svg>',
      // Circuit
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="6" cy="12" r="2"/><circle cx="18" cy="12" r="2"/><path d="M8 12h8M12 8v8"/></svg>',
      // Database
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5M3 12c0 1.66 4 3 9 3s9-1.34 9-3"/></svg>',
      // Network
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="2"/><circle cx="19" cy="5" r="2"/><circle cx="5" cy="5" r="2"/><circle cx="19" cy="19" r="2"/><circle cx="5" cy="19" r="2"/><path d="M12 14v-4m0 0L7 7m5 3l5-3m-5 3v0m0 8l-5 3m5-3l5 3"/></svg>',
      // Settings gear
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="3"/><path d="M12 1v3m0 16v3M4.22 4.22l2.12 2.12m11.32 11.32l2.12 2.12M1 12h3m16 0h3M4.22 19.78l2.12-2.12m11.32-11.32l2.12-2.12"/></svg>',
      // Wifi signal
      '<svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M5 12.55a11 11 0 0114 0M8.5 16.5a6 6 0 017 0"/><circle cx="12" cy="20" r="1" fill="currentColor"/></svg>'
    ];

    const positions = [
      { top: '10%', left: '5%' },
      { top: '15%', right: '8%' },
      { top: '40%', left: '3%' },
      { top: '60%', right: '5%' },
      { top: '75%', left: '10%' },
      { top: '80%', right: '12%' },
      { top: '30%', right: '15%' },
      { top: '50%', left: '8%' }
    ];

    techIcons.forEach((icon, index) => {
      const iconDiv = document.createElement('div');
      iconDiv.className = 'tech-icon';
      iconDiv.innerHTML = icon;
      
      const pos = positions[index];
      Object.keys(pos).forEach(key => {
        iconDiv.style[key] = pos[key];
      });
      
      iconDiv.style.color = Math.random() > 0.5 ? 'rgba(0, 255, 255, 0.2)' : 'rgba(255, 0, 255, 0.2)';
      iconDiv.style.animationDelay = (Math.random() * 5) + 's';
      iconDiv.style.animationDuration = (15 + Math.random() * 10) + 's';
      
      // Random animation type
      if (Math.random() > 0.5) {
        iconDiv.classList.add('rotate-slow');
      } else {
        iconDiv.classList.add('pulse-tech');
      }
      
      techIconsContainer.appendChild(iconDiv);
    });

    const defaultConfig = {
      name: "KAI",
      tagline: "Connect with me! 🚀",
      instagram_label: "Instagram",
      linkedin_label: "LinkedIn",
      twitter_label: "Twitter",
      email_label: "Email Me",
      background_start: "#0a0a0a",
      background_end: "#0f3460",
      text_color: "#00ffff",
      font_family: "Orbitron",
      font_size: 16
    };

    async function onConfigChange(config) {
      const baseSize = config.font_size || defaultConfig.font_size;
      const customFont = config.font_family || defaultConfig.font_family;
      const baseFontStack = 'monospace';

      // Update text content
      document.getElementById('name').textContent = config.name || defaultConfig.name;
      document.getElementById('tagline').textContent = config.tagline || defaultConfig.tagline;
      document.getElementById('instagram_label').textContent = config.instagram_label || defaultConfig.instagram_label;
      document.getElementById('linkedin_label').textContent = config.linkedin_label || defaultConfig.linkedin_label;
      document.getElementById('twitter_label').textContent = config.twitter_label || defaultConfig.twitter_label;
      document.getElementById('email_label').textContent = config.email_label || defaultConfig.email_label;

      // Apply colors
      const bgStart = config.background_start || defaultConfig.background_start;
      const bgEnd = config.background_end || defaultConfig.background_end;
      const textColor = config.text_color || defaultConfig.text_color;
      
      document.getElementById('app').style.background = `linear-gradient(135deg, ${bgStart} 0%, ${bgEnd} 100%)`;
      document.getElementById('name').style.color = textColor;

      // Apply font
      document.getElementById('name').style.fontFamily = `${customFont}, ${baseFontStack}`;
      document.getElementById('tagline').style.fontFamily = `${customFont}, ${baseFontStack}`;
      
      const labels = [
        document.getElementById('instagram_label'),
        document.getElementById('linkedin_label'),
        document.getElementById('twitter_label'),
        document.getElementById('email_label')
      ];
      
      labels.forEach(label => {
        label.style.fontFamily = `${customFont}, ${baseFontStack}`;
      });

      // Apply font sizes
      document.getElementById('name').style.fontSize = `${baseSize * 3.125}px`;
      document.getElementById('tagline').style.fontSize = `${baseSize * 1.25}px`;
      
      labels.forEach(label => {
        label.style.fontSize = `${baseSize * 1.125}px`;
      });
    }

    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities: (config) => ({
          recolorables: [
            {
              get: () => config.background_start || defaultConfig.background_start,
              set: (value) => {
                config.background_start = value;
                window.elementSdk.setConfig({ background_start: value });
              }
            },
            {
              get: () => config.background_end || defaultConfig.background_end,
              set: (value) => {
                config.background_end = value;
                window.elementSdk.setConfig({ background_end: value });
              }
            },
            {
              get: () => config.text_color || defaultConfig.text_color,
              set: (value) => {
                config.text_color = value;
                window.elementSdk.setConfig({ text_color: value });
              }
            }
          ],
          borderables: [],
          fontEditable: {
            get: () => config.font_family || defaultConfig.font_family,
            set: (value) => {
              config.font_family = value;
              window.elementSdk.setConfig({ font_family: value });
            }
          },
          fontSizeable: {
            get: () => config.font_size || defaultConfig.font_size,
            set: (value) => {
              config.font_size = value;
              window.elementSdk.setConfig({ font_size: value });
            }
          }
        }),
        mapToEditPanelValues: (config) => new Map([
          ["name", config.name || defaultConfig.name],
          ["tagline", config.tagline || defaultConfig.tagline],
          ["instagram_label", config.instagram_label || defaultConfig.instagram_label],
          ["linkedin_label", config.linkedin_label || defaultConfig.linkedin_label],
          ["twitter_label", config.twitter_label || defaultConfig.twitter_label],
          ["email_label", config.email_label || defaultConfig.email_label]
        ])
      });
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9bac5be8511379e0',t:'MTc2Nzg4MjI3Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
