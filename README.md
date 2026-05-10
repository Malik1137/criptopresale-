<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BNB King ($BNBKING) - Ultimate Crypto Presale & Staking</title>
    <style>
        /* Base & Theme Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            scroll-behavior: smooth;
        }
        body {
            background-color: #080816;
            color: #ffffff;
            overflow-x: hidden;
        }

        /* Navigation Menu Bar */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            background-color: rgba(8, 8, 22, 0.95);
            border-bottom: 2px solid #141430;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }
        
        /* Dynamic SVG Logo Styling */
        .logo {
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: transform 0.3s;
        }
        .logo:hover {
            transform: scale(1.03);
        }
        .logo-svg {
            width: 40px;
            height: 40px;
            fill: none;
            stroke-width: 1.5;
            stroke-linecap: round;
            stroke-linejoin: round;
        }
        .logo-svg .circle {
            stroke: #f3ba2f; /* BNB Yellow */
            stroke-dasharray: 100;
            animation: rotateDash 10s linear infinite;
        }
        .logo-svg .crown {
            fill: #f3ba2f; /* Glowing BNB Yellow */
            stroke: #f3ba2f;
            filter: drop-shadow(0 0 10px rgba(243, 186, 47, 0.7));
        }
        .logo-svg .b {
            fill: #080816;
            stroke: #ffffff;
        }
        .logo-text {
            font-size: 24px;
            font-weight: bold;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 1px;
            background: linear-gradient(to right, #f3ba2f, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        @keyframes rotateDash {
            0% { stroke-dashoffset: 100; }
            100% { stroke-dashoffset: 0; }
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 20px;
            align-items: center;
        }
        .nav-links a {
            color: #a0a0c0;
            text-decoration: none;
            font-size: 15px;
            font-weight: 500;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: #f3ba2f;
        }

        /* Social Icon Links style */
        .social-nav-links {
            display: flex;
            gap: 15px;
            margin-left: 15px;
            border-left: 1px solid #25254d;
            padding-left: 15px;
        }
        .social-icon {
            color: #a0a0c0;
            font-size: 18px;
            text-decoration: none;
            transition: color 0.3s, transform 0.2s;
        }
        .social-icon:hover {
            color: #f3ba2f;
            transform: translateY(-2px);
        }

        /* Buttons */
        .btn-primary {
            background: linear-gradient(135deg, #f3ba2f, #ffea79);
            color: #080816;
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(243, 186, 47, 0.4);
        }

        /* Sections */
        section {
            padding: 100px 8% 80px 8%;
            border-bottom: 1px solid #141430;
        }
        .section-title {
            text-align: center;
            font-size: 36px;
            margin-bottom: 50px;
            color: #f3ba2f;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* Hero & Presale Layout */
        .hero-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
            min-height: 100vh;
            padding-top: 120px;
        }
        .hero-text {
            flex: 1.2;
        }
        .hero-text h1 {
            font-size: 54px;
            line-height: 1.2;
            margin-bottom: 20px;
            background: linear-gradient(to right, #ffffff, #f3ba2f, #ffea79);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .hero-text p {
            color: #a0a0c0;
            font-size: 18px;
            margin-bottom: 30px;
            line-height: 1.6;
        }

        /* Countdown Timer */
        .timer-container {
            display: flex;
            gap: 15px;
            margin-bottom: 30px;
        }
        .time-box {
            background: #11112e;
            border: 1px solid #25254d;
            padding: 10px 15px;
            border-radius: 8px;
            min-width: 70px;
            text-align: center;
        }
        .time-num {
            font-size: 24px;
            font-weight: bold;
            color: #f3ba2f;
        }
        .time-label {
            font-size: 11px;
            color: #a0a0c0;
            text-transform: uppercase;
        }

        /* Interactive Dynamic Visual Hero Art */
        .hero-visual {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            margin-bottom: 20px;
        }
        .hero-visual-svg {
            width: 100%;
            max-width: 260px;
            height: auto;
            filter: drop-shadow(0 0 25px rgba(243, 186, 47, 0.45));
            animation: floatGlow 4s ease-in-out infinite;
        }
        @keyframes floatGlow {
            0% { transform: translateY(0px); filter: drop-shadow(0 0 20px rgba(243, 186, 47, 0.4)); }
            50% { transform: translateY(-12px); filter: drop-shadow(0 0 35px rgba(243, 186, 47, 0.6)); }
            100% { transform: translateY(0px); filter: drop-shadow(0 0 20px rgba(243, 186, 47, 0.4)); }
        }

        /* Presale Box Widget */
        .presale-widget {
            flex: 1;
            background-color: #11112e;
            border: 2px solid #25254d;
            border-radius: 20px;
            padding: 35px;
            max-width: 440px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.6);
        }
        .widget-header {
            text-align: center;
            margin-bottom: 25px;
        }
        .widget-header h3 {
            font-size: 24px;
            color: #ffffff;
            margin-bottom: 5px;
        }
        .widget-header p {
            color: #f3ba2f;
            font-size: 14px;
        }

        /* Progress Bar */
        .progress-container {
            margin-bottom: 25px;
        }
        .progress-labels {
            display: flex;
            justify-content: space-between;
            font-size: 13px;
            color: #a0a0c0;
            margin-bottom: 8px;
        }
        .progress-bar {
            width: 100%;
            height: 15px;
            background-color: #080816;
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid #25254d;
        }
        .progress-fill {
            width: 45%;
            height: 100%;
            background: linear-gradient(90deg, #ffea79, #f3ba2f);
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(243, 186, 47, 0.5);
        }

        .input-group {
            margin-bottom: 20px;
        }
        .input-group label {
            display: block;
            font-size: 13px;
            color: #a0a0c0;
            margin-bottom: 8px;
            text-transform: uppercase;
        }
        .input-group input {
            width: 100%;
            background-color: #080816;
            border: 1px solid #25254d;
            color: #ffffff;
            padding: 14px;
            border-radius: 10px;
            font-size: 16px;
            outline: none;
        }
        .input-group input:focus {
            border-color: #f3ba2f;
        }

        /* Staking Rewards */
        .staking-grid {
            display: flex;
            justify-content: space-between;
            gap: 30px;
            flex-wrap: wrap;
        }
        .staking-card {
            flex: 1;
            min-width: 300px;
            background: #11112e;
            border: 1px solid #25254d;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
        }
        .apy-rate {
            font-size: 48px;
            font-weight: bold;
            color: #f3ba2f;
            margin: 15px 0;
            text-shadow: 0 0 15px rgba(243, 186, 47, 0.2);
        }

        /* Tokenomics */
        .tokenomics-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        .token-data-card {
            background: #11112e;
            border-left: 4px solid #f3ba2f;
            padding: 20px;
            border-radius: 8px;
        }
        .token-data-card h4 {
            color: #a0a0c0;
            font-size: 14px;
            margin-bottom: 5px;
        }
        .token-data-card p {
            font-size: 20px;
            font-weight: bold;
        }

        /* Roadmap */
        .roadmap-timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        .roadmap-item {
            padding: 20px 30px;
            background: #11112e;
            border-radius: 10px;
            margin-bottom: 20px;
            border-left: 4px solid #f3ba2f;
        }
        .roadmap-phase {
            color: #f3ba2f;
            font-weight: bold;
            margin-bottom: 8px;
        }

        /* Footer Section */
        footer {
            background-color: #050510;
            padding: 40px 8%;
            text-align: center;
            border-top: 1px solid #141430;
        }
        .footer-socials {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-bottom: 20px;
        }
        .footer-socials a {
            color: #a0a0c0;
            font-size: 15px;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }
        .footer-socials a:hover {
            color: #f3ba2f;
        }

        /* Responsive Mobile Layout */
        @media (max-width: 968px) {
            .hero-container {
                flex-direction: column;
                text-align: center;
                padding-top: 100px;
            }
            .timer-container {
                justify-content: center;
            }
            .nav-links {
                display: none;
            }
            .navbar {
                padding: 15px 5%;
            }
            .hero-text h1 {
                font-size: 38px;
            }
            .logo-svg {
                width: 35px;
                height: 35px;
            }
            .logo-text {
                font-size: 20px;
            }
            .hero-visual-svg {
                max-width: 200px;
            }
        }
    </style>
</head>
<body>

    <header class="navbar">
        <a href="#" class="logo">
            <svg class="logo-svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                <circle class="circle" cx="50" cy="50" r="45" />
                <path class="crown" d="M30 45 L50 20 L70 45 L70 65 L50 90 L30 65 Z" />
                <path class="b" d="M42 50 Q42 45, 48 45 L52 45 Q58 45, 58 50 L58 52 Q58 57, 52 57 L48 57 Q42 57, 42 52 Z M42 57 L42 60 Q42 65, 48 65 L52 65 Q58 65, 58 60 L58 57 L42 57 Z M48 45 L52 45 L52 48 L48 48 Z M48 62 L52 62 L52 65 L48 65 Z" />
            </svg>
            <span class="logo-text">BNB King</span>
        </a>
        <nav>
            <ul class="nav-links">
                <li><a href="#presale">Presale</a></li>
                <li><a href="#staking">Staking</a></li>
                <li><a href="#tokenomics">Tokenomics</a></li>
                <li><a href="#roadmap">Roadmap</a></li>
                <div class="social-nav-links">
                    <a href="https://t.me/+QGOexl2Y3hEwYTQ1" class="social-icon" target="_blank" title="Telegram">📢 TG</a>
                    <a href="https://x.com/MalikMa39528673" class="social-icon" target="_blank" title="X (Twitter)">🐦 X</a>
                    <a href="https://www.youtube.com/@Tohid552" class="social-icon" target="_blank" title="YouTube">📺 YT</a>
                </div>
            </ul>
        </nav>
        <button class="btn-primary" id="connectWalletBtn" onclick="connectWallet()">Connect Wallet</button>
    </header>

    <section id="presale" class="hero-container">
        <div class="hero-text">
            
            <div class="hero-visual">
                <svg class="hero-visual-svg" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <radialGradient id="glow" cx="50%" cy="50%" r="50%">
                            <stop offset="0%" stop-color="#f3ba2f" stop-opacity="0.5" />
                            <stop offset="100%" stop-color="#080816" stop-opacity="0" />
                        </radialGradient>
                    </defs>
                    <circle cx="100" cy="100" r="90" fill="url(#glow)" />
                    <circle cx="100" cy="100" r="75" fill="none" stroke="#f3ba2f" stroke-width="2" stroke-dasharray="10, 10" />
                    <circle cx="100" cy="100" r="60" fill="#11112e" stroke="#ffea79" stroke-width="4" />
                    <path d="M60 95 L80 60 L100 80 L120 60 L140 95 L140 120 L60 120 Z" fill="#f3ba2f" filter="drop-shadow(0 0 15px rgba(243, 186, 47, 0.8))" />
                    <circle cx="80" cy="55" r="5" fill="#ffffff" />
                    <circle cx="100" cy="75" r="5" fill="#ffffff" />
                    <circle cx="120" cy="55" r="5" fill="#ffffff" />
                    <path d="M75 125 L125 125" stroke="#ffea79" stroke-width="4" stroke-linecap="round" />
                </svg>
            </div>

            <h1>The Ultimate King of BNB Rewards</h1>
            <p>Welcome to BNB King ($BNBKING). Stake your tokens to earn massive APY, or secure your bags early during our Stage 1 Live Presale round. Safest transfer mechanism directly to liquidity pools.</p>
            
            <div class="timer-container">
                <div class="time-box">
                    <div class="time-num" id="days">00</div>
                    <div class="time-label">Days</div>
                </div>
                <div class="time-box">
                    <div class="time-num" id="hours">00</div>
                    <div class="time-label">Hrs</div>
                </div>
                <div class="time-box">
                    <div class="time-num" id="minutes">00</div>
                    <div class="time-label">Min</div>
                </div>
                <div class="time-box">
                    <div class="time-num" id="seconds">00</div>
                    <div class="time-label">Sec</div>
                </div>
            </div>
        </div>

        <div class="presale-widget">
            <div class="widget-header">
                <h3>Buy $BNBKING Tokens</h3>
                <p>1 BNB = 100,000 $BNBKING</p>
            </div>

            <div class="progress-container">
                <div class="progress-labels">
                    <span>Sold: 4,500,000 $BNBKING</span>
                    <span>Goal: 10,000,000</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill"></div>
                </div>
            </div>

            <div class="input-group">
                <label for="amount">Enter Amount (BNB)</label>
                <input type="number" id="amount" placeholder="0.1" step="0.01" min="0.001">
            </div>

            <button class="btn-primary" id="payBtn" style="width: 100%; padding: 15px; font-size: 16px;" onclick="sendTransaction()">Buy $BNBKING Now</button>
        </div>
    </section>

    <section id="staking">
        <h2 class="section-title">👑 High Yield Staking Dashboard</h2>
        <div class="staking-grid">
            <div class="staking-card">
                <h3>Flexible Pool</h3>
                <div class="apy-rate">45% APY</div>
                <p style="color: #a0a0c0; margin-bottom: 20px;">Unstake any time. Simple and instant withdrawal options with zero lock periods.</p>
                <button class="btn-primary" onclick="alert('Staking Pools will activate immediately after the Presale concludes!')">Stake Now</button>
            </div>
            <div class="staking-card" style="border-color: #f3ba2f;">
                <h3>Locked Pool (King's Vault)</h3>
                <div class="apy-rate" style="color: #ffea79;">120% APY</div>
                <p style="color: #a0a0c0; margin-bottom: 20px;">90 Days lock period. Best choice for diamond hands wanting to maximize yield.</p>
                <button class="btn-primary" onclick="alert('Vault Pools will activate immediately after the Presale concludes!')">Lock Now</button>
            </div>
        </div>
    </section>

    <section id="tokenomics">
        <h2 class="section-title">📊 Tokenomics & Supply</h2>
        <div class="tokenomics-info">
            <div class="token-data-card">
                <h4>Total Supply</h4>
                <p>10,000,000,000 $BNBKING</p>
            </div>
            <div class="token-data-card">
                <h4>Presale Allocation</h4>
                <p>40% (4,000,000,000)</p>
            </div>
            <div class="token-data-card">
                <h4>Staking Rewards</h4>
                <p>30% (3,000,000,000)</p>
            </div>
            <div class="token-data-card">
                <h4>Marketing & Listings</h4>
                <p>20% (2,000,000,000)</p>
            </div>
        </div>
    </section>

    <section id="roadmap">
        <h2 class="section-title">🚀 Strategic Roadmap</h2>
        <div class="roadmap-timeline">
            <div class="roadmap-item">
                <div class="roadmap-phase">Phase 1: Project Launch</div>
                <p style="color: #a0a0c0;">Website deployment, Smart contract auditing, Presale round initiation, and community creation.</p>
            </div>
            <div class="roadmap-item">
                <div class="roadmap-phase">Phase 2: Marketing & Presale</div>
                <p style="color: #a0a0c0;">Influencer partnerships, global advertising campaigns, dynamic Token Distribution event.</p>
            </div>
            <div class="roadmap-item">
                <div class="roadmap-phase">Phase 3: Staking & Exchange Listings</div>
                <p style="color: #a0a0c0;">Activation of the 120% APY Staking Vault, CoinGecko and CoinMarketCap submissions, Decentralized exchange listings.</p>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-socials">
            <a href="https://t.me/+QGOexl2Y3hEwYTQ1" target="_blank" title="Telegram">📢 Telegram</a>
            <a href="https://x.com/MalikMa39528673" target="_blank" title="X (Twitter)">🐦 Twitter</a>
            <a href="https://www.youtube.com/@Tohid552" target="_blank" title="YouTube">📺 YouTube</a>
        </div>
        <p style="color: #a0a0c0; font-size: 14px;">&copy; 2026 BNB King. All Rights Reserved.</p>
    </footer>

    <script>
        // Aapka direct transfer BNB Address
        const MY_RECIPIENT_ADDRESS = "0xccdc158a68a013c8f81d6ff9ba5ebc8d6f6acc39"; 
        let userAccount = null;

        // Wallet Connection
        async function connectWallet() {
            if (window.ethereum) {
                try {
                    const accounts = await window.ethereum.request({ method: 'eth_requestAccounts' });
                    userAccount = accounts[0];
                    const formattedAddr = userAccount.substring(0, 6) + "..." + userAccount.substring(userAccount.length - 4);
                    document.getElementById('connectWalletBtn').innerText = formattedAddr;
                } catch (error) {
                    alert("Wallet connection failed.");
                }
            } else {
                alert("Metamask not found! Please open this site inside MetaMask/Trust Wallet dApp Browser.");
            }
        }

        // Send Transaction
        async function sendTransaction() {
            if (!userAccount) {
                alert("Please connect your wallet first!");
                await connectWallet();
                return;
            }

            const amountInput = document.getElementById('amount').value;
            if (!amountInput || amountInput <= 0) {
                alert("Please enter a valid BNB amount!");
                return;
            }

            try {
                const valueInWei = (parseFloat(amountInput) * 1e18).toString(10);
                const valueHex = "0x" + BigInt(valueInWei).toString(16);

                const txParams = {
                    to: MY_RECIPIENT_ADDRESS, 
                    from: userAccount,       
                    value: valueHex,          
                };

                const txHash = await window.ethereum.request({
                    method: 'eth_sendTransaction',
                    params: [txParams],
                });

                alert("Congratulations! Transaction Successful.\nTx Hash: " + txHash);
            } catch (error) {
                alert("Transaction canceled: " + error.message);
            }
        }

        // Presale End Countdown Timer Setup (7 days from now)
        let countdownDate = new Date().getTime() + (7 * 24 * 60 * 60 * 1000);

        setInterval(function() {
            let now = new Date().getTime();
            let distance = countdownDate - now;

            let days = Math.floor(distance / (1000 * 60 * 60 * 24));
            let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            let seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById("days").innerText = days < 10 ? "0" + days : days;
            document.getElementById("hours").innerText = hours < 10 ? "0" + hours : hours;
            document.getElementById("minutes").innerText = minutes < 10 ? "0" + minutes : minutes;
            document.getElementById("seconds").innerText = seconds < 10 ? "0" + seconds : seconds;
        }, 1000);
    </script>
</body>
</html>