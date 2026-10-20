# Hypermedia Project - Part 1: Curriculum Vitae Website

**Author:** Àlex Rodríguez Artells
**Degree:** Grau en Enginyeria Informàtica (GEINF)
**Live Site:** [https://oloxx.github.io/hypermedia-cv/](https://oloxx.github.io/hypermedia-cv/)
**Figma Project Link:** [Figma Design](https://www.figma.com/design/ciIsrRkTb90COdrX5sBpSE/Hypermedia-Project?node-id=0-1&t=vMILuhZtITJT3J6N-1)

---

## 1. Project Overview & Framework Justification

This project comprises the design, architectural analysis, and implementation of an online **Curriculum Vitae Website** for **Àlex Rodríguez Artells**, a **FullStack Web Developer** based in Vallromanes (Barcelona) and Girona. The objective of this single-page static website is to present professional experience, academic background, technical skills, languages, and contact channels in an structured format.

### Technology Stack & Justification

This project combines semantic HTML with **Pico CSS** and a lightweight custom CSS stylesheet:

| Technology | Purpose & Justification |
| :--- | :--- |
| **HTML** | Structured with semantic landmark tags (`<header>`, `<main>`, `<article>`, `<aside>`, `<footer>`, `<hgroup>`) to maximize accessibility and screen reader compatibility. |
| **Pico CSS** | Selected over heavyweight frameworks because Pico is **class-light and semantic-first**: it styles native HTML tags directly without cluttering the markup with presentational classes. It provides instant dark mode support, typography scales, accessible contrast, and card primitives with zero runtime JavaScript. |
| **Custom CSS** | Complementary stylesheet for predictable layout control, defining the desktop two-column Flexbox arrangement, vertical timeline tracks, company/school logos, and skill badges. |
| **Flexbox Layout** | Applied for the two-column layout (`.cv-layout`), putting into practice the techniques taught in class. |
| **Responsive Design** | Employs fluid viewport behavior and an `@media (min-width: 820px)` breakpoint to guarantee responsiveness across mobile, tablet, and desktop viewports. |

---

## 2. Project Analysis

### 2.1 User Profile (User Persona)

To ensure the website fulfills its purpose, the primary audience was characterized through a User Persona representing industry hiring managers, lead developers, and technical recruiters seeking full-stack engineers.

```
┌────────────────────────────────────────────────────────────────────────┐
│ USER PERSONA: MARC TORRES                                              │
│ • Role: Engineering Manager / Lead Full-Stack Architect                │
│ • Company: Tech Scale-Up & Software Studio (Barcelona / Remote)        │
│ • Age: 36 years old                                                    │
│ • Environment: MacBook Pro (Desktop) + iPhone 15                       │
│ • Key Behavior: Reviews 30–50 candidate profiles per week;             │
│   spends an average of 45–60 seconds on initial candidate screening.   │
└────────────────────────────────────────────────────────────────────────┘
```

#### Goals & Expectations:

* **Immediate Clarity:** Rapidly identify the candidate's core stack-specifically proficiency in modern technologies like **Python**, **TypeScript**, and backend architectures.
* **Verification of Real-World Experience:** Validate the candidate's track record across previous roles, distinguishing between academic exercises and applied company experience.
* **Clean Code & Readability:** Read the information without visual distraction, decorative clutter, or heavy scripts that slow down page rendering.
* **Frictionless Contact:** Quickly locate direct communication pathways (Email, LinkedIn, GitHub).

---

### 2.2 Information Architecture

The Information Architecture is organized as a structured **single-page static website** utilizing a clean **two-column Flexbox layout**, modeled directly after modern professional developer resumes and hypermedia design principles. Unnecessary navigational bars and multi-level menus have been omitted to allow technical recruiters and engineering managers to evaluate core competencies and career milestones immediately upon arrival.

The page is systematically divided into semantic landmark zones:

1. **Header (`<header>`):** Positioned at the top of the document, containing the candidate's circular profile photo (90×90px avatar with cyan accent border), full name (*Àlex Rodríguez Artells*), and professional headline (*FullStack Web Developer*), establishing clear personal branding and immediate identification.
2. **Main Content Area (`<div id="main-content">`):** Structured via Flexbox into two distinct functional columns:
   * **Primary Column (`<div id="primary-column">`):** Holds the greatest visual priority (flex factor of 1.8). It contains the personal biographical summary in the About section, the chronological professional journey in Work Experience (featuring *TechDocs Studio*, *Biel.ai*, and *Berrly* with respective company logos, responsibilities, and achievements), and formal academic degrees in Education (*Universitat de Girona*, *Institut Carles Vallbona*, and *Institut Vilanova del Vallès* with institutional emblems).
   * **Secondary Column (`<aside id="secondary-column">`):** Operates as a focused sidebar (flex factor of 1). It organizes technical competencies into categorized badge lists (*Core Aptitudes* like Python and TypeScript, *Web & Programming*, and *Databases & Tools*), spoken language proficiencies (*Catalan*, *Spanish*, *English*), and direct communication channels (*Email*, *LinkedIn*, and *GitHub*).
3. **Footer (`<footer>`):** Closes the page with formal copyright notices, university affiliation, and academic course attribution.

---

### 2.3 Visual Design

The visual design follows a modern dark theme interface, balancing high typographic readability, accessible color contrast, and refined component hierarchy without relying on heavy external graphics or runtime JavaScript. The design leverages **Pico CSS** as an accessible foundation, complemented by custom CSS.

Key visual design choices include:

* **Color Palette & Contrast:** Dark canvas mode (`data-theme="dark"`) minimizes eye strain. Cyan (`#38bdf8`) serves as the primary accent color for active elements, links, and high-priority skill badges. Lavender-indigo (`#818cf8`) is applied consistently to organization and institutional names to create a distinct secondary layer of semantic meaning. Card containers utilize elevated surface backgrounds with subtle boundary borders for structured separation.
* **Visual Assets & Branding:** The candidate's circular profile picture provides immediate personal recognition, styled with a solid cyan border and drop shadow. Organization and educational logos (44×44px) are embedded alongside timeline items in clean white rounded tiles with subtle borders, ensuring high visual contrast and brand authenticity on dark backgrounds.
* **Typography & Micro-Interactions:** Native system font stacks ensure zero-latency rendering and maximum sharpness across all operating systems. Interactive elements, including badges and navigation links, feature smooth border-color and color transitions on hover, deliberately omitting disruptive movement or transform animations to ensure a stable, distraction-free reading experience.
* **Responsive Layout:** The two-column Flexbox structure effortlessly collapses into an intuitive single-column linear flow on mobile screens (<820px).

---

## 3. Repository Structure

```
hypermedia-cv/
├── index.html          # Main HTML single-page website
├── style.css           # Custom CSS stylesheet
├── assets/             # Static media assets
│   └── img/
│       ├── profile.jpg # Profile avatar photo
│       └── logos/      # Company and educational institution logos
│           ├── berrly.png
│           ├── biel.png
│           ├── techdocs.png
│           ├── udg.png
│           ├── vallbona.png
│           └── vilanova.png
└── README.md           # Project documentation
```
