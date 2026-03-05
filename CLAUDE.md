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

## Current Version
v12.5

## App Details (deako-floorplan-demo.html)
- Dark-themed UI (`#0d1117` background)
- Floor plan image hosted at `https://i.ibb.co/Kp40nS53/Brown-Haven-Preview.webp`
- 14 rooms defined with SVG overlay hotspots (x/y/w/h in viewBox % units)
- Click a room = toggle on/off; long-press (400ms) = open dimmer popup
- 5 scenes: Good Morning, Arrive Home, Dinner, Wind Down, Vacation Mode (button order)
- Brightness state stored in `levels` object (0 = off, 1–100 = dim level)
- Room glow/fill rendered via inline SVG with radial gradients and filters
- Floor plan image brightness/saturation updates dynamically based on average light level
- In-room SVG brightness slider appears at bottom of each lit room (click to latch, click to lock)
- % badge shown at top of each lit room
- Per-room timer settings persisted to localStorage (`bhRoomTimers`)
- Vacation Mode uses `steps` array (timed sequence) instead of `rooms`; all other scenes use `rooms`
- 3 interactive Deako switch images (SVG `<image>` elements): foyer, owner's suite, mud room — each toggles all-off / all-on alternately

## Rooms
dining, kitchen, great, owners, owic, obath, foyer, strg, pantry, mudroom, laundry, powder, porch, deck

## Deako Switch Positions (SVG % coordinates)
- Foyer: x:43.8, y:74.8
- Owner's Suite: x:64.5, y:28.2
- Mud Room: x:19.0, y:60.0
const ROOMS = [
  {id:"dining", label:"Dining", x:11.79, y:59.32, w:12.38, h:8.46},
  {id:"kitchen", label:"Kitchen", x:12.50, y:40.60, w:25.00, h:17.51},
  {id:"great", label:"Great Room", x:38.33, y:20.88, w:26.03, h:37.10},
  {id:"owners", label:"Owner's Suite", x:65.60, y:20.88, w:24.59, h:27.89},
  {id:"owic", label:"O. WIC", x:65.50, y:50.06, w:8.47, h:22.70},
  {id:"obath", label:"O. Bath", x:74.69, y:50.19, w:15.70, h:22.44},
  {id:"foyer", label:"Foyer", x:38.75, y:58.71, w:7.35, h:17.69},
  {id:"strg", label:"Staircase", x:46.59, y:58.63, w:18.08, h:18.15},
  {id:"pantry", label:"Pantry", x:25.00, y:59.14, w:8.57, h:8.82},
  {id:"mudroom", label:"Mud Room", x:5.48, y:59.40, w:18.80, h:8.43},
  {id:"laundry", label:"Laundry", x:13.02, y:69.00, w:11.46, h:11.93},
  {id:"powder", label:"Powder", x:25.31, y:68.87, w:8.26, h:12.06},
  {id:"porch", label:"Front Porch", x:37.91, y:77.82, w:26.97, h:9.47},
  {id:"deck", label:"Rear Deck", x:38.12, y:4.67, w:26.96, h:14.79}
];
are you there?

ls
cd brownhaven
