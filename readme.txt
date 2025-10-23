# Digital Resume – Mattéo Binet

This project is a responsive digital resume built with **HTML, CSS**, and the **Materialize** framework.  
It was created to showcase professional experience, skills, and education in a modern, web-based format.

## Features

- Personal details and contact information
- Hero section with profile picture and headline
- About section
- Experience timeline
- Skills (development, systems, networking)
- Education and certifications
- Interests
- Contact form (static)

## File Structure

- `digitalresume.html` – main HTML page  
- `style.css` – custom styles and responsive design  
- `photo.jpg`, `photo_n2.jpg` – profile images  
- `readme.txt` – documentation  

## Technologies

- **HTML5 / CSS3**
- [Materialize](https://materializecss.com/) (via CDN)
- Lightweight JavaScript for scroll animations and mobile menu initialization

## Responsive Design

The layout automatically adapts to different screen sizes:

- **Mobile (≤ 640px)**  
  Centered title  
  Single-column layout, full-width buttons, centered cards and content.

- **Tablet (768–1023px)**  
  Full navigation menu displayed (like on desktop).  
  Hero section arranged in two columns (text and photo).  
  Adjusted spacing to keep content balanced.

- **Desktop (≥ 1024px)**  
  Standard navigation bar with logo on the left and menu on the right.  
  Wider grid layouts and larger profile image.

These behaviors are controlled with CSS `@media queries`.

## How It Works

- **Theme**: custom “neon glass” effect (`.neon-bg`, `.glass`, `.glass-deep`) using gradients and `backdrop-filter`.  
- **Typography**: adaptive text sizes with `clamp()` for smooth scaling.  
- **Layout**: `grid` and `flexbox` used to align hero section, skills, and timeline.  
- **Navigation**:  
  - Tablet → full menu  
  - Desktop → full menu with extended spacing  
- **Accessibility**: anchor links use `scroll-margin-top` to avoid being hidden behind the fixed navbar.

## Usage

Place all files in the same folder and open `digitalresume.html` in a modern browser.  
Tested with Chrome, Firefox, and Edge.  

To customize:
- Edit texts directly in `digitalresume.html`
- Replace images with personal visuals
- Adjust colors and effects in `style.css`

## Notes

- The contact form is static and not connected to a backend.  
  To enable submissions, integrate a service like Formspree, Netlify Forms, or a custom backend.  
