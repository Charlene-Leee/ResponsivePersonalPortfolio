# Responsive Portfolio Website - Project Details

## 1. Project Overview

This project is a functionally complete, responsive personal portfolio website. It is designed to showcase an individual's skills, qualifications, services offered, a gallery of work, client testimonials, and contact information. The website is a single-page application with smooth scrolling navigation and multiple interactive sections.

## 2. Technology Stack

*   **Core Languages**:
    *   HTML5
    *   CSS3
    *   JavaScript (ES6+)
*   **CSS Features**:
    *   CSS Variables (Custom Properties) for theming and maintainability.
    *   Flexbox and CSS Grid for layout.
    *   Media Queries for responsive design across various devices.
*   **JavaScript Libraries**:
    *   **Swiper.js**: Used for creating interactive and touch-friendly carousels in the "Portfolio" and "Testimonials" sections.
*   **Iconography**:
    *   **Unicons**: A library of vector icons used throughout the user interface, loaded via CDN.
*   **Typography**:
    *   **Google Fonts**: Utilizes the "Poppins" font family.

## 3. Project Structure

The project follows a standard static website structure:

*   **`index.html`**: The main and only HTML file, serving as the entry point for this single-page application. It contains the markup for all sections of the portfolio.
*   **`assets/`**: A directory containing all static resources.
    *   **`css/`**:
        *   `styles.css`: The primary custom stylesheet containing all project-specific styles, including responsive rules and theme definitions.
        *   `swiper-bundle.min.css`: The official CSS file for the Swiper.js library.
    *   **`js/`**:
        *   `main.js`: The primary custom JavaScript file that handles all client-side interactivity, including navigation, modals, carousels, and theme switching.
        *   `swiper-bundle.min.js`: The official JavaScript file for the Swiper.js library.
    *   **`img/`**: Contains all images used in the project, such as the profile picture, "About Me" image, portfolio item screenshots, project showcase image, and testimonial avatars.
    *   **`pdf/`**: Stores PDF documents, primarily intended for the downloadable CV (e.g., `Alexa-Cv.pdf`).
*   **`README.md`**: The original brief readme file.
*   **`PROJECT_DETAILS.md`**: This file, providing a more comprehensive overview.

## 4. Detailed Features

The website incorporates a variety of modern web features:

*   **Responsive Design**: Adapts seamlessly to different screen sizes (desktops, tablets, and mobile phones) ensuring a consistent user experience.
*   **Theme Switching (Dark/Light Mode)**:
    *   Users can toggle between a light and a dark theme.
    *   The selected theme preference is saved in the browser's `localStorage` and applied on subsequent visits.
*   **Navigation System**:
    *   A persistent navigation bar (fixed to the top on desktop, bottom on mobile).
    *   Smooth scrolling to corresponding sections when navigation links are clicked.
    *   **Scrollspy**: Automatically highlights the active navigation link based on the section currently visible in the viewport.
    *   The header background dynamically changes on scroll for better visual feedback.
*   **Main Sections & Functionality**:
    *   **Home**: Introduction with name, title, brief description, social media links, and a profile image displayed within an SVG blob.
    *   **About**: Detailed personal introduction, key experience metrics (e.g., years of experience, projects completed), and a button to download the CV.
    *   **Skills**: An accordion-style display of different skill sets (e.g., Frontend, Backend, Design) with progress bars indicating proficiency levels.
    *   **Qualification**: A tabbed interface to switch between "Education" and "Work" timelines, showcasing chronological milestones.
    *   **Services**: Displays offered services. Each service can be clicked to open a modal window with more detailed information (e.g., list of what the service includes).
    *   **Portfolio**: Showcases recent work using a Swiper.js carousel. Each portfolio item includes an image, title, description, and a demo link.
    *   **Project in Mind**: A "call to action" section encouraging visitors to get in touch for new projects.
    *   **Testimonials**: Displays client feedback using another Swiper.js carousel. Each testimonial includes an avatar, name, client status, star rating, and a quote.
    *   **Contact Me**: Provides contact information (phone, email, location) and a functional contact form layout (note: form submission backend is not implemented in this frontend-only project).
*   **Scroll-to-Top Button**: A button that appears when the user scrolls down the page, allowing for quick navigation back to the top.

## 5. How to Run / Local Development

To run this project locally:

1.  Ensure you have a modern web browser (e.g., Chrome, Firefox, Edge, Safari).
2.  Clone or download the project files to your local machine.
3.  Navigate to the project's root directory.
4.  Simply open the `index.html` file in your web browser.

No special build steps or local server (beyond what your browser might use for certain features like `localStorage` if run strictly via `file:///` protocol, though usually it works fine) is required for basic viewing and interaction.

## 6. Customization Guide

This portfolio is designed to be easily personalized:

*   **Text Content**: Most text (your name, job title, descriptions, skill details, project information, contact details, etc.) can be directly edited within the `index.html` file in the respective sections.
*   **Images**:
    *   **Profile Image**: Replace `assets/img/perfil.png`.
    *   **About Image**: Replace `assets/img/about.jpg`.
    *   **Portfolio Item Images**: Replace `assets/img/portfolio1.jpg`, `portfolio2.jpg`, etc.
    *   **Project Showcase Image**: Replace `assets/img/project.png`.
    *   **Testimonial Avatars**: Replace `assets/img/testimonial1.jpg`, `testimonial2.jpg`, etc.
    *   When replacing images, try to use images of similar dimensions to maintain the layout. If you change filenames or paths, update the corresponding `src` attributes in `index.html`.
*   **CV / Resume**:
    *   Replace the file `assets/pdf/Alexa-Cv.pdf` (or the name used in your project if different) with your own PDF resume. Ensure the link in the "About" section (`<a download="" href="assets/pdf/Your-CV-Name.pdf" ...>`) points to your file.
*   **Links**:
    *   **Social Media**: Update the `href` attributes for social media icons in the "Home" section and "Footer".
    *   **Portfolio Demo Links**: Update the `href` attributes for the "Demo" buttons in the "Portfolio" section.
    *   **Contact Information**: Modify phone number, email address, and location details in the "Contact Me" section.
    *   **Footer Links**: Adjust navigation links in the footer if necessary.
*   **Color Scheme**:
    *   The primary color scheme can be easily changed by modifying the `--hue-color` CSS variable at the top of `assets/css/styles.css`.
    *   Dark theme colors are also defined using CSS variables under the `body.dark-theme` rule in `assets/css/styles.css` and can be adjusted there.
*   **Skill Percentages**:
    *   The visual percentage for skill bars in the "Skills" section is controlled by inline styles on `<span>` elements (e.g., `class="skills__percentage skills__html"` where `.skills__html` has a `width` property in `styles.css`) and the text percentage is in a separate `<span>`. Update both the CSS width (e.g., in `.skills__html { width: 90%; }`) and the corresponding text in `index.html` (`<span class="skills__number">90%</span>`).

By modifying these elements, you can effectively tailor the website to your personal brand and information. 
