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

*   **`Header.svelte`**: A navigation bar that is fixed to the top of the page and smoothly scrolls to the different sections of the portfolio. It includes social media links (GitHub, LinkedIn) with icons.
*   **`Hero.svelte`**: A prominent "hero" section at the top of the page with a welcoming message, his name, title, and social media links (GitHub, LinkedIn) with icons.
*   **`About.svelte`**: A section detailing his personal information, specializations, and a brief bio.
*   **`Experience.svelte`**: A timeline-style component to showcase his professional experience.
*   **`Projects.svelte`**: A grid or carousel of cards to display his live deployments and GitHub repositories, with links to each.
*   **`Certifications.svelte`**: A section to list his certifications and licenses, possibly with logos of the issuing institutions.
*   **`Volunteering.svelte`**: A section to highlight his volunteering experience.
*   **`Footer.svelte`**: A footer with contact information, copyright details, and social media links (GitHub, LinkedIn) with icons.
*   **`App.svelte`**: The main application component that will assemble all the other components.

## 3. Plan for Current Change: Enhance Header, Footer, and Hero

The goal is to enhance the `Header.svelte`, `Footer.svelte`, and `Hero.svelte` components by adding social media icons and improving the overall structure and styling.

*   **Step 1:** Modify `Header.svelte` to include GitHub and LinkedIn icons. The icons will be implemented as inline SVGs for better control and performance. The layout will be adjusted to accommodate the new icons, placing them on the right side of the navigation links.
*   **Step 2:** Add non-inline CSS to `Header.svelte` for styling the icons, including hover effects to improve user interaction.
*   **Step 3:** Modify `Footer.svelte` to replace the text-based social media links with SVG icons for GitHub and LinkedIn, matching the style of the header.
*   **Step 4:** Add non-inline CSS to `Footer.svelte` to style the icons and ensure a consistent look and feel with the rest of the application.
*   **Step 5:** Modify `Hero.svelte` to replace the text-based social media links with SVG icons for GitHub and LinkedIn.
*   **Step 6:** Add scoped CSS to `Hero.svelte` to style the new icons and ensure they are visually consistent with the rest of the site.
*   **Step 7:** Update the `blueprint.md` file to reflect these changes.
