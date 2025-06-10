# GazeScore

**As a musician — PAGE TURNING SUCKS!**  
You miss your turn, or flip too many — it’s a mess.  
That’s where GazeScore comes in — keeping your next line in sight, so you’re always ready to play!

---

## Inspiration

One of our team members, Manit, has been a classical pianist for over 10 years. Page turning has always been a frustrating challenge. While recording a 40-minute piano performance this year, he lost two incredible takes — all because of bad page turns. A small mistake, big consequences.

When brainstorming for the hackathon, we asked:  
**What would the ideal solution look like?**  
Simple: seamless, natural page turns that always show the next line right when you need it.

That's what inspired us to create GazeScore.

---

## What It Does

The GazeScore web app has two main sections:

- **Setup**: Upload your sheet music as a PDF and complete a quick eye-tracking calibration.
- **Perform**: Play your piece with intelligently split sheet music and gaze-based page turning.

### How it works

1. The sheet music is split into top and bottom halves.
2. As the musician reads the top half, nothing changes.
3. When they focus on the bottom half for ~3 seconds, the top half of the next page is preloaded.
4. Once they shift to the new top half, the bottom half is preloaded.
5. This loop continues seamlessly through the entire performance.

No delays. No buttons. Just music.

---

## How We Built It

**Tech Stack**: React + Vite  
We integrated several libraries to handle PDF rendering, eye tracking, and dynamic logic.

### Development Process

- Mapped the entire project on a whiteboard before coding.
- Brainstormed functionality and future features.
- Delegated tasks based on strengths for parallel progress.

### PDF Upload & Processing

- Used `pdf.js` and `pdf-lib` to split music pages into top and bottom halves for performance-friendly rendering.

### Eye Tracking Calibration

- Integrated `WebGazer.js` for real-time gaze tracking.
- Built a custom calibration process to ensure high accuracy across all screen points.

### Smart Page-Turning Logic

- Split screen into top/bottom halves.
- Tracked how long the user focuses on each half.
- Preloaded the next half after a 3-second confirmation.
- Managed transitions using booleans to keep page turns smooth and reliable.

---

## Challenges We Faced

- PDF rendering issues and worker debugging.
- Built custom logic for page flipping — no existing solution matched our needs.
- Converted existing C# PDF logic into JavaScript.
- CSS integration conflicts between components.
- Calibrating WebGazer to accurately detect gaze intent across screen zones.

---

## Accomplishments We're Proud Of

- Successfully integrated real-time eye tracking.
- Designed a clean and consistent UI.
- Wrote custom page-turning logic from scratch.
- Improved team collaboration and task division.
- Delivered a working MVP that solves a real-world problem for musicians.

---

## What We Learned

- How to build apps using React and Vite.
- Implementing eye-tracking with browser-based APIs.
- UI/UX design fundamentals for performance tools.
- Project management: breaking down large features into smaller, manageable tasks and integrating them into a complete product.

---

## What's Next for GazeScore

We’re excited to keep building. Here are the next steps on our roadmap:

- **Audio-Based Page Turning**: Use sound cues to supplement or replace gaze detection.
- **Improved Page-Turning Algorithms**: Shift from a fixed window to a sliding window approach.
- **User Accounts & Cloud Syncing**: Enable profiles, preferences, and sheet music to be saved via Firebase.
- **URL-to-PDF Conversion**: Convert online sheet music into PDFs directly in the app.
- **Premium Features**: Cloud storage, advanced customization, and monetization for long-term sustainability.

---

Thanks for checking out GazeScore.  
We believe technology should support musicians — not distract them.

Play more. Turn less.
