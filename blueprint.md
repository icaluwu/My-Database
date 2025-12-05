# Blueprint: Personal Portfolio Website for Teuku Vaickal Rizki Irdian (IcalUwU)

## 1. Overview

This document outlines the plan for creating a personal portfolio website for Teuku Vaickal Rizki Irdian (IcalUwU). The website will be a single-page application built with Svelte and Vite, showcasing his skills, experience, projects, and certifications. The design will be modern, responsive, and visually appealing, following the aesthetic guidelines defined in the project's `GEMINI.md` file.

## 2. Project Outline

### 2.1. Design & Styling

*   **Aesthetics:** The site will have a clean, modern aesthetic with a focus on readability and visual hierarchy.
*   **Layout:** A single-page, scrolling layout with clear sections for each content category. It will be fully responsive for mobile and desktop viewing.
*   **Color Palette:** A professional color scheme will be chosen, likely incorporating blues, dark grays, and white, with accent colors to draw attention to key elements.
*   **Typography:** We will use a clean, sans-serif font like 'Inter' or 'Poppins' for readability. Font sizes and weights will be used to create a clear visual hierarchy.
*   **Iconography:** Icons will be used to visually represent different sections, skills, and contact information.
*   **Effects:** Subtle animations and hover effects will be used to create a more dynamic and engaging user experience.

### 2.2. Features & Components

The application will be structured into the following components:

*   **`Header.svelte`**: A navigation bar that is fixed to the top of the page and smoothly scrolls to the different sections of the portfolio.
*   **`Hero.svelte`**: A prominent "hero" section at the top of the page with a welcoming message, his name, title, and social media/contact links.
*   **`About.svelte`**: A section detailing his personal information, specializations, and a brief bio.
*   **`Experience.svelte`**: A timeline-style component to showcase his professional experience.
*   **`Projects.svelte`**: A grid or carousel of cards to display his live deployments and GitHub repositories, with links to each.
*   **`Certifications.svelte`**: A section to list his certifications and licenses, possibly with logos of the issuing institutions.
*   **`Volunteering.svelte`**: A section to highlight his volunteering experience.
*   **`Footer.svelte`**: A footer with contact information and copyright details.
*   **`App.svelte`**: The main application component that will assemble all the other components.

## 3. Current Task: Initial Scaffolding

The current plan is to begin by scaffolding the basic structure of the application.

*   **Step 1:** Create the `blueprint.md` file to document the project plan.
*   **Step 2:** Clean up the existing `src` directory to remove the default boilerplate code.
*   **Step 3:** Create the new component files within the `src/lib` directory.
*   **Step 4:** Update `App.svelte` to import and render the new components.
*   **Step 5:** Add basic styling to `app.css` to set the overall look and feel.
