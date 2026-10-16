<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scale=no">
    <title>For You — A Friendship Story</title>
    <meta name="description" content="A personal digital experience, made for someone who matters.">
    <meta property="og:title" content="I Made Something For You">
    <meta property="og:description" content="A personal digital experience. Open it.">
    <meta property="og:type" content="website">
    <meta name="theme-color" content="#0B0D12">

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

    <style>
        /* ============================================================
           CONFIGURATION — Edit these CSS custom properties to 
           quickly change colors, fonts, and spacing.
           ============================================================ */
        :root {
            --bg-primary: #0B0D12;
            --bg-secondary: #151922;
            --bg-tertiary: #1a1f2b;
            --text-primary: #F5F1E8;
            --text-secondary: #A5A9B3;
            --accent: #C8A96B;
            --accent-dim: rgba(200, 169, 107, 0.15);
            --accent-glow: rgba(200, 169, 107, 0.08);
            --font-serif: 'Cormorant Garamond', 'Georgia', serif;
            --font-sans: 'Inter', -apple-system, 'Segoe UI', sans-serif;
            --transition-smooth: cubic-bezier(0.25, 0.46, 0.45, 0.94);
            --transition-elegant: cubic-bezier(0.19, 1, 0.22, 1);
            --grain-opacity: 0.03;
        }

        @media (prefers-reduced-motion: reduce) {
            *, *::before, *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }

        /* ============================================================
           RESET & BASE
           ============================================================ */
        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            -webkit-text-size-adjust: 100%;
            font-size: 16px;
        }

        body {
            font-family: var(--font-sans);
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* Film grain overlay */
        body::after {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 10000;
            opacity: var(--grain-opacity);
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='1'/%3E%3C/svg%3E");
        }

        img {
            max-width: 100%;
            display: block;
        }

        a {
            color: var(--accent);
            text-decoration: none;
        }

        button {
            font-family: var(--font-sans);
            cursor: pointer;
            border: none;
            background: none;
            color: inherit;
        }

        button:focus-visible,
        a:focus-visible {
            outline: 2px solid var(--accent);
            outline-offset: 4px;
            border-radius: 2px;
        }

        ::selection {
            background: var(--accent);
            color: var(--bg-primary);
        }

        /* ============================================================
           SCROLLBAR
           ============================================================ */
        ::-webkit-scrollbar {
            width: 4px;
        }
        ::-webkit-scrollbar-track {
            background: var(--bg-primary);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--bg-tertiary);
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: var(--accent);
        }

        /* ============================================================
           TYPOGRAPHY
           ============================================================ */
        .heading-serif {
            font-family: var(--font-serif);
            font-weight: 300;
            letter-spacing: 0.02em;
            line-height: 1.2;
        }

        .chapter-label {
            font-family: var(--font-sans);
            font-size: 0.7rem;
            font-weight: 500;
            letter-spacing: 0.25em;
            text-transform: uppercase;
            color: var(--accent);
            margin-bottom: 1rem;
            display: block;
        }

        .body-text {
            font-family: var(--font-sans);
            font-weight: 300;
            font-size: 1rem;
            line-height: 1.85;
            color: var(--text-secondary);
            max-width: 560px;
        }

        /* ============================================================
           SHARED LAYOUT COMPONENTS
           ============================================================ */
        .section-container {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 6rem 1.5rem;
            position: relative;
        }

        .section-inner {
            max-width: 720px;
            width: 100%;
            margin: 0 auto;
        }

        .section-divider {
            width: 40px;
            height: 1px;
            background: var(--accent);
            margin: 2rem 0;
            opacity: 0.4;
        }

        /* Primary CTA button */
        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 1rem 2.5rem;
            border: 1px solid var(--accent);
            color: var(--accent);
            font-family: var(--font-sans);
            font-size: 0.85rem;
            font-weight: 400;
            letter-spacing: 0.15em;
            text-transform: uppercase;
            background: transparent;
            transition: all 0.5s var(--transition-smooth);
            position: relative;
            overflow: hidden;
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: var(--accent);
            transition: left 0.5s var(--transition-elegant);
            z-index: 0;
        }

        .btn-primary:hover::before {
            left: 0;
        }

        .btn-primary:hover {
            color: var(--bg-primary);
        }

        .btn-primary span {
            position: relative;
            z-index: 1;
        }

        .btn-primary .arrow {
            position: relative;
            z-index: 1;
            transition: transform 0.3s var(--transition-smooth);
        }

        .btn-primary:hover .arrow {
            transform: translateX(4px);
        }

        /* Secondary / ghost button */
        .btn-ghost {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.75rem 1.5rem;
            color: var(--text-secondary);
            font-size: 0.8rem;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            transition: color 0.3s;
        }

        .btn-ghost:hover {
            color: var(--accent);
        }

        /* ============================================================
           SCROLL-TRIGGERED REVEALS
           ============================================================ */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s var(--transition-smooth),
                        transform 0.8s var(--transition-elegant);
        }

        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .reveal-delay-1 { transition-delay: 0.15s; }
        .reveal-delay-2 { transition-delay: 0.3s; }
        .reveal-delay-3 { transition-delay: 0.45s; }
        .reveal-delay-4 { transition-delay: 0.6s; }
        .reveal-delay-5 { transition-delay: 0.75s; }

        /* ============================================================
           PROGRESS INDICATOR
           ============================================================ */
        .progress-bar {
            position: fixed;
            top: 0;
            left: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--accent), rgba(200, 169, 107, 0.3));
            z-index: 9999;
            transition: width 0.1s linear;
            width: 0%;
        }

        /* Chapter nav dots */
        .chapter-nav {
            position: fixed;
            right: 1.25rem;
            top: 50%;
            transform: translateY(-50%);
            z-index: 9998;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            opacity: 0;
            transition: opacity 0.5s;
        }

        .chapter-nav.visible {
            opacity: 1;
        }

        .chapter-nav-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            border: 1px solid var(--text-secondary);
            background: transparent;
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
        }

        .chapter-nav-dot.active {
            background: var(--accent);
            border-color: var(--accent);
            transform: scale(1.2);
        }

        .chapter-nav-dot::after {
            content: attr(data-label);
            position: absolute;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 0.65rem;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            color: var(--text-secondary);
            white-space: nowrap;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s;
        }

        .chapter-nav-dot:hover::after {
            opacity: 1;
        }

        @media (max-width: 768px) {
            .chapter-nav {
                right: 0.75rem;
                gap: 0.75rem;
            }
            .chapter-nav-dot {
                width: 6px;
                height: 6px;
            }
            .chapter-nav-dot::after {
                display: none;
            }
        }

        /* ============================================================
           OPENING EXPERIENCE (#intro)
           ============================================================ */
        #intro {
            position: fixed;
            inset: 0;
            z-index: 10001;
            background: var(--bg-primary);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 2rem;
            transition: opacity 1s var(--transition-smooth),
                        visibility 0s linear 0s;
        }

        #intro.hidden {
            opacity: 0;
            visibility: hidden;
            transition: opacity 1s var(--transition-smooth),
                        visibility 0s linear 1s;
        }

        #intro .glow-orb {
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: radial-gradient(circle, var(--accent-glow) 0%, transparent 70%);
            animation: pulse-glow 4s ease-in-out infinite;
            pointer-events: none;
        }

        @keyframes pulse-glow {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.15); opacity: 1; }
        }

        .intro-line {
            font-family: var(--font-serif);
            font-weight: 300;
            font-size: clamp(1.3rem, 4vw, 2rem);
            color: var(--text-primary);
            opacity: 0;
            transform: translateY(15px);
            transition: opacity 1.2s, transform 1.2s var(--transition-elegant);
            margin-bottom: 0.75rem;
            line-height: 1.4;
        }

        .intro-line.show {
            opacity: 1;
            transform: translateY(0);
        }

        .intro-line.fade-out {
            opacity: 0;
            transform: translateY(-10px);
        }

        .intro-line.sub {
            font-family: var(--font-sans);
            font-size: clamp(0.85rem, 2.5vw, 1rem);
            font-weight: 300;
            color: var(--text-secondary);
            letter-spacing: 0.05em;
        }

        #intro .btn-primary {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 1s 0.3s, transform 1s 0.3s var(--transition-elegant),
                        background 0.5s, color 0.5s;
            margin-top: 2.5rem;
        }

        #intro .btn-primary.show {
            opacity: 1;
            transform: translateY(0);
        }

        /* ============================================================
           CHAPTER 01 — THE BEGINNING
           ============================================================ */
        #chapter-01 {
            padding-top: 8rem;
        }

        #chapter-01 .chapter-heading {
            font-size: clamp(2rem, 5vw, 3.5rem);
            margin-bottom: 2rem;
        }

        .timeline-marker {
            display: inline-flex;
            align-items: center;
            gap: 0.75rem;
            color: var(--accent);
            font-family: var(--font-sans);
            font-size: 0.75rem;
            letter-spacing: 0.2em;
            text-transform: uppercase;
            margin-bottom: 2rem;
        }

        .timeline-marker::before {
            content: '';
            display: block;
            width: 20px;
            height: 1px;
            background: var(--accent);
        }

        /* ============================================================
           CHAPTER 02 — GALLERY / ARCHIVE
           ============================================================ */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 1.25rem;
            margin-top: 2rem;
        }

        @media (max-width: 500px) {
            .gallery-grid {
                grid-template-columns: 1fr 1fr;
                gap: 0.75rem;
            }
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 4px;
            cursor: pointer;
            background: var(--bg-secondary);
            transition: transform 0.5s var(--transition-elegant);
        }

        .gallery-item:hover {
            transform: translateY(-4px);
        }

        .gallery-item img {
            width: 100%;
            aspect-ratio: 4/5;
            object-fit: cover;
            transition: transform 0.6s var(--transition-elegant),
                        filter 0.6s;
            filter: saturate(0.85);
        }

        .gallery-item:hover img {
            transform: scale(1.05);
            filter: saturate(1);
        }

        .gallery-item .overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(11,13,18,0.85) 0%, transparent 60%);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 1rem;
            opacity: 0;
            transition: opacity 0.4s;
        }

        .gallery-item:hover .overlay {
            opacity: 1;
        }

        .gallery-item .overlay .caption-title {
            font-family: var(--font-serif);
            font-size: 1rem;
            font-weight: 400;
            color: var(--text-primary);
            margin-bottom: 0.25rem;
        }

        .gallery-item .overlay .caption-date {
            font-size: 0.7rem;
            color: var(--accent);
            letter-spacing: 0.1em;
            text-transform: uppercase;
        }

        /* Polaroid variant */
        .gallery-item.polaroid {
            background: var(--text-primary);
            padding: 0.6rem 0.6rem 2.5rem;
            border-radius: 2px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.4);
        }

        .gallery-item.polaroid img {
            aspect-ratio: 1/1;
            border-radius: 0;
        }

        .gallery-item.polaroid .polaroid-caption {
            position: absolute;
            bottom: 0.5rem;
            left: 0.6rem;
            right: 0.6rem;
            text-align: center;
            font-family: var(--font-serif);
            font-size: 0.8rem;
            font-style: italic;
            color: var(--bg-primary);
        }

        /* Placeholder image styling */
        .placeholder-img {
            width: 100%;
            aspect-ratio: 4/5;
            background: var(--bg-tertiary);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: var(--text-secondary);
            font-size: 0.75rem;
            gap: 0.5rem;
        }

        .placeholder-img .icon {
            font-size: 1.5rem;
            opacity: 0.4;
        }

        /* Lightbox / modal */
        .lightbox {
            position: fixed;
            inset: 0;
            z-index: 10002;
            background: rgba(11, 13, 18, 0.96);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.4s, visibility 0s 0.4s;
            padding: 2rem;
        }

        .lightbox.active {
            opacity: 1;
            visibility: visible;
            transition: opacity 0.4s, visibility 0s 0s;
        }

        .lightbox-content {
            max-width: 90vw;
            max-height: 85vh;
            position: relative;
            text-align: center;
        }

        .lightbox-content img {
            max-width: 100%;
            max-height: 75vh;
            object-fit: contain;
            border-radius: 4px;
        }

        .lightbox-caption {
            margin-top: 1rem;
            font-family: var(--font-serif);
            font-size: 1.1rem;
            color: var(--text-primary);
        }

        .lightbox-date {
            font-family: var(--font-sans);
            font-size: 0.75rem;
            color: var(--accent);
            margin-top: 0.35rem;
            letter-spacing: 0.1em;
        }

        .lightbox-story {
            font-family: var(--font-sans);
            font-weight: 300;
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin-top: 0.75rem;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.7;
        }

        .lightbox-close {
            position: absolute;
            top: -3rem;
            right: 0;
            color: var(--text-secondary);
            font-size: 1.5rem;
            cursor: pointer;
            transition: color 0.3s;
            background: none;
            border: none;
            padding: 0.5rem;
        }

        .lightbox-close:hover {
            color: var(--accent);
        }

        .lightbox-nav {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-secondary);
            font-size: 2rem;
            cursor: pointer;
            transition: color 0.3s;
            background: none;
            border: none;
            padding: 1rem;
        }

        .lightbox-nav:hover { color: var(--accent); }
        .lightbox-prev { left: -3rem; }
        .lightbox-next { right: -3rem; }

        @media (max-width: 768px) {
            .lightbox-prev { left: -1rem; font-size: 1.5rem; }
            .lightbox-next { right: -1rem; font-size: 1.5rem; }
        }

        /* ============================================================
           CHAPTER 03 — REVEAL CARDS
           ============================================================ */
        .reveal-cards {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1rem;
            margin-top: 2rem;
            max-width: 560px;
        }

        @media (min-width: 600px) {
            .reveal-cards {
                grid-template-columns: 1fr 1fr;
            }
        }

        .reveal-card {
            background: var(--bg-secondary);
            border: 1px solid rgba(200, 169, 107, 0.08);
            border-radius: 6px;
            padding: 1.5rem;
            cursor: pointer;
            transition: all 0.4s var(--transition-smooth);
            position: relative;
            overflow: hidden;
            min-height: 100px;
        }

        .reveal-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 3px;
            height: 0;
            background: var(--accent);
            transition: height 0.5s var(--transition-elegant);
        }

        .reveal-card:hover {
            border-color: rgba(200, 169, 107, 0.2);
            transform: translateY(-2px);
        }

        .reveal-card:hover::before {
            height: 100%;
        }

        .card-front {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            transition: opacity 0.4s;
        }

        .card-front .card-icon {
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .card-front .card-title {
            font-family: var(--font-sans);
            font-size: 0.85rem;
            font-weight: 400;
            color: var(--text-primary);
            letter-spacing: 0.02em;
        }

        .card-hint {
            font-size: 0.7rem;
            color: var(--text-secondary);
            opacity: 0.5;
            margin-top: 0.5rem;
            font-style: italic;
        }

        .card-back {
            display: none;
            animation: cardReveal 0.6s var(--transition-elegant);
        }

        @keyframes cardReveal {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .card-back .card-message {
            font-family: var(--font-serif);
            font-size: 1.05rem;
            font-weight: 300;
            color: var(--text-primary);
            line-height: 1.7;
            font-style: italic;
        }

        .reveal-card.flipped .card-front { display: none; }
        .reveal-card.flipped .card-back { display: block; }
        .reveal-card.flipped { background: var(--bg-tertiary); }
        .reveal-card.flipped::before { height: 100%; }

        /* ============================================================
           CHAPTER 04 — QUIZ
           ============================================================ */
        .quiz-container {
            max-width: 560px;
            margin-top: 2rem;
        }

        .quiz-progress {
            display: flex;
            gap: 0.5rem;
            margin-bottom: 2rem;
        }

        .quiz-progress .step {
            flex: 1;
            height: 2px;
            background: var(--bg-tertiary);
            border-radius: 2px;
            transition: background 0.4s;
        }

        .quiz-progress .step.active {
            background: var(--accent);
        }

        .quiz-question {
            display: none;
        }

        .quiz-question.active {
            display: block;
            animation: cardReveal 0.5s var(--transition-elegant);
        }

        .quiz-question h3 {
            font-family: var(--font-serif);
            font-size: clamp(1.2rem, 3vw, 1.6rem);
            font-weight: 300;
            margin-bottom: 1.5rem;
            line-height: 1.4;
        }

        .quiz-options {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }

        .quiz-option {
            display: block;
            width: 100%;
            text-align: left;
            padding: 1rem 1.25rem;
            background: var(--bg-secondary);
            border: 1px solid rgba(200, 169, 107, 0.08);
            border-radius: 6px;
            color: var(--text-primary);
            font-size: 0.9rem;
            font-weight: 300;
            transition: all 0.3s;
            cursor: pointer;
        }

        .quiz-option:hover {
            border-color: var(--accent);
            background: var(--bg-tertiary);
        }

        .quiz-option.selected {
            border-color: var(--accent);
            background: var(--accent-dim);
        }

        .quiz-option.correct {
            border-color: #6BCF8E;
            background: rgba(107, 207, 142, 0.1);
        }

        .quiz-option.wrong {
            border-color: #CF6B6B;
            background: rgba(207, 107, 107, 0.1);
        }

        .quiz-feedback {
            margin-top: 1rem;
            font-size: 0.9rem;
            color: var(--accent);
            font-style: italic;
            display: none;
        }

        .quiz-feedback.show { display: block; animation: cardReveal 0.4s; }

        .quiz-next-btn {
            margin-top: 1.5rem;
            display: none;
        }

        .quiz-next-btn.show { display: inline-flex; }

        .quiz-result {
            display: none;
            text-align: center;
            padding: 2rem 0;
        }

        .quiz-result.active {
            display: block;
            animation: cardReveal 0.6s;
        }

        .quiz-result .score-text {
            font-family: var(--font-serif);
            font-size: clamp(1.5rem, 4vw, 2.2rem);
            font-weight: 300;
            margin-bottom: 1rem;
        }

        .quiz-result .score-msg {
            font-size: 0.95rem;
            color: var(--text-secondary);
            line-height: 1.7;
            margin-bottom: 2rem;
        }

        /* ============================================================
           CHAPTER 05 — THE LETTER / HIDDEN NOTE
           ============================================================ */
        .envelope-container {
            display: flex;
            justify-content: center;
            margin-top: 3rem;
        }

        .envelope {
            width: 200px;
            height: 140px;
            background: var(--bg-secondary);
            border: 1px solid rgba(200, 169, 107, 0.15);
            border-radius: 4px;
            position: relative;
            cursor: pointer;
            transition: all 0.5s var(--transition-elegant);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .envelope::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 100px solid transparent;
            border-right: 100px solid transparent;
            border-top: 70px solid var(--bg-tertiary);
            transition: all 0.5s;
        }

        .envelope:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
            box-shadow: 0 10px 40px rgba(200, 169, 107, 0.1);
        }

        .envelope .seal {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: var(--accent);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            color: var(--bg-primary);
            z-index: 1;
            transition: transform 0.3s;
        }

        .envelope:hover .seal {
            transform: scale(1.1);
        }

        .envelope-hint {
            text-align: center;
            margin-top: 1rem;
            font-size: 0.75rem;
            color: var(--text-secondary);
            opacity: 0.5;
        }

        .letter-container {
            display: none;
            max-width: 560px;
            margin: 2rem auto 0;
            padding: 2rem;
            background: var(--bg-secondary);
            border: 1px solid rgba(200, 169, 107, 0.08);
            border-radius: 6px;
            position: relative;
        }

        .letter-container.active {
            display: block;
            animation: cardReveal 0.8s;
        }

        .letter-text {
            font-family: var(--font-serif);
            font-size: 1.1rem;
            font-weight: 300;
            line-height: 2;
            color: var(--text-primary);
        }

        .letter-text .letter-line {
            opacity: 0;
            display: block;
            margin-bottom: 0.5em;
        }

        .letter-text .letter-line.typed {
            opacity: 1;
            animation: lineReveal 0.8s var(--transition-elegant);
        }

        @keyframes lineReveal {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .letter-skip {
            margin-top: 1.5rem;
            text-align: right;
        }

        /* ============================================================
           CHAPTER 06 — FINAL REVEAL
           ============================================================ */
        #chapter-06 {
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        #chapter-06 .final-glow {
            position: absolute;
            width: 500px;
            height: 500px;
            border-radius: 50%;
            background: radial-gradient(circle, var(--accent-glow) 0%, transparent 70%);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            animation: pulse-glow 5s ease-in-out infinite;
            pointer-events: none;
        }

        .final-message {
            font-family: var(--font-serif);
            font-weight: 300;
            font-size: clamp(1rem, 3vw, 1.3rem);
            color: var(--text-secondary);
            margin-bottom: 1rem;
            line-height: 1.6;
        }

        .final-name {
            font-family: var(--font-serif);
            font-weight: 400;
            font-size: clamp(2rem, 6vw, 3.5rem);
            color: var(--text-primary);
            margin-bottom: 0.5rem;
            letter-spacing: 0.02em;
        }

        .final-date {
            font-family: var(--font-sans);
            font-size: 0.8rem;
            color: var(--accent);
            letter-spacing: 0.2em;
            text-transform: uppercase;
            margin-bottom: 0.5rem;
        }

        .final-counter {
            font-family: var(--font-sans);
            font-size: 0.8rem;
            color: var(--text-secondary);
            margin-bottom: 3rem;
        }

        .hidden-message-trigger {
            width: 20px;
            height: 20px;
            margin: 2rem auto 0;
            border-radius: 50%;
            background: var(--accent-dim);
            cursor: pointer;
            transition: all 0.5s;
            border: none;
            opacity: 0.3;
        }

        .hidden-message-trigger:hover {
            opacity: 1;
            transform: scale(1.5);
            background: var(--accent);
            box-shadow: 0 0 20px var(--accent-glow);
        }

        .hidden-extra {
            display: none;
            margin-top: 1.5rem;
            font-family: var(--font-serif);
            font-size: 1rem;
            font-style: italic;
            color: var(--accent);
            animation: cardReveal 0.8s;
        }

        .hidden-extra.show {
            display: block;
        }

        /* ============================================================
           FOOTER
           ============================================================ */
        .site-footer {
            text-align: center;
            padding: 3rem 1.5rem;
            font-size: 0.7rem;
            color: var(--text-secondary);
            opacity: 0.3;
            letter-spacing: 0.1em;
        }

        /* ============================================================
           SKIP/REVEAL LETTER INSTANTLY (reduced motion)
           ============================================================ */
        @media (prefers-reduced-motion: reduce) {
            .intro-line { transition: opacity 0.3s; }
            .reveal { transition: opacity 0.3s; transform: none !important; }
            .reveal.visible { opacity: 1; }
            .gallery-item img { transition: none; }
            .gallery-item:hover { transform: none; }
            .envelope:hover { transform: none; }
        }
    </style>
</head>
<body>

<!-- ================================================================
     CONFIGURATION — Edit this script block to personalize everything.
     ================================================================ -->
<script>
// ═══════════════════════════════════════════════════════════════════
// ██  EDIT THIS SECTION TO CUSTOMIZE YOUR WEBSITE                ██
// ═══════════════════════════════════════════════════════════════════

const CONFIG = {

    // ─── Friend's Info ───────────────────────────────────────────
    friendName: "Alex",
    anniversaryDate: "2020-09-15",   // Format: YYYY-MM-DD (or leave "" to hide counter)

    // ─── Opening Screen Lines ────────────────────────────────────
    introLines: [
        "Not every important story is written down.",
        "Some are simply lived.",
        "I made something for you."
    ],
    introButton: "Enter Our Little World",

    // ─── Chapter 01: The Beginning ───────────────────────────────
    ch01: {
        label: "Chapter 01",
        heading: "Every friendship has a beginning.",
        date: "September 2020",
        paragraphs: [
            "We didn't plan it. There was no dramatic first meeting, no instant spark that lit up the room. It started small — a conversation that lasted longer than expected, a joke that only we understood, a silence that didn't feel uncomfortable.",
            "Somewhere along the way, you stopped being someone I just knew and became someone I couldn't imagine not knowing. That shift happened quietly, the way all important things do.",
            "This is the story of us. Not the version we'd tell anyone else — but the real one."
        ]
    },

    // ─── Chapter 02: Photo Gallery ──────────────────────────────
    // Replace placeholder images with your own.
    // Use relative paths (e.g., "photos/img1.jpg") or full URLs.
    // Set `src: ""` to show a placeholder.
    // Set `polaroid: true` for Polaroid-style framing.
    ch02: {
        label: "Chapter 02",
        heading: "Moments that deserve to stay.",
        subtitle: "A small collection of us.",
        photos: [
            {
                src: "",
                caption: "The one that started it all",
                date: "Sept 2020",
                story: "Replace this with a short story about this photo.",
                polaroid: false
            },
            {
                src: "",
                caption: "That trip we still talk about",
                date: "Summer 2021",
                story: "Add your own memory here.",
                polaroid: true
            },
            {
                src: "",
                caption: "When we didn't stop laughing",
                date: "2022",
                story: "",
                polaroid: false
            },
            {
                src: "",
                caption: "A quiet afternoon",
                date: "2023",
                story: "Sometimes the best moments are the ones where nothing special happened.",
                polaroid: true
            },
            {
                src: "",
                caption: "The most recent one",
                date: "2024",
                story: "",
                polaroid: false
            },
            {
                src: "",
                caption: "Your spot here",
                date: "",
                story: "Add more photos or remove this entry.",
                polaroid: false
            }
        ]
    },

    // ─── Chapter 03: Reveal Cards ───────────────────────────────
    ch03: {
        label: "Chapter 03",
        heading: "Things you should know.",
        subtitle: "A few things I don't say often. Tap to reveal.",
        cards: [
            {
                icon: "✦",
                title: "One thing I respect about you",
                message: "Your ability to stay honest even when it's uncomfortable. You don't say what people want to hear — you say what they need to hear. That takes more courage than most people realize."
            },
            {
                icon: "◈",
                title: "A memory that still makes me laugh",
                message: "Replace this with your own memory. Think of a moment that makes you smile every time it crosses your mind."
            },
            {
                icon: "✧",
                title: "Something you helped me understand",
                message: "That you don't always need a solution. Sometimes showing up and just being there is more than enough. You taught me that without ever saying it."
            },
            {
                icon: "⬥",
                title: "An inside joke only we understand",
                message: "Write your inside joke here. The one that makes no sense to anyone else but makes you both lose it."
            },
            {
                icon: "◇",
                title: "Something I hope never changes",
                message: "The way we can pick up exactly where we left off, no matter how much time has passed. That's rare, and I never want to take it for granted."
            }
        ]
    },

    // ─── Chapter 04: Quiz ───────────────────────────────────────
    ch04: {
        label: "Chapter 04",
        heading: "A small test.",
        subtitle: "How well do you remember us?",
        questions: [
            {
                question: "Where did we first meet?",
                options: [
                    "At school",
                    "Through a mutual friend",
                    "Online",
                    "At that one place we keep forgetting the name of"
                ],
                correct: 1,  // Index (0-based). 1 = "Through a mutual friend"
                feedback: {
                    correct: "You actually remember. I'm impressed.",
                    wrong: "Interesting version of events... but not quite right."
                }
            },
            {
                question: "What's the one food we always end up ordering?",
                options: [
                    "Pizza, obviously",
                    "Sushi",
                    "Burgers from that place",
                    "Whatever's cheapest"
                ],
                correct: 0,
                feedback: {
                    correct: "Some things never change.",
                    wrong: "We clearly need to eat together more."
                }
            },
            {
                question: "What would I say is your most annoying habit?",
                options: [
                    "Being late to everything",
                    "Sending voice notes instead of texts",
                    "Overthinking every small decision",
                    "All of the above, honestly"
                ],
                correct: 3,
                feedback: {
                    correct: "At least you're self-aware about it.",
                    wrong: "I'll let you think about that one."
                }
            }
        ],
        results: {
            perfect: "You remember everything. Some friendships just stay sharp.",
            good: "Pretty solid. You got most of it right.",
            poor: "Your memory could use some work... but I'll keep you around anyway."
        }
    },

    // ─── Chapter 05: The Letter ─────────────────────────────────
    ch05: {
        label: "Chapter 05",
        heading: "There's one more thing.",
        subtitle: "I wrote something. Not because I had to — because I wanted to.",
        letter: [
            "Hey,",
            "I'm not great at saying things like this out loud, so I wrote them down instead.",
            "You've been a constant in a world that doesn't stay still. Not because you had to be, but because you chose to be. And I don't think I've told you enough how much that matters to me.",
            "We've been through things that would've ended most friendships. But somehow we're still here — still laughing at the same stupid things, still having conversations that go nowhere and everywhere at the same time.",
            "I don't know what the next years look like. But I know I want you in them.",
            "Thanks for being the kind of friend most people only get to imagine having.",
            "— Always, your friend"
        ]
    },

    // ─── Chapter 06: Final Reveal ───────────────────────────────
    ch06: {
        message1: "Some memories fade. Some people become part of the story.",
        message2: "Happy Friendship Anniversary,",
        restartButton: "One More Time",
        hiddenMessage: "P.S. — You're stuck with me. No refunds."
    }
};

// ═══════════════════════════════════════════════════════════════════
// ██  END OF CONFIGURATION                                       ██
// ═══════════════════════════════════════════════════════════════════
</script>

<!-- ================================================================
     PROGRESS BAR
     ================================================================ -->
<div class="progress-bar" id="progressBar"></div>

<!-- ================================================================
     CHAPTER NAVIGATION DOTS
     ================================================================ -->
<nav class="chapter-nav" id="chapterNav" aria-label="Chapter navigation">
    <button class="chapter-nav-dot" data-target="chapter-01" data-label="The Beginning" aria-label="Chapter 1"></button>
    <button class="chapter-nav-dot" data-target="chapter-02" data-label="Archive" aria-label="Chapter 2"></button>
    <button class="chapter-nav-dot" data-target="chapter-03" data-label="Things to Know" aria-label="Chapter 3"></button>
    <button class="chapter-nav-dot" data-target="chapter-04" data-label="The Quiz" aria-label="Chapter 4"></button>
    <button class="chapter-nav-dot" data-target="chapter-05" data-label="Hidden Note" aria-label="Chapter 5"></button>
    <button class="chapter-nav-dot" data-target="chapter-06" data-label="Final" aria-label="Chapter 6"></button>
</nav>

<!-- ================================================================
     INTRO / OPENING EXPERIENCE
     ================================================================ -->
<div id="intro">
    <div class="glow-orb"></div>
    <div id="introLines"></div>
    <button class="btn-primary" id="enterBtn" style="display:none;">
        <span id="enterBtnText"></span>
        <span class="arrow">→</span>
    </button>
</div>

<!-- ================================================================
     MAIN CONTENT
     ================================================================ -->
<main id="mainContent" style="display:none;">

    <!-- CHAPTER 01 — THE BEGINNING -->
    <section class="section-container" id="chapter-01">
        <div class="section-inner">
            <span class="chapter-label reveal" id="ch01Label"></span>
            <h2 class="heading-serif chapter-heading reveal reveal-delay-1" id="ch01Heading"></h2>
            <div class="timeline-marker reveal reveal-delay-2" id="ch01Date"></div>
            <div id="ch01Paragraphs"></div>
        </div>
    </section>

    <!-- CHAPTER 02 — GALLERY -->
    <section class="section-container" id="chapter-02">
        <div class="section-inner">
            <span class="chapter-label reveal" id="ch02Label"></span>
            <h2 class="heading-serif chapter-heading reveal reveal-delay-1" id="ch02Heading" style="font-size: clamp(2rem, 5vw, 3.5rem); margin-bottom: 0.5rem;"></h2>
            <p class="body-text reveal reveal-delay-2" id="ch02Subtitle" style="margin-bottom: 2rem;"></p>
            <div class="gallery-grid" id="galleryGrid"></div>
        </div>
    </section>

    <!-- CHAPTER 03 — REVEAL CARDS -->
    <section class="section-container" id="chapter-03">
        <div class="section-inner">
            <span class="chapter-label reveal" id="ch03Label"></span>
            <h2 class="heading-serif chapter-heading reveal reveal-delay-1" id="ch03Heading" style="font-size: clamp(2rem, 5vw, 3.5rem); margin-bottom: 0.5rem;"></h2>
            <p class="body-text reveal reveal-delay-2" id="ch03Subtitle" style="margin-bottom: 1rem;"></p>
            <div class="reveal-cards" id="revealCards"></div>
        </div>
    </section>

    <!-- CHAPTER 04 — QUIZ -->
    <section class="section-container" id="chapter-04">
        <div class="section-inner">
            <span class="chapter-label reveal" id="ch04Label"></span>
            <h2 class="heading-serif chapter-heading reveal reveal-delay-1" id="ch04Heading" style="font-size: clamp(2rem, 5vw, 3.5rem); margin-bottom: 0.5rem;"></h2>
            <p class="body-text reveal reveal-delay-2" id="ch04Subtitle" style="margin-bottom: 1rem;"></p>
            <div class="quiz-container reveal reveal-delay-3" id="quizContainer">
                <div class="quiz-progress" id="quizProgress"></div>
                <div id="quizQuestions"></div>
                <div class="quiz-result" id="quizResult">
                    <div class="score-text" id="quizScoreText"></div>
                    <div class="score-msg" id="quizScoreMsg"></div>
                    <button class="btn-primary" id="quizReplay" onclick="resetQuiz()">
                        <span>Try Again</span>
                        <span class="arrow">↺</span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- CHAPTER 05 — THE LETTER -->
    <section class="section-container" id="chapter-05">
        <div class="section-inner" style="text-align: center;">
            <span class="chapter-label reveal" id="ch05Label"></span>
            <h2 class="heading-serif chapter-heading reveal reveal-delay-1" id="ch05Heading" style="font-size: clamp(2rem, 5vw, 3.5rem); margin-bottom: 0.5rem;"></h2>
            <p class="body-text reveal reveal-delay-2" id="ch05Subtitle" style="margin: 0 auto 1rem; text-align: center;"></p>
            <div class="envelope-container reveal reveal-delay-3">
                <div class="envelope" id="envelope" onclick="openLetter()" role="button" tabindex="0" aria-label="Open letter">
                    <div class="seal">✉</div>
                </div>
            </div>
            <div class="envelope-hint reveal reveal-delay-4" id="envelopeHint">tap to open</div>
            <div class="letter-container" id="letterContainer">
                <div class="letter-text" id="letterText"></div>
                <div class="letter-skip">
                    <button class="btn-ghost" id="letterSkipBtn" onclick="revealFullLetter()">
                        Show full letter →
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- CHAPTER 06 — FINAL REVEAL -->
    <section class="section-container" id="chapter-06">
        <div class="final-glow"></div>
        <div class="section-inner" style="text-align: center; position: relative; z-index: 1;">
            <p class="final-message reveal" id="finalMsg1"></p>
            <div class="section-divider reveal reveal-delay-1" style="margin: 1.5rem auto;"></div>
            <p class="final-message reveal reveal-delay-2" id="finalMsg2"></p>
            <h2 class="final-name heading-serif reveal reveal-delay-3" id="finalName"></h2>
            <p class="final-date reveal reveal-delay-4" id="finalDate"></p>
            <p class="final-counter reveal reveal-delay-4" id="finalCounter"></p>
            <button class="btn-primary reveal reveal-delay-5" id="restartBtn" style="margin-top: 1rem;">
                <span id="restartBtnText"></span>
                <span class="arrow">↺</span>
            </button>
            <button class="hidden-message-trigger reveal reveal-delay-5" id="hiddenTrigger" aria-label="Hidden message" onclick="showHiddenMsg()"></button>
            <div class="hidden-extra" id="hiddenExtra"></div>
        </div>
    </section>

    <footer class="site-footer">
        Made with care, not with templates.
    </footer>
</main>

<!-- ================================================================
     LIGHTBOX
     ================================================================ -->
<div class="lightbox" id="lightbox" role="dialog" aria-label="Image viewer">
    <div class="lightbox-content">
        <button class="lightbox-close" onclick="closeLightbox()" aria-label="Close">&times;</button>
        <button class="lightbox-nav lightbox-prev" onclick="navigateLightbox(-1)" aria-label="Previous">‹</button>
        <button class="lightbox-nav lightbox-next" onclick="navigateLightbox(1)" aria-label="Next">›</button>
        <img id="lightboxImg" src="" alt="">
        <div class="lightbox-caption" id="lightboxCaption"></div>
        <div class="lightbox-date" id="lightboxDate"></div>
        <div class="lightbox-story" id="lightboxStory"></div>
    </div>
</div>

<!-- ================================================================
     MAIN APPLICATION SCRIPT
     ================================================================ -->
<script>
(function() {
    'use strict';

    // ── State ────────────────────────────────────────────────────
    let currentLightboxIndex = 0;
    let quizCurrentQ = 0;
    let quizScore = 0;
    let quizAnswered = [];
    let letterAnimTimeout = null;
    const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

    // ── Populate Content from CONFIG ─────────────────────────────

    function init() {
        populateIntro();
        populateChapter01();
        populateChapter02();
        populateChapter03();
        populateChapter04();
        populateChapter05();
        populateChapter06();
        setupScrollReveals();
        setupProgressBar();
        setupChapterNav();
        setupKeyboard();
    }

    // ─── INTRO ───────────────────────────────────────────────────

    function populateIntro() {
        const container = document.getElementById('introLines');
        CONFIG.introLines.forEach((line, i) => {
            const el = document.createElement('div');
            el.className = 'intro-line';
            el.textContent = line;
            if (i === CONFIG.introLines.length - 1) el.classList.add('sub');
            el.id = 'introLine' + i;
            container.appendChild(el);
        });
        document.getElementById('enterBtnText').textContent = CONFIG.introButton;
        startIntroSequence();
    }

    function startIntroSequence() {
        const lines = CONFIG.introLines;
        const delays = [];
        let cumulativeDelay = 800;

        // Show each line, then fade out lines before the last set
        lines.forEach((_, i) => {
            delays.push(cumulativeDelay);
            cumulativeDelay += 2200;
        });

        // Phase 1 & 2: Show first line, pause, fade it, show second, etc.
        if (prefersReducedMotion) {
            // Show all instantly
            lines.forEach((_, i) => {
                document.getElementById('introLine' + i).classList.add('show');
            });
            const btn = document.getElementById('enterBtn');
            btn.style.display = '';
            btn.classList.add('show');
            return;
        }

        // Sequence: show line 0, wait, fade it, show line 1, wait, fade it, show line 2 + button
        let t = 600;

        // Show line 0
        setTimeout(() => {
            document.getElementById('introLine0').classList.add('show');
        }, t);
        t += 2400;

        // Fade line 0, show line 1
        setTimeout(() => {
            document.getElementById('introLine0').classList.add('fade-out');
        }, t);
        t += 800;

        setTimeout(() => {
            document.getElementById('introLine1').classList.add('show');
        }, t);
        t += 2400;

        // Fade line 1, show line 2 + button
        setTimeout(() => {
            document.getElementById('introLine1').classList.add('fade-out');
        }, t);
        t += 800;

        setTimeout(() => {
            document.getElementById('introLine2').classList.add('show');
        }, t);
        t += 1200;

        setTimeout(() => {
            const btn = document.getElementById('enterBtn');
            btn.style.display = '';
            btn.classList.add('show');
        }, t);
    }

    // Enter the main experience
    document.getElementById('enterBtn').addEventListener('click', function() {
        document.getElementById('intro').classList.add('hidden');
        document.getElementById('mainContent').style.display = 'block';
        document.getElementById('chapterNav').classList.add('visible');
        // Trigger first reveals
        setTimeout(() => {
            triggerVisibleReveals();
        }, 300);
    });

    // Also handle Enter key on envelope
    document.getElementById('envelope').addEventListener('keydown', function(e) {
        if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); openLetter(); }
    });

    // ─── CHAPTER 01 ──────────────────────────────────────────────

    function populateChapter01() {
        document.getElementById('ch01Label').textContent = CONFIG.ch01.label;
        document.getElementById('ch01Heading').textContent = CONFIG.ch01.heading;
        document.getElementById('ch01Date').textContent = CONFIG.ch01.date;
        const cont = document.getElementById('ch01Paragraphs');
        CONFIG.ch01.paragraphs.forEach((p, i) => {
            const el = document.createElement('p');
            el.className = 'body-text reveal reveal-delay-' + Math.min(i + 3, 5);
            el.textContent = p;
            el.style.marginBottom = '1.25rem';
            cont.appendChild(el);
        });
    }

    // ─── CHAPTER 02 ──────────────────────────────────────────────

    function populateChapter02() {
        document.getElementById('ch02Label').textContent = CONFIG.ch02.label;
        document.getElementById('ch02Heading').textContent = CONFIG.ch02.heading;
        document.getElementById('ch02Subtitle').textContent = CONFIG.ch02.subtitle;
        const grid = document.getElementById('galleryGrid');
        CONFIG.ch02.photos.forEach((photo, i) => {
            const item = document.createElement('div');
            item.className = 'gallery-item reveal' + (photo.polaroid ? ' polaroid' : '');
            item.style.transitionDelay = (i * 0.1) + 's';

            if (photo.src) {
                const img = document.createElement('img');
                img.src = photo.src;
                img.alt = photo.caption || 'Photo ' + (i + 1);
                img.loading = 'lazy';
                item.appendChild(img);
            } else {
                const ph = document.createElement('div');
                ph.className = 'placeholder-img';
                ph.innerHTML = '<span class="icon">◻</span><span>Photo ' + (i + 1) + '</span>';
                item.appendChild(ph);
            }

            if (photo.polaroid && photo.caption) {
                const cap = document.createElement('div');
                cap.className = 'polaroid-caption';
                cap.textContent = photo.caption;
                item.appendChild(cap);
            } else if (!photo.polaroid) {
                const overlay = document.createElement('div');
                overlay.className = 'overlay';
                if (photo.caption) {
                    const ct = document.createElement('div');
                    ct.className = 'caption-title';
                    ct.textContent = photo.caption;
                    overlay.appendChild(ct);
                }
                if (photo.date) {
                    const cd = document.createElement('div');
                    cd.className = 'caption-date';
                    cd.textContent = photo.date;
                    overlay.appendChild(cd);
                }
                item.appendChild(overlay);
            }

            item.addEventListener('click', () => openLightbox(i));
            grid.appendChild(item);
        });
    }

    // ─── LIGHTBOX ────────────────────────────────────────────────

    window.openLightbox = function(index) {
        const photos = CONFIG.ch02.photos;
        if (!photos[index] || !photos[index].src) return;
        currentLightboxIndex = index;
        updateLightbox();
        document.getElementById('lightbox').classList.add('active');
        document.body.style.overflow = 'hidden';
    };

    window.closeLightbox = function() {
        document.getElementById('lightbox').classList.remove('active');
        document.body.style.overflow = '';
    };

    window.navigateLightbox = function(dir) {
        const photos = CONFIG.ch02.photos;
        let newIndex = currentLightboxIndex + dir;
        // Find next photo that has a src
        while (newIndex >= 0 && newIndex < photos.length && !photos[newIndex].src) {
            newIndex += dir;
        }
        if (newIndex >= 0 && newIndex < photos.length && photos[newIndex].src) {
            currentLightboxIndex = newIndex;
            updateLightbox();
        }
    };

    function updateLightbox() {
        const photo = CONFIG.ch02.photos[currentLightboxIndex];
        document.getElementById('lightboxImg').src = photo.src;
        document.getElementById('lightboxImg').alt = photo.caption || '';
        document.getElementById('lightboxCaption').textContent = photo.caption || '';
        document.getElementById('lightboxDate').textContent = photo.date || '';
        document.getElementById('lightboxStory').textContent = photo.story || '';
    }

    // Close lightbox on background click
    document.getElementById('lightbox').addEventListener('click', function(e) {
        if (e.target === this) closeLightbox();
    });

    // ─── CHAPTER 03 ──────────────────────────────────────────────

    function populateChapter03() {
        document.getElementById('ch03Label').textContent = CONFIG.ch03.label;
        document.getElementById('ch03Heading').textContent = CONFIG.ch03.heading;
        document.getElementById('ch03Subtitle').textContent = CONFIG.ch03.subtitle;
        const cont = document.getElementById('revealCards');
        CONFIG.ch03.cards.forEach((card, i) => {
            const el = document.createElement('div');
            el.className = 'reveal-card reveal';
            el.style.transitionDelay = (i * 0.1) + 's';
            el.setAttribute('role', 'button');
            el.setAttribute('tabindex', '0');
            el.setAttribute('aria-label', card.title + '. Tap to reveal.');
            el.innerHTML = `
                <div class="card-front">
                    <span class="card-icon">${card.icon}</span>
                    <div>
                        <div class="card-title">${card.title}</div>
                        <div class="card-hint">tap to reveal</div>
                    </div>
                </div>
                <div class="card-back">
                    <div class="card-message">${card.message}</div>
                </div>
            `;
            el.addEventListener('click', function() {
                this.classList.toggle('flipped');
            });
            el.addEventListener('keydown', function(e) {
                if (e.key === 'Enter' || e.key === ' ') {
                    e.preventDefault();
                    this.classList.toggle('flipped');
                }
            });
            cont.appendChild(el);
        });
    }

    // ─── CHAPTER 04 ──────────────────────────────────────────────

    function populateChapter04() {
        document.getElementById('ch04Label').textContent = CONFIG.ch04.label;
        document.getElementById('ch04Heading').textContent = CONFIG.ch04.heading;
        document.getElementById('ch04Subtitle').textContent = CONFIG.ch04.subtitle;

        const progressCont = document.getElementById('quizProgress');
        const qCont = document.getElementById('quizQuestions');

        CONFIG.ch04.questions.forEach((q, qi) => {
            // Progress step
            const step = document.createElement('div');
            step.className = 'step' + (qi === 0 ? ' active' : '');
            step.id = 'quizStep' + qi;
            progressCont.appendChild(step);

            // Question block
            const qDiv = document.createElement('div');
            qDiv.className = 'quiz-question' + (qi === 0 ? ' active' : '');
            qDiv.id = 'quizQ' + qi;

            let optionsHTML = '';
            q.options.forEach((opt, oi) => {
                optionsHTML += `<button class="quiz-option" data-q="${qi}" data-o="${oi}" onclick="selectAnswer(${qi}, ${oi})">${opt}</button>`;
            });

            qDiv.innerHTML = `
                <h3>${q.question}</h3>
                <div class="quiz-options">${optionsHTML}</div>
                <div class="quiz-feedback" id="quizFeedback${qi}"></div>
                <button class="btn-primary quiz-next-btn" id="quizNext${qi}" onclick="nextQuestion(${qi})">
                    <span>${qi < CONFIG.ch04.questions.length - 1 ? 'Next' : 'See Results'}</span>
                    <span class="arrow">→</span>
                </button>
            `;
            qCont.appendChild(qDiv);
        });

        quizAnswered = new Array(CONFIG.ch04.questions.length).fill(false);
    }

    window.selectAnswer = function(qi, oi) {
        if (quizAnswered[qi]) return;
        quizAnswered[qi] = true;

        const q = CONFIG.ch04.questions[qi];
        const buttons = document.querySelectorAll(`[data-q="${qi}"]`);
        buttons.forEach((btn, idx) => {
            btn.disabled = true;
            if (idx === q.correct) btn.classList.add('correct');
            if (idx === oi && oi !== q.correct) btn.classList.add('wrong');
            if (idx === oi) btn.classList.add('selected');
        });

        if (oi === q.correct) quizScore++;

        const fb = document.getElementById('quizFeedback' + qi);
        fb.textContent = oi === q.correct ? q.feedback.correct : q.feedback.wrong;
        fb.classList.add('show');

        document.getElementById('quizNext' + qi).classList.add('show');
    };

    window.nextQuestion = function(qi) {
        const questions = CONFIG.ch04.questions;
        document.getElementById('quizQ' + qi).classList.remove('active');

        if (qi + 1 < questions.length) {
            quizCurrentQ = qi + 1;
            document.getElementById('quizQ' + quizCurrentQ).classList.add('active');
            document.getElementById('quizStep' + quizCurrentQ).classList.add('active');
        } else {
            // Show results
            showQuizResults();
        }
    };

    function showQuizResults() {
        const total = CONFIG.ch04.questions.length;
        const result = document.getElementById('quizResult');
        const scoreText = document.getElementById('quizScoreText');
        const scoreMsg = document.getElementById('quizScoreMsg');

        scoreText.textContent = quizScore + ' / ' + total;

        if (quizScore === total) {
            scoreMsg.textContent = CONFIG.ch04.results.perfect;
        } else if (quizScore >= Math.ceil(total / 2)) {
            scoreMsg.textContent = CONFIG.ch04.results.good;
        } else {
            scoreMsg.textContent = CONFIG.ch04.results.poor;
        }

        result.classList.add('active');
    }

    window.resetQuiz = function() {
        quizScore = 0;
        quizCurrentQ = 0;
        quizAnswered = new Array(CONFIG.ch04.questions.length).fill(false);

        document.getElementById('quizResult').classList.remove('active');

        CONFIG.ch04.questions.forEach((_, qi) => {
            const qDiv = document.getElementById('quizQ' + qi);
            qDiv.classList.remove('active');
            const buttons = qDiv.querySelectorAll('.quiz-option');
            buttons.forEach(btn => {
                btn.classList.remove('correct', 'wrong', 'selected');
                btn.disabled = false;
            });
            document.getElementById('quizFeedback' + qi).classList.remove('show');
            document.getElementById('quizNext' + qi).classList.remove('show');
            document.getElementById('quizStep' + qi).classList.remove('active');
        });

        document.getElementById('quizQ0').classList.add('active');
        document.getElementById('quizStep0').classList.add('active');
    };

    // ─── CHAPTER 05 ──────────────────────────────────────────────

    function populateChapter05() {
        document.getElementById('ch05Label').textContent = CONFIG.ch05.label;
        document.getElementById('ch05Heading').textContent = CONFIG.ch05.heading;
        document.getElementById('ch05Subtitle').textContent = CONFIG.ch05.subtitle;

        const textCont = document.getElementById('letterText');
        CONFIG.ch05.letter.forEach(line => {
            const span = document.createElement('span');
            span.className = 'letter-line';
            span.textContent = line;
            textCont.appendChild(span);
        });
    }

    let letterOpened = false;

    window.openLetter = function() {
        if (letterOpened) return;
        letterOpened = true;
        document.getElementById('envelope').style.display = 'none';
        document.getElementById('envelopeHint').style.display = 'none';
        const cont = document.getElementById('letterContainer');
        cont.classList.add('active');

        if (prefersReducedMotion) {
            revealFullLetter();
            return;
        }

        // Animate lines one by one
        const lines = cont.querySelectorAll('.letter-line');
        lines.forEach((line, i) => {
            letterAnimTimeout = setTimeout(() => {
                line.classList.add('typed');
            }, i * 700);
        });

        // Hide skip button after all lines shown
        setTimeout(() => {
            document.getElementById('letterSkipBtn').style.opacity = '0.3';
        }, lines.length * 700 + 500);
    };

    window.revealFullLetter = function() {
        clearTimeout(letterAnimTimeout);
        const lines = document.querySelectorAll('#letterText .letter-line');
        lines.forEach(line => {
            line.classList.add('typed');
            line.style.animation = 'none';
        });
        document.getElementById('letterSkipBtn').style.display = 'none';
    };

    // ─── CHAPTER 06 ──────────────────────────────────────────────

    function populateChapter06() {
        document.getElementById('finalMsg1').textContent = CONFIG.ch06.message1;
        document.getElementById('finalMsg2').textContent = CONFIG.ch06.message2;
        document.getElementById('finalName').textContent = CONFIG.friendName + '.';
        document.getElementById('restartBtnText').textContent = CONFIG.ch06.restartButton;
        document.getElementById('hiddenExtra').textContent = CONFIG.ch06.hiddenMessage;

        // Date
        if (CONFIG.anniversaryDate) {
            const date = new Date(CONFIG.anniversaryDate + 'T00:00:00');
            if (!isNaN(date.getTime())) {
                const options = { year: 'numeric', month: 'long', day: 'numeric' };
                document.getElementById('finalDate').textContent = date.toLocaleDateString('en-US', options);

                // Duration counter
                const now = new Date();
                const diff = now - date;
                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const years = Math.floor(days / 365);
                const remainingDays = days % 365;
                const months = Math.floor(remainingDays / 30);

                let counterText = '';
                if (years > 0) counterText += years + (years === 1 ? ' year' : ' years');
                if (months > 0) counterText += (counterText ? ', ' : '') + months + (months === 1 ? ' month' : ' months');
                if (years === 0 && months === 0) counterText = days + ' days';
                counterText += ' and counting';
                document.getElementById('finalCounter').textContent = counterText;
            }
        }

        // Restart button
        document.getElementById('restartBtn').addEventListener('click', function() {
            window.scrollTo({ top: 0, behavior: 'instant' });
            document.getElementById('mainContent').style.display = 'none';
            document.getElementById('chapterNav').classList.remove('visible');

            // Reset intro
            const intro = document.getElementById('intro');
            intro.classList.remove('hidden');

            // Reset letter
            letterOpened = false;
            document.getElementById('envelope').style.display = '';
            document.getElementById('envelopeHint').style.display = '';
            document.getElementById('letterContainer').classList.remove('active');
            document.querySelectorAll('#letterText .letter-line').forEach(l => {
                l.classList.remove('typed');
                l.style.animation = '';
            });
            document.getElementById('letterSkipBtn').style.display = '';
            document.getElementById('letterSkipBtn').style.opacity = '';

            // Reset reveal cards
            document.querySelectorAll('.reveal-card').forEach(c => c.classList.remove('flipped'));

            // Reset quiz
            resetQuiz();

            // Reset hidden message
            document.getElementById('hiddenExtra').classList.remove('show');

            // Reset reveals
            document.querySelectorAll('.reveal').forEach(el => el.classList.remove('visible'));

            // Restart intro sequence
            document.querySelectorAll('.intro-line').forEach(l => {
                l.classList.remove('show', 'fade-out');
            });
            document.getElementById('enterBtn').classList.remove('show');
            setTimeout(startIntroSequence, 200);
        });
    }

    window.showHiddenMsg = function() {
        document.getElementById('hiddenExtra').classList.toggle('show');
    };

    // ─── SCROLL REVEALS ──────────────────────────────────────────

    function setupScrollReveals() {
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        });

        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
    }

    function triggerVisibleReveals() {
        document.querySelectorAll('.reveal').forEach(el => {
            const rect = el.getBoundingClientRect();
            if (rect.top < window.innerHeight && rect.bottom > 0) {
                el.classList.add('visible');
            }
        });
    }

    // ─── PROGRESS BAR ────────────────────────────────────────────

    function setupProgressBar() {
        const bar = document.getElementById('progressBar');
        window.addEventListener('scroll', () => {
            const scrollTop = window.scrollY;
            const docHeight = document.documentElement.scrollHeight - window.innerHeight;
            const pct = docHeight > 0 ? (scrollTop / docHeight) * 100 : 0;
            bar.style.width = pct + '%';
        }, { passive: true });
    }

    // ─── CHAPTER NAV ─────────────────────────────────────────────

    function setupChapterNav() {
        const dots = document.querySelectorAll('.chapter-nav-dot');
        const sections = [];
        dots.forEach(dot => {
            const target = document.getElementById(dot.dataset.target);
            if (target) sections.push({ dot, target });
            dot.addEventListener('click', () => {
                target.scrollIntoView({ behavior: 'smooth' });
            });
        });

        window.addEventListener('scroll', () => {
            const scrollY = window.scrollY + window.innerHeight / 2;
            let activeIndex = 0;
            sections.forEach((s, i) => {
                if (s.target.offsetTop <= scrollY) activeIndex = i;
            });
            dots.forEach((d, i) => {
                d.classList.toggle('active', i === activeIndex);
            });
        }, { passive: true });
    }

    // ─── KEYBOARD ────────────────────────────────────────────────

    function setupKeyboard() {
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') {
                closeLightbox();
            }
            if (document.getElementById('lightbox').classList.contains('active')) {
                if (e.key === 'ArrowLeft') navigateLightbox(-1);
                if (e.key === 'ArrowRight') navigateLightbox(1);
            }
        });
    }

    // ─── TOUCH: Swipe for lightbox ───────────────────────────────

    (function() {
        let startX = 0;
        const lb = document.getElementById('lightbox');
        lb.addEventListener('touchstart', (e) => {
            startX = e.changedTouches[0].screenX;
        }, { passive: true });
        lb.addEventListener('touchend', (e) => {
            const diff = e.changedTouches[0].screenX - startX;
            if (Math.abs(diff) > 50) {
                navigateLightbox(diff > 0 ? -1 : 1);
            }
        }, { passive: true });
    })();

    // ─── INIT ────────────────────────────────────────────────────
    if (document.readyState === 'loading') {
        document.addEventListener('DOMContentLoaded', init);
    } else {
        init();
    }

})();
</script>

</body>
</html>
