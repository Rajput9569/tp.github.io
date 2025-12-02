<!--
CompleteMyOnlineClass - Homepage clone
Single-file HTML + CSS + JS
Replace placeholder images/text/logo as needed.
Author: ChatGPT
-->

<!doctype html>
<html lang="hi">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>CompleteMyOnlineClass - Clone (Demo)</title>
    <meta name="description" content="CompleteMyOnlineClass - Demo clone homepage" />
    <style>
         :root {
            --brand: #0b6cf0;
            /* primary */
            --dark: #0f1723;
            --muted: #6b7280;
            --card: #ffffff;
            --glass: rgba(255, 255, 255, 0.06);
            --radius: 12px;
            font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
        }
        
        * {
            box-sizing: border-box
        }
        
        html,
        body {
            height: 100%;
            margin: 0;
            background: linear-gradient(180deg, #f7f9fc 0%, #ffffff 100%);
            color: var(--dark);
        }
        
        a {
            color: inherit;
            text-decoration: none
        }
        /* ---------- container ---------- */
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px
        }
        /* ---------- header / navbar ---------- */
        
        header {
            backdrop-filter: blur(6px);
            position: sticky;
            top: 0;
            z-index: 60;
            background: rgba(255, 255, 255, 0.8);
            box-shadow: 0 6px 18px rgba(16, 24, 40, 0.06)
        }
        
        .nav {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 14px 0
        }
        
        .brand {
            display: flex;
            align-items: center;
            gap: 10px
        }
        
        .logo {
            width: 40px;
            height: 40px;
            border-radius: 8px;
            background: linear-gradient(135deg, var(--brand), #7dd3fc);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-weight: 700
        }
        
        nav ul {
            display: flex;
            gap: 18px;
            align-items: center;
            margin: 0;
            padding: 0;
            list-style: none
        }
        
        nav a {
            font-weight: 600;
            color: var(--dark);
            opacity: 0.95
        }
        
        .cta {
            display: flex;
            gap: 10px
        }
        
        .btn {
            background: var(--brand);
            color: #fff;
            padding: 10px 14px;
            border-radius: 10px;
            font-weight: 700;
            box-shadow: 0 6px 18px rgba(11, 108, 240, 0.18);
            border: 0;
            cursor: pointer
        }
        
        .btn.ghost {
            background: transparent;
            color: var(--brand);
            border: 2px solid rgba(11, 108, 240, 0.12)
        }
        /* mobile menu button */
        
        .menu-toggle {
            display: none;
            background: transparent;
            border: 0;
            padding: 8px;
            border-radius: 8px
        }
        /* ---------- hero ---------- */
        
        .hero {
            display: grid;
            grid-template-columns: 1fr 480px;
            gap: 36px;
            align-items: center;
            padding: 56px 0
        }
        
        .hero-left {
            padding-right: 10px
        }
        
        .eyebrow {
            display: inline-block;
            background: rgba(11, 108, 240, 0.08);
            color: var(--brand);
            padding: 6px 10px;
            border-radius: 999px;
            font-weight: 700;
            margin-bottom: 18px
        }
        
        h1 {
            font-size: clamp(28px, 4.6vw, 44px);
            margin: 0 0 16px;
            line-height: 1.05
        }
        
        p.lead {
            color: var(--muted);
            font-size: 16px;
            margin: 0 0 20px
        }
        
        .hero-actions {
            display: flex;
            gap: 12px;
            flex-wrap: wrap
        }
        
        .hero-right {
            position: relative
        }
        
        .hero-card {
            background: linear-gradient(180deg, #ffffff, #f8fbff);
            border-radius: 20px;
            padding: 18px;
            box-shadow: 0 20px 50px rgba(16, 24, 40, 0.08)
        }
        
        .hero-image {
            width: 100%;
            height: 300px;
            border-radius: 12px;
            background-size: cover;
            background-position: center
        }
        /* stats */
        
        .stats {
            display: flex;
            gap: 12px;
            margin-top: 16px
        }
        
        .stat {
            background: rgba(15, 23, 35, 0.03);
            padding: 10px 12px;
            border-radius: 10px;
            font-weight: 700
        }
        /* ---------- features / cards ---------- */
        
        .grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 18px;
            margin-top: 36px
        }
        
        .card {
            background: var(--card);
            padding: 18px;
            border-radius: 14px;
            box-shadow: 0 8px 30px rgba(16, 24, 40, 0.06)
        }
        
        .card h3 {
            margin: 0 0 8px
        }
        
        .card p {
            margin: 0;
            color: var(--muted)
        }
        /* ---------- courses list ---------- */
        
        .courses {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 18px;
            margin: 36px 0
        }
        
        .course {
            background: linear-gradient(180deg, #fff, #fbfdff);
            border-radius: 12px;
            padding: 12px;
            display: flex;
            gap: 12px;
            align-items: center
        }
        
        .course .thumb {
            width: 90px;
            height: 70px;
            border-radius: 8px;
            background-size: cover;
            background-position: center
        }
        
        .course .meta {
            flex: 1
        }
        
        .pill {
            font-size: 12px;
            padding: 6px 8px;
            border-radius: 999px;
            display: inline-block;
            background: rgba(11, 108, 240, 0.08);
            color: var(--brand);
            font-weight: 700
        }
        /* ---------- CTA strip ---------- */
        
        .cta-strip {
            background: linear-gradient(90deg, rgba(11, 108, 240, 0.06), rgba(124, 58, 237, 0.04));
            padding: 26px;
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 12px
        }
        /* ---------- footer ---------- */
        
        footer {
            margin-top: 40px;
            padding: 36px 0;
            color: var(--muted)
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px
        }
        /* responsive */
        
        @media(max-width:980px) {
            .hero {
                grid-template-columns: 1fr;
            }
            .hero-right {
                order: 2
            }
            .hero-left {
                order: 1
            }
            .grid,
            .courses {
                grid-template-columns: repeat(2, 1fr)
            }
        }
        
        @media(max-width:640px) {
            nav ul {
                display: none
            }
            .menu-toggle {
                display: block
            }
            .hero {
                padding: 28px 0
            }
            .grid,
            .courses {
                grid-template-columns: 1fr
            }
            .hero-right {
                display: block
            }
            .hero-image {
                height: 220px
            }
        }
        /* mobile menu slide */
        
        .mobile-menu {
            position: fixed;
            inset: 0;
            background: rgba(8, 10, 15, 0.5);
            display: none;
            align-items: flex-start;
            padding: 80px 20px 20px;
            z-index: 80
        }
        
        .mobile-menu .panel {
            background: #fff;
            border-radius: 12px;
            padding: 20px;
            max-width: 320px;
            width: 100%
        }
        
        .mobile-menu.show {
            display: flex
        }
        /* small helpers */
        
        .muted {
            color: var(--muted)
        }
        
        .center {
            display: flex;
            align-items: center;
            justify-content: center
        }
    </style>
</head>

<body>
    <header>
        <div class="container">
            <div class="nav">
                <div class="brand">
                    <div class="logo">CM</div>
                    <div>
                        <div style="font-weight:800">CompleteMyOnlineClass</div>
                        <div style="font-size:12px;color:var(--muted);margin-top:2px">Fast. Reliable. Affordable.</div>
                    </div>
                </div>

                <nav>
                    <ul>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#courses">Courses</a></li>
                        <li><a href="#how">How it works</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>

                <div class="cta">
                    <button class="btn ghost" id="loginBtn">Login</button>
                    <button class="btn" id="signupBtn">Get Started</button>
                    <button class="menu-toggle" id="menuToggle" aria-label="Open menu">☰</button>
                </div>
            </div>
        </div>
    </header>

    <!-- mobile menu -->
    <div class="mobile-menu" id="mobileMenu" role="dialog" aria-modal="true">
        <div class="panel">
            <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:16px">
                <div style="display:flex;gap:8px;align-items:center">
                    <div class="logo">CM</div><strong>CompleteMyOnlineClass</strong></div>
                <button id="closeMenu" style="background:none;border:0;font-size:20px">✕</button>
            </div>
            <nav style="display:flex;flex-direction:column;gap:12px">
                <a href="#services">Services</a>
                <a href="#courses">Courses</a>
                <a href="#how">How it works</a>
                <a href="#contact">Contact</a>
            </nav>
            <div style="margin-top:18px;display:flex;gap:8px">
                <button class="btn ghost" style="flex:1">Login</button>
                <button class="btn" style="flex:1">Sign up</button>
            </div>
        </div>
    </div>

    <main class="container">
        <section class="hero">
            <div class="hero-left">
                <span class="eyebrow">Trusted since 2018</span>
                <h1>Online class assignments, projects, and tests — hum kar denge.
                </h1>
                <p class="lead">High-quality solutions, quick turnaround, and secure delivery. Get help from expert tutors and subject-matter specialists — live chat support available.</p>
                <div class="hero-actions">
                    <button class="btn">Place an order</button>
                    <button class="btn ghost">How it works</button>
                    <div style="align-self:center;color:var(--muted);font-weight:700">or call: <span style="color:var(--brand)">+91-90000-00000</span></div>
                </div>

                <div class="stats">
                    <div class="stat">5k+ orders completed</div>
                    <div class="stat">4.8/5 rating</div>
                    <div class="stat">24/7 support</div>
                </div>

                <div class="grid" id="services">
                    <div class="card">
                        <h3>Assignments</h3>
                        <p>We handle programming, essays, reports and more — delivered with code comments and explanations.</p>
                    </div>
                    <div class="card">
                        <h3>Quizzes & Tests</h3>
                        <p>Secure, time-bound solutions and step-by-step answers for objective quizzes.</p>
                    </div>
                    <div class="card">
                        <h3>Projects</h3>
                        <p>End-to-end project development with documentation, demos and test cases.</p>
                    </div>
                </div>

            </div>

            <div class="hero-right">
                <div class="hero-card">
                    <div class="hero-image" style="background-image:url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=1400&auto=format&fit=crop&s=1bd3ac7c91f3f77c3b7a3b6a2d0f4f8d');"></div>
                    <div style="display:flex;justify-content:space-between;align-items:center;margin-top:12px">
                        <div>
                            <strong>Featured service</strong>
                            <div class="muted" style="font-size:13px">Custom coding assignment — 24 hr delivery</div>
                        </div>
                        <div style="text-align:right">
                            <div style="font-weight:800">₹499</div>
                            <div class="muted" style="font-size:12px">Starting price</div>
                        </div>
                    </div>
                    <div style="display:flex;gap:8px;margin-top:12px">
                        <button class="btn" style="flex:1">Order now</button>
                        <button class="btn ghost" style="flex:1">Chat with tutor</button>
                    </div>
                </div>

                <div style="display:flex;gap:12px;margin-top:14px">
                    <div style="flex:1" class="card center">
                        <div>
                            <div style="font-weight:800;font-size:22px">100+</div>
                            <div class="muted">Subjects</div>
                        </div>
                    </div>
                    <div style="flex:1" class="card center">
                        <div>
                            <div style="font-weight:800;font-size:22px">3000+</div>
                            <div class="muted">Happy students</div>
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <section id="courses">
            <div style="display:flex;align-items:center;justify-content:space-between">
                <h2>Popular Services</h2>
                <a href="#" class="muted">View all</a>
            </div>

            <div class="courses">
                <div class="course">
                    <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=1400&auto=format&fit=crop&s=3d8f3d9f3b2a8b7a4f3f7f8b1f2e3c4d')"></div>
                    <div class="meta">
                        <div style="display:flex;align-items:center;gap:8px">
                            <div class="pill">Programming</div><strong>Java Assignment</strong></div>
                        <div class="muted">Detailed comments + sample outputs</div>
                    </div>
                    <div style="text-align:right">
                        <div style="font-weight:800">₹799</div>
                        <div class="muted">from</div>
                    </div>
                </div>

                <div class="course">
                    <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1526378721793-5f5a3f4b6b4e?q=80&w=1400&auto=format&fit=crop&s=8f2a1b6c9e1d2f3a4b5c6d7e8f9a0b1c')"></div>
                    <div class="meta">
                        <div style="display:flex;align-items:center;gap:8px">
                            <div class="pill">Data</div><strong>Matlab Project</strong></div>
                        <div class="muted">Plots, scripts, report</div>
                    </div>
                    <div style="text-align:right">
                        <div style="font-weight:800">₹1299</div>
                        <div class="muted">from</div>
                    </div>
                </div>

                <div class="course">
                    <div class="thumb" style="background-image:url('https://images.unsplash.com/photo-1526378721793-5f5a3f4b6b4e?q=80&w=1400&auto=format&fit=crop&s=8f2a1b6c9e1d2f3a4b5c6d7e8f9a0b1c')"></div>
                    <div class="meta">
                        <div style="display:flex;align-items:center;gap:8px">
                            <div class="pill">Essay</div><strong>Business Report</strong></div>
                        <div class="muted">Research + citations</div>
                    </div>
                    <div style="text-align:right">
                        <div style="font-weight:800">₹599</div>
                        <div class="muted">from</div>
                    </div>
                </div>

            </div>
        </section>

        <section id="how" style="margin-top:8px">
            <h2>How it works</h2>
            <div style="display:flex;gap:12px;margin-top:12px;flex-wrap:wrap">
                <div class="card" style="flex:1;min-width:220px">
                    <h3>1. Place an order</h3>
                    <p class="muted">Tell us your requirements, deadline, and attachments.</p>
                </div>
                <div class="card" style="flex:1;min-width:220px">
                    <h3>2. We assign an expert</h3>
                    <p class="muted">A subject-matter expert starts working and keeps you updated.</p>
                </div>
                <div class="card" style="flex:1;min-width:220px">
                    <h3>3. Delivery & revisions</h3>
                    <p class="muted">Download the work, ask for revisions if needed.</p>
                </div>
            </div>
        </section>

        <section style="margin-top:36px" id="contact">
            <div class="cta-strip">
                <div>
                    <div style="font-weight:800;font-size:18px">Get help now — first consultation free</div>
                    <div class="muted">Chat with an expert or place an order — 24/7</div>
                </div>
                <div style="display:flex;gap:10px;align-items:center">
                    <input id="email" placeholder="Your email" style="padding:10px;border-radius:10px;border:1px solid rgba(15,23,35,0.06)" />
                    <button class="btn" id="subscribeBtn">Contact us</button>
                </div>
            </div>
        </section>

        <footer>
            <div class="footer-grid">
                <div>
                    <strong>CompleteMyOnlineClass</strong>
                    <div class="muted" style="margin-top:8px">Helping students since 2018. Confidential and trustworthy service.</div>
                </div>
                <div>
                    <h4>Services</h4>
                    <div class="muted">Assignments<br/>Projects<br/>Quizzes</div>
                </div>
                <div>
                    <h4>Company</h4>
                    <div class="muted">About<br/>Terms<br/>Privacy</div>
                </div>
                <div>
                    <h4>Contact</h4>
                    <div class="muted">support@completemyonlineclass.com<br/>+91-90000-00000</div>
                </div>
            </div>
        </footer>

    </main>

    <script>
        // Mobile menu toggles
        const menuToggle = document.getElementById('menuToggle');
        const mobileMenu = document.getElementById('mobileMenu');
        const closeMenu = document.getElementById('closeMenu');
        menuToggle.addEventListener('click', () => mobileMenu.classList.add('show'));
        closeMenu.addEventListener('click', () => mobileMenu.classList.remove('show'));
        mobileMenu.addEventListener('click', (e) => {
            if (e.target === mobileMenu) mobileMenu.classList.remove('show')
        });

        // Simple form interaction
        const subscribeBtn = document.getElementById('subscribeBtn');
        subscribeBtn.addEventListener('click', () => {
            const email = document.getElementById('email').value.trim();
            if (!email || !email.includes('@')) {
                alert('Please enter a valid email.');
                return;
            }
            // Fake submit - replace with real request
            alert('Thank you! We will contact you at ' + email);
            document.getElementById('email').value = '';
        });

        // Demo: scroll to section when nav links clicked (smooth)
        document.querySelectorAll('a[href^="#"]').forEach(a => {
            a.addEventListener('click', e => {
                const href = a.getAttribute('href');
                if (href.length > 1) {
                    e.preventDefault();
                    document.querySelector(href).scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                    if (window.innerWidth < 640) mobileMenu.classList.remove('show');
                }
            })
        })
    </script>

</body>

</html>
