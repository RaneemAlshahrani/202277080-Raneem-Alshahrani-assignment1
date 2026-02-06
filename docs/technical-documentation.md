# Technical Documentation

## Overview

This project is a responsive personal portfolio website developed to showcase academic background, technical skills, and projects. The purpose of the system is to provide a clean, accessible, and modern web interface that adapts to different devices, supports light/dark mode, and demonstrates front-end development best practices.

### Scope

* Front-end only (HTML, CSS, JavaScript)
* No backend or database integration
* Optimized for desktop and mobile browsers

## Architecture

### System Design and Components

The system follows a static front-end architecture composed of:

* **HTML**: Semantic structure of the website
* **CSS**: Layout, theming (light/dark mode), animations, and responsiveness
* **JavaScript**: UI interactivity and state management

### Main Components

* Header & Navigation Bar
* Hero Section
* Projects Section
* Skills Section
* Contact Form
* Footer

### Data Flow

* User interactions (clicks, scrolls) trigger JavaScript events
* UI state (theme, font size) is stored in `localStorage`
* No external APIs or backend communication

## Installation

### Prerequisites

* A modern web browser (Chrome, Firefox, Edge, Safari)
* Optional: VS Code with Live Server extension for local development

### Setup Instructions

1. Download or clone the project files
2. Ensure the following folder structure:

```
assignment-1/
├── README.md
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── assets/
│   └── images/
├── docs/
│   ├── ai-usage-report.md
│   └── technical-documentation.md
└── .gitignore

```

3. Open `index.html` directly in a browser **or**
4. Run Live Server in VS Code for automatic reload

## Configuration

* No environment variables required
* Theme and font preferences are automatically saved in the browser

## Usage

### How to Use the Website

* Navigate using the top navigation bar
* Scroll to view different sections
* Use buttons in the navigation bar to:

  * Toggle Light/Dark Mode
  * Increase/Decrease Font Size
  * Open Mobile Menu (on small screens)

### Common Workflows

* **Viewing Projects**: Scroll to the Projects section
* **Changing Theme**: Click the moon/sun icon
* **Mobile Navigation**: Click ☰ on mobile view
* **Contacting**: Fill out the contact form to send an email

### Command-Line Usage

Not applicable — this is a client-side web application.

## API Reference

This project does not expose or consume external APIs.

### Internal JavaScript Functions (Examples)

* `applyTheme(theme)` – switches between light and dark modes
* `openMenu()` / `closeMenu()` – controls mobile menu visibility
* `IntersectionObserver` – triggers scroll-based animations

## Troubleshooting

### Common Issues

* **Issue**: Dark icons not visible in dark mode  
  **Solution**: Apply the `dark-invert` CSS class to black icons

* **Issue**: Mobile menu does not close  
  **Solution**: Ensure the `.hidden` class is applied correctly and JavaScript event listeners are active

* **Issue**: Theme or font size resets on refresh  
  **Solution**: Verify `localStorage` access is not blocked by the browser

## Contributing

### Contribution Guidelines

This project is currently a personal academic portfolio and not open for external contributions.

### Development Setup

* Modify HTML for content updates
* Update CSS variables for design changes
* Extend JavaScript for new UI features

## References

* zybook of the course
* w3schools Web Docs – HTML, CSS, JavaScript
* YouTube video

## Conclusion

This portfolio website demonstrates a structured front-end architecture, responsive design principles, and modern JavaScript techniques. The documentation ensures maintainability, clarity, and ease of future extension while serving as a technical reference for understanding the system.

## Next Steps

1. Review the documentation for clarity
2. Add screenshots for each major section
3. Document future enhancements (e.g., backend integration)
4. Keep documentation updated with new features
5. Validate accessibility improvements periodically
