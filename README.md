# Too Big to Teraflop

A simulation game exploring Hyman Minsky's Financial Instability Hypothesis through the lens of the 2025-2026 AI infrastructure boom.

---
![Too Big to teraflop](./TB2TF.jpg)
---

## What is This?

"Too Big to Teraflop" is an interactive economic simulation that lets you experience firsthand how financial bubbles form and collapse. You'll trade alongside AI-driven Value Traders and Momentum Traders as the market cycles through Minsky's five stages: Displacement, Boom, Euphoria, Distress, and Panic.

The game demonstrates why stability breeds instability, and how even transformative technologies like AI can fuel speculative bubbles that eventually crash.

## Quick Start (Play Now!)

The easiest way to play is with the HTML version:

1. **Download** [tb2tf-app.html](tb2tf-app.html) to your local drive
2. **Double-click** the file to open it in your browser
3. **Start playing!** No installation required.

The HTML file uses CDNs (Content Delivery Networks) to load required libraries from the internet, so it works as a standalone file that you can open directly in any modern web browser.

> **Note:** The game requires an internet connection to load the external libraries (React, Recharts, etc.) from CDNs.

## File Overview

This repository contains multiple versions of the game:

- **[tb2tf-app.html](tb2tf-app.html)** - Standalone HTML version, ready to play immediately
- **[tb2tf-app.jsx](tb2tf-app.jsx)** - React source file (JSX = JavaScript XML) with the same game logic
- **[minsky_ai_bubble_overview.md](minsky_ai_bubble_overview.md)** - Detailed explanation of the economic theory and mathematical models behind the game

### HTML vs JSX

- **HTML file:** Uses CDNs to load libraries over the internet. Just save and open in your browser - no setup needed.
- **JSX file:** Requires Node.js and a build process. This is the standard React development format for those who want to modify or extend the code.

## GitHub Pages (Coming Soon)

While the game is fully functional, GitHub Pages hosting is not yet configured. For now, please download the HTML file to play locally. Setting up GitHub Pages would allow you to play directly from your browser without downloading.

## Theory & Background

The game is based on **Hyman Minsky's Financial Instability Hypothesis**, which argues that financial systems are inherently unstable because periods of stability encourage excessive risk-taking.

Read the full theory breakdown in [minsky_ai_bubble_overview.md](minsky_ai_bubble_overview.md), which covers:

- The three types of finance: Hedge, Speculative, and Ponzi
- The five stages of a Minsky bubble
- Mathematical models of Value vs Momentum trading
- Why the 2025 AI boom exhibits classic bubble characteristics

## How to Play (JSX Development Version)

If you want to work with the React/JSX source code:

1. **Install Node.js** (if not already installed)
2. **Set up a React development environment** (e.g., Create React App, Vite, etc.)
3. **Copy the JSX code** from [tb2tf-app.jsx](tb2tf-app.jsx) into your React project
4. **Install dependencies:**
   ```bash
   npm install react recharts
   ```
5. **Run your development server**

## Game Mechanics

- **Three Stock Types:** Growth, Mediocre, and Fraud stocks with different earnings trajectories
- **Two AI Traders:** Value Traders (anchored to P/E ratios) vs Momentum Traders (chasing trends)
- **Market Phases:** Watch as the market cycles through boom, euphoria, and crash
- **Your Strategy:** Decide when to buy, hold, or sell as you compete against the AI agents

## License

This project is open source. Feel free to learn from it, modify it, and share it.

## Credits

Created to illustrate economic theory through interactive simulation. Inspired by the work of Hyman Minsky and the ongoing discussions about AI infrastructure valuations.

---

**Play responsibly. This is a simulation for educational purposes - not financial advice!**
