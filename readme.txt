Nexus - Modern Portfolio HTML Template Documentation

Thank you for purchasing the Nexus - Modern Portfolio HTML Template!
This document will guide you through the setup and customization process.

==============================
1. Template Overview
==============================

Nexus is a clean, modern, and responsive one-page HTML template designed specifically for creative freelancers, designers, developers, photographers, artists, and other professionals looking to showcase their work online.

It includes all the essential sections to present your profile, services, portfolio, testimonials, and contact information in a single, engaging page.

==============================
2. Included Files
==============================

The template package contains the following files and folders:

- index.html: The main HTML file containing the structure and content of the template.
- styles.css: The CSS file containing all the styling and layout rules for the template.
- script.js: The JavaScript file responsible for animations, interactivity (like the mobile menu toggle, scroll effects, portfolio filtering, testimonial slider, and preloader).
- images/ : A folder included to help you organize your image files.

==============================
3. Getting Started
==============================

To set up the template:

1.  **Download & Unzip:** Download the template package and unzip the files to a folder on your computer. You will see the `index.html`, `styles.css`, `script.js` files, and the `images` folder.
2.  **Add Your Images:** Place your own images into the `images` folder.
3.  **Open in Code Editor:** Open the template folder in your preferred code editor (like VS Code, Sublime Text, Atom, Notepad++, etc.). You will primarily work with the `index.html` and `styles.css` files.
4.  **Replace Content:** Follow the customization guide below to replace the demo content (text, images, links) with your own information.
5.  **Upload to Hosting:** Once customized, upload *all* the template files and folders (including the `images` folder with your photos inside) to your web hosting server. The `index.html` file should typically be placed in the root directory (e.g., `public_html` or `www`).

==============================
4. Customization Guide
==============================

You will make most content changes in the `index.html` file. Visual styling changes are primarily in `styles.css`.

**4.1. Basic Site Information (`index.html`)**

* **Browser Tab Title:**
    Find the `<title>` tag in the `<head>` section (around line 9) and change "Nexus | Creative Portfolio" to your desired title.
    ```html
    <title>Your Name | Your Title</title>
    ```
* **Site Logo/Name (Header & Footer):**
    Find the `<a class="logo">Nexus</a>` tag in the `<header>` section (around line 44) and the `<h3>Nexus</h3>` tag in the `<footer>` section (around line 430). Change "Nexus" to your name or brand name.

**4.2. Navigation Menu (`index.html`)**

* The navigation links are in the `<ul class="nav-links">` block (around line 50).
* To change the text of a link, modify the text between the `<a>` tags (e.g., change `Home` to `Intro`).
* To change where a link goes, modify the `href="#section-id"` attribute (e.g., change `#about` to `#my-story`).
* To add or remove a link, add or remove the corresponding `<li>` element.

**4.3. Hero Section (`index.html`)**

* This is the first `<section id="hero">` (around line 67).
* Change the "Hello, I'm" text in the `<h4>` tag.
* Change the name "Alex Johnson" in the `<h1>` tag.
* Change the descriptive paragraph in the `<p>` tag.
* Update the "Hire Me" button text and `href` attribute as needed.
* **Social Icons:**
    Find the `<div class="social-icons">` block (around line 80).
    * To change the link, modify the `href` attribute for each `<a>` tag.
    * To change the icon, find the `<i>` tag and replace the Font Awesome class (e.g., `fab fa-dribbble`) with the class for your desired icon. You can find Font Awesome icons and their classes on the Font Awesome website.

**4.4. About Section (`index.html`)**

* This is the `<section id="about">` (around line 94).
* Change the section title "About Me" in the `<h2>` tag.
* Change the subtitle "Creative Developer & Designer" in the `<h3>` tag.
* Update the paragraphs about yourself in the `<p>` tags.
* **About Image:**
    Find the `<img>` tag within `<div class="about-img">` (around line 103).
    * **ACTION REQUIRED:** You must replace the placeholder `src` URL (`https://images.unsplash.com/...`) with the **relative path** to *your own* photo placed in the `images` folder.
    * **Example:** If your photo is named `my-profile.jpg` and you put it inside the `images` folder, the `src` should be `"images/my-profile.jpg"`.
    * Recommended Image Size: The current placeholder is [Inspect code, e.g., 450x550px]. Aim for a similar aspect ratio and a resolution that looks sharp but isn't excessively large (e.g., width around 600-800px).
    * Update the `alt` text with a brief description of the image (e.g., "Your Name photo").
    ```html
    <img src="images/your-profile.jpg" alt="Your Name">
    ```
* **Skills:**
    Find the `<div class="skills">` block (around line 116).
    * Each `<div class="skill">` represents a skill.
    * Change the skill name (e.g., `<span>Web Development</span>`).
    * Change the percentage displayed (e.g., `<span>95%</span>`).
    * **Important:** To change the actual progress bar width, modify the `data-width` attribute on the `<div class="skill-progress">`. The JavaScript uses this attribute to set the width.

**4.5. Services Section (`index.html`)**

* This is the `<section id="services">` (around line 153).
* Change the section title "My Services".
* Find the `<div class="services-grid">` containing the service cards.
* For each `<div class="service-card fade-in">`:
    * Change the icon: Find the `<i>` tag within `<div class="service-icon">` and replace the Font Awesome class (e.g., `fas fa-laptop-code`) with your desired service icon.
    * Change the title in the `<h3>` tag.
    * Change the service description in the `<p>` tag.

**4.6. Portfolio Section (`index.html`)**

* This is the `<section id="portfolio">` (around line 192).
* Change the section title "Featured Work".
* **Filters:**
    Find the `<div class="portfolio-filter">` (around line 195).
    * Change the text in the filter buttons (e.g., "Web Design", "App Development").
    * **Important:** Change the `data-filter` attribute to match the categories you will use for your portfolio items (e.g., `data-filter="my-web-category"`). The JavaScript uses these attributes for filtering.
* **Portfolio Items:**
    Find the `<div class="portfolio-grid">` containing the portfolio items.
    * Each `<div class="portfolio-item">` is a portfolio entry.
    * **Important:** The `data-category` attribute on the `<div class="portfolio-item">` must match the `data-filter` attributes of the buttons (e.g., `data-category="web app"` means this item will show for both "Web Design" and "App Development" filters, plus "All"). Change these to match your project categories.
    * **ACTION REQUIRED:** Replace the `src` URLs for the `<img>` tags within each portfolio item. Use the **relative path** to *your own* project images placed in the `images` folder.
    * **Example:** If you have a project image named `project1.jpg` in the `images` folder, the `src` should be `"images/project1.jpg"`.
    * Recommended Image Size: The current placeholders are [Inspect code, e.g., 600x600px]. Square or consistent aspect ratios often work best here. Aim for a resolution that looks good without being excessively large (e.g., 800x800px or 1000x800px depending on the original placeholder aspect ratio).
    * Update the `alt` text.
    ```html
    <img src="images/your-project1.jpg" alt="Description of project 1">
    ```
    * Change the project title in the `<h3>` tag within the `.portfolio-overlay`.
    * Change the project category text in the `<p>` tag within the `.portfolio-overlay`.
    * To add or remove items, add or remove the corresponding `<div class="portfolio-item">` blocks. Make sure to update the filter buttons and JavaScript if you significantly change the categories or number of items.
* Update the "View More" button text and `href` if you have a separate, more extensive portfolio page.

**4.7. Testimonials Section (`index.html`)**

* This is the `<section id="testimonials">` (around line 286).
* Change the section title "Client Testimonials".
* Find the `<div class="testimonials-track">` containing the testimonial slides.
* Each `<div class="testimonial-slide">` contains one testimonial.
    * **ACTION REQUIRED:** Replace the `src` URL for the client avatar `<img>` tags. Use the **relative path** to *your own* client photos placed in the `images` folder.
    * **Example:** If a client photo is named `client1.jpg` in the `images` folder, the `src` should be `"images/client1.jpg"`.
    * Recommended Image Size: The current placeholders are [Inspect code, e.g., 200x200px]. Small square images are typical.
    * Update the `alt` text.
    ```html
    <img src="images/client1.jpg" alt="Client Name Photo">
    ```
    * Change the testimonial text within `<div class="testimonial-text">`.
    * Change the author's name in the `<h4>` tag.
    * Change the author's title/company in the `<p>` tag.
    * To add or remove testimonials, add or remove the corresponding `<div class="testimonial-slide">` blocks. You will likely need to update the testimonial dots (`<div class="dot">`) section accordingly and potentially adjust the JavaScript depending on how it's implemented to handle a different number of slides.

**4.8. Contact Section (`index.html`)**

* This is the `<section id="contact">` (around line 366).
* Change the section title "Get In Touch".
* Change the heading and paragraph text in the `contact-info` block.
* **Contact Details:**
    Find the `<div class="contact-details">` block.
    * Update the text for Location, Email, and Phone in the `<h4>` and `<p>` tags within each `contact-item`.
    * [Optional] Change the icons by replacing the Font Awesome classes in the `<i>` tags.
* **Contact Form:**
    Find the `<form id="contactForm">` block.
    * You can change the placeholder text for the input fields (`placeholder="Your Name *"`).
    * **IMPORTANT ACTION REQUIRED:** The included form is frontend HTML/CSS only. To make it functional so you receive messages, you *must* integrate it with a backend service (e.g., Formspree, EmailJS, Netlify Forms, or your own server-side script). The `action` and `method` attributes of the `<form>` tag, and the JavaScript (`script.js`), will need modification depending on the service you choose. This template *does not* include a pre-built functional backend for the form.

**4.9. Footer (`index.html`)**

* This is the `<footer>` section (around line 426).
* Update the site name/logo (`<h3>Nexus</h3>`) in the first column.
* Change the description paragraph.
* Update the social icons and links within the `social-icons` block (same as the Hero section).
* Modify or remove the Services and Quick Links lists (`<ul class="footer-links">`) as needed.
* Update the newsletter text and potentially integrate the form with a mailing list service (similar to the contact form, this frontend needs a backend).
* Update the copyright text in the `<div class="footer-bottom">` (e.g., `&copy; 2025 Your Name/Brand. All Rights Reserved.`).

**4.10. Styling (`styles.css`)**

* The `styles.css` file controls the visual appearance.
* You can change colors, fonts, spacing, and other styles here.
* Look for the `:root` block at the top (around line 13) to easily change the primary, secondary, dark, and light theme colors, which are used throughout the template.
* Be cautious when making extensive changes if you are not familiar with CSS.

**4.11. JavaScript (`script.js`)**

* The `script.js` file contains the code that adds dynamic behavior to the template.
* This includes handling the mobile navigation toggle, adding scroll effects (like the header changing appearance), animating elements into view (the `fade-in` effect), managing the portfolio filtering, controlling the testimonial slider, and hiding the preloader once the page loads.
* You generally do not need to edit this file unless you intend to modify the specific functionality or animations.

==============================
5. Important Notes
==============================

* **Images:** Remember to replace all placeholder images in the `images` folder and update the `src` attributes in `index.html` with the correct relative paths to your own photos.
* **Contact Form & Newsletter:** The forms are frontend designs only. You need to integrate them with a backend service to receive submissions or manage newsletter signups.
* **Hosting:** This is a static HTML template. You need to upload the files to a web server to view it online. Ensure you upload the `images` folder as well.

==============================
6. Need Help?
==============================

If you encounter any issues or have questions that are not covered in this documentation, please feel free to contact me via [Your preferred contact method - e.g., Payhip messages, email address].