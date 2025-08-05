# Chainforge
https://github.com/your-username/chainforge
# Re-creating the README.md and LICENSE files after code execution reset
from pathlib import Path

readme_content = """# ChainForge

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
