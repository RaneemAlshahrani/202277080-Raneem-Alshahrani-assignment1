
# AI Usage Report

## Overview
This report documents the use of AI tools during the development of a personal portfolio website. AI assistance supported front-end development, code optimization, debugging, accessibility improvements, and UI/UX enhancements. The tools were used as learning aids and code reviewers to improve code quality and understanding of modern web development practices.

## AI Tools Used
- **ChatGPT**:
[Debugging HTML, CSS, and JavaScript, Designing responsive layouts (hero section, navigation, mobile menu), 
Implementing light/dark mode and font-size toggles, Improving UI/UX consistency]

- **Cloud AI**: [CSS optimization and redundancy removal, Adding detailed comments to improve readability,
Identifying duplicated and conflicting CSS rules, Fixing dark mode compatibility issues]

## Features Developed with AI Assistance
- **Dark Mode Implementation**:
- Description: Implemented a full light/dark theme toggle with system preference detection.
- AI’s Role:
Fixed visibility issues for dark-colored icons (e.g., GitHub icon) in dark mode
Suggested CSS filter-based icon inversion using a reusable dark-invert class
Implemented theme persistence using localStorage
- **Responsive Mobile Navigation Menu**: 
- Description: Created a hamburger menu for mobile devices with a backdrop overlay.
- AI’s Role:
Identified duplicated and conflicting menu CSS definitions
Refactored positioning logic for reliable centering
Implemented open/close logic with JavaScript
- **Scroll Reveal Animations**:
- Description: Added fade-in animations to sections as they appear while scrolling.
- AI’s Role:
Recommended IntersectionObserver for efficient scroll detection
Removed duplicated reveal implementations
Added support for prefers-reduced-motion for accessibility

## Learning Outcomes
- **CSS Concepts Learned**:

- CSS Custom Properties (Variables)
Learned how to use variables for theming, spacing, and consistent styling across light and dark modes.

- Modern Layout Techniques
Gained experience using Flexbox and Grid appropriately for different layout needs.

- Accessibility Best Practices
Learned to respect user preferences such as prefers-reduced-motion, ensure keyboard navigation, and maintain proper color contrast.

- **JavaScript Concepts Learned**:

- DOM Manipulation & Event Handling
Improved understanding of event listeners for UI controls such as theme toggles, font size toggles, and mobile menus.

- Browser APIs
Learned to use localStorage, matchMedia, and IntersectionObserver effectively.

## Code Examples

- **Dark Mode Icon Fix (CSS)**:
```
:root[data-theme="dark"] img.dark-invert{
  filter: invert(1) hue-rotate(180deg) contrast(1.05);
}
```
- **Theme Toggle with Persistence (JavaScript)**:
```
function applyTheme(theme) {
  document.documentElement.setAttribute("data-theme", theme);
  localStorage.setItem("theme", theme);
}
```
- **Scroll Reveal Implementation (JavaScript)**:

```
const observer = new IntersectionObserver((entries, obs) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("show");
      obs.unobserve(entry.target);
    }
  });
});

```

## Challenges & Solutions

- **Challenge 1**: Dark Icons Invisible in Dark Mode
- Problem: Black icons disappeared on dark backgrounds.
- Solution: AI recommended using CSS filters applied selectively via a dark-invert class.

- **Challenge 2**: Mobile Menu Not Closing Properly
- Problem: Menu remained visible or conflicted with desktop layout.
- Solution: AI identified duplicated CSS and missing event handlers, leading to a clean, single-source implementation.

## Acknowledgments
This project was developed with assistance from:
- ChatGPT (OpenAI) for debugging, explanations, and UI/UX guidance
- Claude AI (Anthropic) for in-depth code review, optimization, and accessibility improvements
All AI-generated suggestions were reviewed, tested, and adapted to meet the project’s requirements.

## Conclusion
AI tools significantly enhanced my learning and development process by providing real-time feedback, debugging assistance, and guidance on best practices. Instead of replacing learning, AI supported deeper understanding of front-end development concepts and enabled me to build a more polished, accessible, and maintainable portfolio website.