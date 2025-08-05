# Chainforge
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ChainForge XP + Market Dashboard</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background: #0d0d0d;
      color: #f0f0f0;
      padding: 20px;
    }
    h2 {
      color: #00ccff;
      border-bottom: 1px solid #222;
      padding-bottom: 10px;
      margin-top: 30px;
    }
    .section {
      margin-bottom: 30px;
    }
    .card {
      background: #1a1a1a;
      border: 1px solid #222;
      border-radius: 10px;
      padding: 15px;
      margin-bottom: 15px;
      box-shadow: 0 0 8px rgba(0, 204, 255, 0.1);
    }
    .task-complete {
      background: #004455;
    }
    .task-incomplete {
      background: #332200;
    }
    .graph-placeholder {
      background: #111;
      border: 2px dashed #333;
      height: 200px;
      margin-top: 15px;
      text-align: center;
      line-height: 200px;
      color: #666;
      border-radius: 8px;
    }
    .badge {
      background: #00ccff22;
      color: #00ccff;
      font-size: 0.85em;
      padding: 4px 10px;
      border-radius: 20px;
      margin-left: 10px;
    }
  </style>
</head>
<body>

<h1>🔗 ChainForge: Team XP + Market Dashboard</h1>

<div class="section">
  <h2>📈 Market Tracker XP</h2>
  <div class="card">
    <strong>Task:</strong> Logged in during BTC +4% spike
    <span class="badge">+25 XP</span><br>
    <em>Status:</em> Complete ✅
  </div>
  <div class="card">
    <strong>Task:</strong> Suggested sell zone for $AVAX at $26
    <span class="badge">+40 XP</span><br>
    <em>Status:</em> Confirmed +7.3% gain
  </div>
  <div class="graph-placeholder">[BTC Price vs XP Gained Graph]</div>
</div>

<div class="section">
  <h2>🧠 Insight & Missions</h2>
  <div class="card">
    <strong>Task:</strong> Posted thread: “What Hashrate Teaches Us”
    <span class="badge">+15 XP</span><br>
    <em>Status:</em> 3 teammates viewed, 1 bookmarked
  </div>
  <div class="card task-incomplete">
    <strong>Weekly Mission:</strong> Share 1 low-cap altcoin under $30M MC
    <span class="badge">Pending</span><br>
    <em>Due:</em> Sunday
  </div>
</div>

<div class="section">
  <h2>👥 Team Feedback & Watchlist</h2>
  <div class="card">
    <strong>Altcoin Watch:</strong> $KAS — Suggested by ChainMaster21
    <span class="badge">4 votes</span><br>
    <em>Sentiment:</em> “Innovative PoW potential”<br>
    <em>Target:</em> 15% gain suggested. Watchlist status: <strong>Active</strong>
  </div>
  <div class="card">
    <strong>Timing Journal:</strong> Sold $INJ at $30.5
    <br><em>Outcome:</em> Price dropped to $27.8 — ✔️ Good call
  </div>
  <div class="graph-placeholder">[Team XP Split by Member / Category]</div>
</div>

</body>
</html>

(https://img.shields.io/badge/Built%20With-HTML%2FCSS%2FJS-blue)
![Status]
(https://img.shields.io/badge/Status-Prototype-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)
https://github.com/Steener99/Chainforge.git

## 🖼️ Dashboard Preview
## 🖼️ Dashboard Hero

> ChainForge XP Dashboard — Track XP, Missions, Wallets, and Team Power.

![ChainForge Hero](./assets/chainforge-hero.png)
> Simulated XP Dashboard featuring Market Tracker, Missions, Wallet Preview & Team Feedback.

![ChainForge Dashboard](./ChainForge_XP_+.png)
![ChainForge Dashboard](./chainforge-dashboard.png)

from pathlib import Path
## 🖼️ Screenshots

> ChainForge XP Dashboard, Simulated Wallet, and Market Feedback Preview


🔗 **ChainForge** is an XP-driven crypto intelligence dashboard that empowers users with:
- Real-time market task tracking
- Team collaboration via XP contribution
- Wallet simulation and mining strategy insight
- A gamified approach to blockchain analytics

## 🚀 Features
- 🔥 "Begin Your Forge" startup interaction
- 📊 Dynamic XP & market chart integration (powered by Chart.js)
- 🧠 Mission tracker for individual and team insights
- 💼 Wallet preview and simulated balance tracking

## 📁 Structure
This is a single-page HTML application:
- `index.html` – Main interface
- All logic, charts, and style are inline for simplicity (no build step needed)

## 🛠 Roadmap
- [ ] Live wallet API integration
- [ ] Team XP leaderboard syncing
- [ ] ForgeChest rewards system
- [ ] Token tracker & trade simulation

## ⚖ License
MIT License

---

Made with passion, precision, and community fire. 🔥
"""

license_content = """MIT License

Copyright (c) 2025 Tanner Dawson

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
"""

# Paths
readme_path = Path("/mnt/data/README.md")
license_path = Path("/mnt/data/LICENSE")

# Write files
readme_path.write_text(readme_content)
license_path.write_text(license_content)

[readme_path.name, license_path.name]
## 🧬 What is ChainForge?

ChainForge is a crypto intelligence dashboard that gamifies blockchain analysis.

It rewards user activity with XP, tracks team performance, and simulates wallet interactions — transforming market strategy into an engaging, forge-like experience.
 🌐 Live Demo

➡️ [Launch the ChainForge Dashboard](https://your-netlify-site.netlify.app)

> Simulated environment: XP tracker, wallet UI, and live graphs.
> ## 🧱 Architecture

- **Frontend:** Pure HTML + CSS + JavaScript (Chart.js)
- **Hosting:** Netlify (single-page static app)
- **No backend yet:** All data is simulated

Future phases will introduce:
- Wallet APIs
- XP history DB
- Token integration
## 🧪 Run Locally

Just open `index.html` in any browser.
No installation or build tools required
## 🧠 Creators

- **Tanner Dawson Steen** – Vision, design, implementation
- (More to be added as team expands)
- ## 🔮 Coming Soon

- $CHAIN Token Simulation & Reward System
- ForgeChest Leaderboards
- Team Strategy Missions
- Altcoin & Sell-Zone Suggestion Tools
- Smart Contract Integration
- ## 📬 Contact

For investor access, demos, or questions:
📧 Tanner Steen – dennydimension@gmail.com
## 🖼️ Screenshots

![Dashboard Preview](./assets/chainforge-dashboard.png)
> Live XP tracker + wallet preview + mission cards
> ![HTML](https://img.shields.io/badge/Built%20With-HTML%2FCSS%2FJS-blue)
![Status](https://img.shields.io/badge/Status-Prototype-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)
> ## 🤝 Contributing

We welcome ideas, UX feedback, and crypto visionaries to help evolve ChainForge.

📬 Reach out via issues, or connect directly if you're interested in joining the forge.
# ChainForge

[Badges]

## 🧬 What is ChainForge?
## 🌐 Live Demo
## 🧱 Architecture
## 📁 Structure
## 🖼️ Screenshots
## 🧠 Creators
## 🔮 Roadmap
## 🤝 Contributing
## 📊 For Investors
## ⚖ License

from pathlib import Path
from PIL import Image
import shutil

# Redefine paths after code reset
src_path = "/mnt/data/A_branding_image_for_ChainForge_XP_Intelligence_Da.png"
dst_path = "/mnt/data/chainforge-logo.png"

# Copy file for GitHub-friendly name
shutil.copy(src_path, dst_path)

# Return path to user
dst_path
## 🔗 ChainForge Logo

![ChainForge Logo](./chainforge-logo.png)
This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.
