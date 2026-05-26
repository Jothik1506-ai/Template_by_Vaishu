# 🌌 AIVA Portfolio — Premium Developer & Designer Showcase

Welcome to **AIVA Portfolio**, an immersive, high-end, dark-themed portfolio website designed for digital creators, designers, and developers. Featuring sleek glassmorphism, dynamic canvas background effects, vibrant accent gradients, and micro-interactions, this project is built to make a stunning first impression.

---

## ✨ Features & Sections

### 1. 🧭 Interactive Navigation Bar
* **Glassmorphic Navigation Capsule**: A floating navigation bar that utilizes backdrop blurs and subtle borders.
* **Micro-Interactions**: Hover effects on links (Home, Work, Resume) and a dynamic **"Say hi"** call-to-action button featuring responsive gradients.
* **Responsive Logo**: A custom circular logo badge (`JA`) with premium accent transitions.

### 2. 🌀 Immersive Hero Header
* **Interactive Backdrop Canvas**: A fixed canvas element rendering high-performance background particles.
* **Vite-Powered Video/Image Background**: A looping galaxy/nebula video combined with space mapping overlays.
* **The "AIVA" Pulse Ring**: Nested rotating orbital borders (spinning in opposite directions) circling the glowing core **AIVA** branding text.
* **Dynamic Introduction**: Beautiful typographic hierarchy displaying the creator's role, locations, and interactive CTA buttons (*"See Works"*, *"Reach out..."*).

### 3. 🎨 Selected Work / Featured Projects Grid
* A structured grid of case studies featuring smooth scale-ups, backdrop blur changes, and interactive slide-in descriptions upon hover:
  * 🚗 **Automotive Motion**: Interactive 3D vehicle configurator (7/12 grid-span).
  * 🏢 **Urban Architecture**: Immersive VR city tour (5/12 grid-span).
  * 🧠 **Human Perspective**: AI-driven emotion analysis (5/12 grid-span).
  * 🏷️ **Brand Identity**: Generative brand design system (7/12 grid-span).

### 4. ✍️ Journal / Recent Thoughts
* A list of clean, list-style articles showcasing reflections on design, AI, and motion technology.
* Hover states trigger sliding gradient overlays, glowing bullets, and custom animated arrow vectors.

### 5. 🎢 Visual Playground (Explorations)
* A high-impact showcase utilizing card layouts and rotated grid capsules. 
* Designed to exhibit experiments, 3D renders, and digital art with smooth parallax-like transitions.

### 6. 📊 Accomplishment Metrics
* Clean showcase exhibiting key statistics (e.g. *Years of Experience*, *Projects Completed*, *Client Satisfaction Rates*) with text-gradient overlays.

### 7. 📬 Premium Contact Form & Footer
* A glassmorphic form block with floating borders, input glow, and a custom background container.
* Integrated availability indicator displaying a green pulsing badge (*"Available for projects"*).
* Clean layout for social links (Twitter, LinkedIn, Dribbble, GitHub) and copyright details.

---

## 🛠️ Technology Stack
* **Framework**: React & TypeScript
* **Build System**: Vite
* **Styling**: Tailwind CSS & Vanilla CSS (supporting modern OKLCH color palettes, custom `@layer` setups, and CSS variables)
* **Smooth Scrolling**: Lenis Scroll (Lenis-smooth custom classes applied on document level)
* **Graphics**: HTML5 Canvas & Custom SVGs

---

## 📂 Current Directory Structure

The project currently contains a high-fidelity local snapshot of the compiled frontend:

```bash
aivapro/
├── README.md                 # Project documentation (this file)
├── templateweb.html          # High-fidelity static HTML build of the website
└── templateweb_files/        # Extracted client assets & source scripts
    ├── client                # Saved Vite client & Hot Module Replacement module
    └── main.tsx              # React entry point script
```

---

## 🚀 How to Run the Static Build
To quickly serve and inspect the static snapshot, you can use any static server. For example:

### Using Python
Run this command in the project directory:
```bash
python -m http.server 8000
```
Then visit: `http://localhost:8000/templateweb.html`

### Using Node.js (via `serve`)
```bash
npx serve ./
```
Then visit: `http://localhost:3000/templateweb.html`

---

## 🔧 Reconstructing as a Standard React Project

To reconstruct this snapshot back into an editable React + Vite developer directory, follow these steps:

1. **Initialize the Project**:
   ```bash
   npm create vite@latest aiva-portfolio -- --template react-ts
   cd aiva-portfolio
   npm install
   ```

2. **Install Styling and Scroll Dependencies**:
   ```bash
   npm install tailwindcss lenis lucide-react
   ```

3. **Extract Components**:
   * Migrate the CSS rules inside the `<style>` block in `templateweb.html` into your project's `src/index.css`.
   * Separate sections of the HTML inside `<body>` into modular React components inside a `src/components/` directory:
     * `Navbar.tsx`
     * `Hero.tsx`
     * `Projects.tsx`
     * `Journal.tsx`
     * `Playground.tsx`
     * `Contact.tsx`
   * Implement the background HTML5 canvas particle logic in a clean custom React Hook or helper file.
