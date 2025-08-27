<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lumen - AI-Powered Grid Forecasting</title>
    <style>
        :root {
            --primary-purple: #6B46C1;
            --accent-purple: #8B5CF6;
            --light-purple: #EDE9FE;
            --dark-purple: #4C1D95;
            --text-dark: #1F2937;
            --text-light: #6B7280;
            --bg-white: #FFFFFF;
            --bg-gray: #F9FAFB;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Calibri', 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background: var(--bg-white);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: var(--bg-white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary-purple);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-purple);
        }

        .cta-button {
            background: var(--primary-purple);
            color: white;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s ease;
            cursor: pointer;
        }

        .cta-button:hover {
            background: var(--dark-purple);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-purple) 0%, var(--accent-purple) 100%);
            color: white;
            padding: 8rem 0 4rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: bold;
        }

        .hero .subtitle {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero-description {
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto 2rem;
            opacity: 0.8;
        }

        /* Word Cloud Section */
        .word-cloud-section {
            padding: 4rem 0;
            background: var(--bg-gray);
        }

        .word-cloud {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
        }

        .word {
            background: var(--light-purple);
            color: var(--primary-purple);
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }

        .word:hover {
            background: var(--primary-purple);
            color: white;
            transform: translateY(-2px);
        }

        .word.large {
            font-size: 1.5rem;
            padding: 0.75rem 1.5rem;
        }

        .word.medium {
            font-size: 1.25rem;
            padding: 0.6rem 1.25rem;
        }

        /* Features Section */
        .features {
            padding: 4rem 0;
        }

        .features h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary-purple);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            background: var(--light-purple);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
            font-size: 1.5rem;
            color: var(--primary-purple);
        }

        .feature-card h3 {
            color: var(--primary-purple);
            margin-bottom: 1rem;
        }

        /* Market Impact Section */
        .market-impact {
            background: var(--primary-purple);
            color: white;
            padding: 4rem 0;
        }

        .impact-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .stat {
            padding: 1rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* Footer */
        footer {
            background: var(--text-dark);
            color: white;
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            color: var(--accent-purple);
            margin-bottom: 1rem;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #374151;
            opacity: 0.7;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .subtitle {
                font-size: 1.2rem;
            }

            .word-cloud {
                gap: 1rem;
            }

            .word {
                font-size: 0.9rem;
                padding: 0.4rem 0.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">Lumen</div>
            <ul class="nav-links">
                <li><a href="#features">Features</a></li>
                <li><a href="#impact">Impact</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#demo" class="cta-button">Request Demo</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Welcome to Lumen</h1>
            <p class="subtitle">World's First Data-Driven AI Forecasting Engine</p>
            <p class="hero-description">
                Revolutionizing grid management with probabilistic forecasting, prescriptive recommendations, 
                and hyper-local weather modeling for a renewable-powered future.
            </p>
            <a href="#features" class="cta-button" style="font-size: 1.1rem; padding: 1rem 2rem;">
                Explore Our Solution
            </a>
        </div>
    </section>

    <!-- Word Cloud Section -->
    <section class="word-cloud-section">
        <div class="container">
            <h2 style="text-align: center; margin-bottom: 2rem; color: var(--primary-purple);">
                Powering the Future of Grid Intelligence
            </h2>
            <div class="word-cloud">
                <span class="word large">AI Forecasting</span>
                <span class="word medium">Grid Optimization</span>
                <span class="word">Renewable Integration</span>
                <span class="word medium">Smart Analytics</span>
                <span class="word">Demand Response</span>
                <span class="word large">Predictive Intelligence</span>
                <span class="word">Real-time Monitoring</span>
                <span class="word medium">Energy Efficiency</span>
                <span class="word">Load Balancing</span>
                <span class="word">Cost Reduction</span>
                <span class="word medium">Sustainability</span>
                <span class="word">Grid Stability</span>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <h2>Core Capabilities</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">🔮</div>
                    <h3>Probabilistic Forecasting</h3>
                    <p>Advanced AI algorithms predict renewable energy variability with confidence intervals, 
                    enabling better grid planning and reducing forecast errors by >15%.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3>Prescriptive Recommendations</h3>
                    <p>Real-time dispatch optimization and load-shifting suggestions that help operators 
                    make data-driven decisions and avoid costly DSM penalties.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌦️</div>
                    <h3>Hyper-Local Weather Modeling</h3>
                    <p>Granular weather predictions at the feeder level enable precise solar and wind 
                    generation forecasts, maximizing renewable energy utilization.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📊</div>
                    <h3>SCADA Integration</h3>
                    <p>Seamless integration with existing grid infrastructure provides real-time visibility 
                    and enables immediate response to changing grid conditions.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">☁️</div>
                    <h3>Cloud-Native Architecture</h3>
                    <p>Scalable, secure cloud deployment ensures rapid rollout across utilities 
                    with minimal infrastructure investment.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🎯</div>
                    <h3>Anomaly Detection</h3>
                    <p>Advanced pattern recognition identifies grid anomalies and potential failures 
                    before they impact operations, preventing costly outages.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Market Impact Section -->
    <section class="market-impact" id="impact">
        <div class="container">
            <h2 style="text-align: center; margin-bottom: 3rem;">Transforming Grid Economics</h2>
            <div class="impact-stats">
                <div class="stat">
                    <div class="stat-number">20%+</div>
                    <div class="stat-label">Reduction in DSM Penalties</div>
                </div>
                <div class="stat">
                    <div class="stat-number">30%</div>
                    <div class="stat-label">Higher Grid Utilization</div>
                </div>
                <div class="stat">
                    <div class="stat-number">50%</div>
                    <div class="stat-label">Less Renewable Curtailment</div>
                </div>
                <div class="stat">
                    <div class="stat-number">15%</div>
                    <div class="stat-label">More Renewable Integration</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Lumen AI</h3>
                    <p>Revolutionizing grid management through intelligent forecasting and optimization.</p>
                </div>
                <div class="footer-section">
                    <h3>Solutions</h3>
                    <p>• Grid Forecasting<br>
                    • Renewable Integration<br>
                    • Demand Optimization<br>
                    • Real-time Analytics</p>
                </div>
                <div class="footer-section">
                    <h3>Contact</h3>
                    <p>Ready to transform your grid operations?<br>
                    Get in touch for a personalized demo.</p>
                    <a href="#demo" class="cta-button" style="margin-top: 1rem; display: inline-block;">
                        Schedule Demo
                    </a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Lumen AI. Powering the future of intelligent grids.</p>
            </div>
        </div>
    </footer>
</body>
</html>
