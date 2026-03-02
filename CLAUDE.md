# Brownhaven Project

## Overview
Interactive smart lighting demo for a Brownhaven home floor plan, built for Deako Smart Lighting. Single-page vanilla HTML/CSS/JS app — no build tools or dependencies.

## Paths
- **Project root:** `C:/Users/slypi/ClaudeProjects/Brownhaven/`
- **GitHub repo:** https://github.com/snappahands/brownhaven

## Files
- `index.html` — main entry point (placeholder)
- `deako-floorplan-demo.html` — the main Deako smart lighting demo app
- `style.css` — shared stylesheet
- `script.js` — shared script

## Git & GitHub
- **GitHub user:** snappahands (slypig@gmail.com)
- **Remote:** https://github.com/snappahands/brownhaven.git
- **Default branch:** master
- GitHub CLI (`gh`) is installed at `C:/Program Files/GitHub CLI/` — already added to bash PATH via `~/.bashrc`, so git/gh commands work directly without using PowerShell
- **GitHub Pages:** https://snappahands.github.io/brownhaven/deako-floorplan-demo.html

## Workflow
- After every code change:
  1. Increment the version number in the status bar (`v1.0`, `v1.1`, etc.)
  2. Commit and push to GitHub
  3. Tell the user the new version number and share the live link: https://snappahands.github.io/brownhaven/deako-floorplan-demo.html

## App Details (deako-floorplan-demo.html)
- Dark-themed UI (`#0d1117` background)
- Floor plan image hosted at `https://i.ibb.co/Kp40nS53/Brown-Haven-Preview.webp`
- 14 rooms defined with SVG overlay hotspots (x/y/w/h in viewBox % units)
- Click a room = toggle on/off; long-press (400ms) = open dimmer popup
- 5 scenes: Arrive Home, Dinner, Wind Down, Vacation Mode, Good Morning
- Brightness state stored in `levels` object (0 = off, 1–100 = dim level)
- Room glow/fill rendered via inline SVG with radial gradients and filters
- Floor plan image brightness/saturation updates dynamically based on average light level

## Rooms
dining, kitchen, great, owners, owic, obath, foyer, strg, pantry, mudroom, laundry, powder, porch, deck
