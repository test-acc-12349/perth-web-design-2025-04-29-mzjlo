# Perth Web Design Landing Page - Maintenance & Customization Guide

Welcome! This document provides a comprehensive guide for maintaining and customizing the Perth Web Design landing page. It's designed for developers of all skill levels, especially those new to HTML, CSS, and Tailwind CSS.

## Table of Contents

1.  [Introduction](#introduction)
2.  [Prerequisites](#prerequisites)
3.  [File Structure](#file-structure)
4.  [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
    *   [Text Content Updates](#text-content-updates)
    *   [Tailwind CSS Updates](#tailwind-css-updates)
5.  [Fixing Broken Links](#fixing-broken-links)
    *   [Navigation Menu Links](#navigation-menu-links)
    *   [Footer Links](#footer-links)
    *   [Troubleshooting Broken Links](#troubleshooting-broken-links)
6.  [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
    *   [Adding Links in the Footer](#adding-links-in-the-footer)
7.  [Troubleshooting](#troubleshooting)
8.  [Best Practices](#best-practices)

## Introduction

This landing page promotes web design services in Perth. It's built using HTML and styled with Tailwind CSS. This guide will help you understand how to modify the content, fix links, and add new functionalities.  Don't worry if you're just starting out; we'll break down everything step-by-step.

## Prerequisites

*   **Basic understanding of HTML:** Knowing the basics of HTML tags (like `<h1>`, `<p>`, `<a>`) is essential.
*   **A text editor:**  VS Code, Sublime Text, Atom, or any editor you're comfortable with.
*   **A web browser:** Chrome, Firefox, Safari, or Edge to view your changes.
*   **(Optional) Basic understanding of Tailwind CSS:** Knowing how Tailwind CSS classes work will allow you to more easily style content.
*   **The landing page's `index.html` file.** This is the file we'll be directly editing.

## File Structure

For this project, all the code is contained within a single `index.html` file. This file includes the structure, content and style rules for the landing page. If more complexity were necessary, the styling would be externalized to a css or js file.

## Updating Text and Tailwind CSS Classes

### Text Content Updates

The text displayed on the landing page is directly embedded within the HTML tags.  Here's how to update the text in different sections:

*   **Header:**
    *   **Website Title:** Locate this line within the `<header>` section:
        ```html
        <a href="#" class="text-xl font-bold text-gray-900">
            Perth Web Design
        </a>
        ```
        Change "Perth Web Design" to your desired title. For example:
        ```html
        <a href="#" class="text-xl font-bold text-gray-900">
            Acme Web Solutions
        </a>
        ```
    *   **Navigation Links:** Update the text of links within the `<nav>` element:
        ```html
        <nav class="hidden md:flex items-center space-x-6">
            <a href="#" class="hover:text-blue-500 transition duration-300">Home</a>
            <a href="#" class="hover:text-blue-500 transition duration-300">Services</a>
            <a href="#" class="hover:text-blue-500 transition duration-300">Portfolio</a>
            <a href="#" class="hover:text-blue-500 transition duration-300">Contact</a>
        </nav>
        ```
        For example, to change "Services" to "Our Services":
        ```html
            <a href="#" class="hover:text-blue-500 transition duration-300">Our Services</a>
        ```

*   **Hero Section:**
    *   **Main Heading:** Find the `<h1>` tag within the `<section>` with `class="bg-gray-50 py-24"`:
        ```html
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
            Best Websites In Perth
        </h1>
        ```
        Change "Best Websites In Perth" to your desired headline.
    *   **Sub Heading:**  The `<h2>` under the `<h1>` element. For Example:
        ```html
        <p class="text-lg text-gray-700 mb-8">
            We create stunning, high-performing websites that help your business thrive online.
        </p>
        ```

*   **Features Section:**
    *   **Section Heading:**  Located above the features grid:
        ```html
        <h2 class="text-3xl font-semibold text-gray-900 text-center mb-12">
            Why Choose Perth Web Design?
        </h2>
        ```
        Update the text between the `<h2>` and `</h2>` tags.
    *   **Feature Titles & Descriptions:**  Each feature has an `<h3>` for the title and a `<p>` for the description.  Locate these within each `<div>` with `class="bg-white shadow-md rounded-lg p-6 hover:shadow-lg transition duration-300"`.

*   **Benefits Section:**
    *   **Section Heading:** Similar to the Features Section, the heading is located above the benefits grid.
    *   **Benefit Titles & Descriptions:**  Within each `<div>` of the benefits grid, you'll find an `<h3>` for the title and a `<p>` for the description.

*   **Call to Action (CTA) Section:**
    *   **Heading & Description:** Located within the `<section class="py-24 bg-blue-600 text-white" ...>` section.
    *   **Button Text:**  Update the text between the `<a>` tags of the CTA button.

*   **FAQ Section:**
    *   **Section Heading:** Located at the top of the section.
    *   **FAQ Questions & Answers:**  Update the `<h3>` for the question and the `<p>` for the answer within each `accordion-item` section.

*   **Contact Section:**
    *   **Section Heading:** Located above the email address
    *   **Email Address:** Update the email address within the `<a href="mailto:admin@twd.com" ...>` tag.

*   **Footer:**
    *   **About Us:**  Located in the first `<div>` within the `<footer>`. Update the `<p>` tag.
    *   **Quick Links:**  Update the text of the links within the `<ul>` element.
    *   **Contact Information:** Update the email address within the `<p>` tag, similar to the Contact Section.

**Important:** Remember to save your `index.html` file after making changes and refresh your browser to see the updates.

### Tailwind CSS Updates

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS, you apply pre-defined classes to your HTML elements.

*   **Understanding Tailwind Classes:**  Each class represents a specific CSS property and value.  For example:
    *   `text-xl`:  Sets the font size to extra large.
    *   `font-bold`:  Sets the font weight to bold.
    *   `text-gray-900`:  Sets the text color to a dark gray.
    *   `bg-blue-500`:  Sets the background color to a blue shade.
    *   `hover:bg-blue-700`:  Changes the background color to a darker blue on hover.
    *   `md:text-5xl`:  Sets the text size to 5xl on medium screens and above (responsive design).
    *   `lg:grid-cols-3`:  Creates a three-column grid on large screens and above.
    *   `shadow-md`:  Adds a medium-sized shadow.

*   **Modifying Classes:** To change the styling, simply modify or add/remove Tailwind CSS classes in your HTML.

**Examples:**

1.  **Changing the Hero Section Heading Color:**
    *   Original:
        ```html
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
            Best Websites In Perth
        </h1>
        ```
    *   To change the heading color to blue, replace `text-gray-900` with `text-blue-500`:
        ```html
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-blue-500 leading-tight tracking-tight mb-6">
            Best Websites In Perth
        </h1>
        ```

2.  **Making the Feature Boxes Rounded:**
    *   Original:
        ```html
        <div class="bg-white shadow-md rounded-lg p-6 hover:shadow-lg transition duration-300">
        ```
    * To make them more rounded, increase the `rounded-lg` class to `rounded-xl`:
    ```html
        <div class="bg-white shadow-md rounded-xl p-6 hover:shadow-lg transition duration-300">
    ```

3.  **Changing Button Color and Hover State:**
    *   Original:
        ```html
        <a href="https://twd.com" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-3 px-6 rounded-md shadow-md transition duration-300 transform hover:scale-105 inline-block">
            Get a Free Quote
        </a>
        ```
    *   To change the button color to green and the hover to a lighter green, change `bg-blue-500` to `bg-green-500` and `hover:bg-blue-700` to `hover:bg-green-700`:
        ```html
        <a href="https://twd.com" class="bg-green-500 hover:bg-green-700 text-white font-bold py-3 px-6 rounded-md shadow-md transition duration-300 transform hover:scale-105 inline-block">
            Get a Free Quote
        </a>
        ```

*   **Responsive Design with Tailwind:** Tailwind uses prefixes like `md:`, `lg:`, `xl:` to apply styles at different screen sizes.
    *   `md:text-5xl` means "apply `text-5xl` style on medium screens and above."
    *   If you want a different font size on smaller screens, add a class without a prefix (e.g., `text-3xl`).

## Fixing Broken Links

The landing page currently contains placeholder links (`href="#"`).  It's crucial to replace these with actual URLs.

### Navigation Menu Links

1.  **Locate the `<nav>` element:** Within the `<header>` section, find the following code:
    ```html
    <nav class="hidden md:flex items-center space-x-6">
        <a href="#" class="hover:text-blue-500 transition duration-300">Home</a>
        <a href="#" class="hover:text-blue-500 transition duration-300">Services</a>
        <a href="#" class="hover:text-blue-500 transition duration-300">Portfolio</a>
        <a href="#" class="hover:text-blue-500 transition duration-300">Contact</a>
    </nav>
    ```

2.  **Update the `href` attributes:** Replace the `#` with the correct URLs for each link.  For example:
    ```html
    <nav class="hidden md:flex items-center space-x-6">
        <a href="index.html" class="hover:text-blue-500 transition duration-300">Home</a>
        <a href="services.html" class="hover:text-blue-500 transition duration-300">Services</a>
        <a href="portfolio.html" class="hover:text-blue-500 transition duration-300">Portfolio</a>
        <a href="contact.html" class="hover:text-blue-500 transition duration-300">Contact</a>
    </nav>
    ```

    *   **Internal Links:** Use relative paths (e.g., `services.html`, `contact.html`) to link to other pages within your website.  These should be in the same folder as your `index.html`.
    *   **External Links:** Use absolute URLs (e.g., `https://www.example.com/`) to link to external websites.

### Footer Links

1.  **Locate the "Quick Links" section in the `<footer>`:**
    ```html
    <div>
        <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
        <ul class="space-y-2">
            <li><a href="#" class="hover:text-blue-500 transition duration-300">Home</a></li>
            <li><a href="#" class="hover:text-blue-500 transition duration-300">Services</a></li>
            <li><a href="#" class="hover:text-blue-500 transition duration-300">Portfolio</a></li>
            <li><a href="#" class="hover:text-blue-500 transition duration-300">Contact</a></li>
            <li><a href="#" class="hover:text-blue-500 transition duration-300">Blog</a></li>
        </ul>
    </div>
    ```

2.  **Update the `href` attributes:** Replace the `#` with the correct URLs for each link, similar to the navigation menu:
    ```html
    <div>
        <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
        <ul class="space-y-2">
            <li><a href="index.html" class="hover:text-blue-500 transition duration-300">Home</a></li>
            <li><a href="services.html" class="hover:text-blue-500 transition duration-300">Services</a></li>
            <li><a href="portfolio.html" class="hover:text-blue-500 transition duration-300">Portfolio</a></li>
            <li><a href="contact.html" class="hover:text-blue-500 transition duration-300">Contact</a></li>
            <li><a href="blog.html" class="hover:text-blue-500 transition duration-300">Blog</a></li>
        </ul>
    </div>
    ```

### Troubleshooting Broken Links

*   **Double-check the URLs:** Ensure the URLs are typed correctly and point to the right location.
*   **Check file paths:**  Verify that the paths to your internal pages are correct relative to your `index.html` file.
*   **Test in different browsers:**  Sometimes, caching issues can cause links to appear broken in one browser but not another. Clear your browser's cache or try a different browser.
*   **Use your browser's developer tools:**  Open the "Network" tab in your browser's developer tools (usually by pressing F12). When you click a link, you can see if the browser is successfully retrieving the linked page. If you see an error (like a 404 Not Found), there's an issue with the URL.

## Linking Privacy and Terms Pages

It's important to include links to your Privacy Policy and Terms of Service pages.  We'll add these to the footer.

### Adding Links in the Footer

1.  **Locate the "Quick Links" section in the `<footer>`:** (Same as in the previous section)

2.  **Add the Privacy Policy and Terms of Service links:**  Insert these links within the `<ul>` element:
    ```html
    <div>
        <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
        <ul class="space-y-2">
            <li><a href="index.html" class="hover:text-blue-500 transition duration-300">Home</a></li>
            <li><a href="services.html" class="hover:text-blue-500 transition duration-300">Services</a></li>
            <li><a href="portfolio.html" class="hover:text-blue-500 transition duration-300">Portfolio</a></li>
            <li><a href="contact.html" class="hover:text-blue-500 transition duration-300">Contact</a></li>
            <li><a href="blog.html" class="hover:text-blue-500 transition duration-300">Blog</a></li>
            <li><a href="privacy.html" class="hover:text-blue-500 transition duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="hover:text-blue-500 transition duration-300">Terms of Service</a></li>
        </ul>
    </div>
    ```

    *   **Make sure you have `privacy.html` and `terms.html` files** in the same directory as your `index.html` file.  Create them if they don't exist.
    *   **Adjust the `href` attributes if your privacy and terms pages are in a different location.**
    *   **Ensure your privacy and terms pages adhere to legal requirements.**

## Troubleshooting

*   **Changes not showing up:**  Clear your browser's cache.  Press Ctrl+Shift+R (or Cmd+Shift+R on a Mac) to force a hard refresh.
*   **Tailwind CSS classes not working:**  Make sure you've included the Tailwind CSS stylesheet in the `<head>` section of your `index.html`.  Check for typos in the class names.
*   **Website looks broken on mobile:**  Check your viewport meta tag in the `<head>` section.  It should look like this:
    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
    This ensures the website scales correctly on different screen sizes.
*   **Images not loading:** Ensure the image paths in the `src` attribute of your `<img>` tags are correct.
*   **The Accordian Functionality not working:** This is a javascript driven functionality that is not active in this code. To make this work, you must include a `<script>` tag that defines the appropriate events.

## Best Practices

*   **Use descriptive class names:**  While Tailwind's utility classes are powerful, add comments or use custom CSS classes (if needed) to make your code more readable.
*   **Test on different devices:**  Use browser developer tools to simulate different screen sizes and devices to ensure your website is responsive.
*   **Validate your HTML:**  Use an HTML validator (like the one at [https://validator.w3.org/](https://validator.w3.org/)) to check for errors in your HTML code.
*   **Keep your code organized:** Use proper indentation and comments to make your code easier to understand and maintain.

By following this guide, you should be well-equipped to maintain and customize the Perth Web Design landing page. Remember to experiment, test, and have fun!