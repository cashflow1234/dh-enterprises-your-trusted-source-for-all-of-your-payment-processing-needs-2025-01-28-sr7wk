# DH Enterprises Landing Page - Maintenance Guide

This guide will help you maintain and customize the DH Enterprises landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
The company name appears in the header:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    DH Enterprises
</div>
```
To update:
1. Simply replace "DH Enterprises" with your company name
2. The gradient colors can be modified by changing `from-blue-600` and `to-purple-600`

### Hero Section Text
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Your Trusted Source For All of Your Payment Processing Needs
</h1>
```
To modify:
1. Change the heading text between the `<h1>` tags
2. Adjust text size using Tailwind classes:
   - `text-4xl`: default size
   - `md:text-5xl`: medium screens
   - `lg:text-6xl`: large screens

### Features and Benefits
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-shield-alt text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Security</h3>
    <p class="text-gray-600">State-of-the-art encryption...</p>
</div>
```
To update:
1. Change the icon by replacing the `fa-shield-alt` class with any [Font Awesome](https://fontawesome.com/icons) icon
2. Modify the heading text within `<h3>` tags
3. Update the description text within `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Modify the `href` attribute to point to the correct section ID
2. Ensure section IDs match exactly (case-sensitive)
3. For external links, use complete URLs starting with `https://`

### Call-to-Action Buttons
The page contains two CTA buttons:
```html
<a href="https://form.jotform.com/250266352834053" class="inline-block px-8 py-4 text-lg font-semibold text-white bg-blue-600 rounded-full hover:bg-blue-700">
    Get Started Today
</a>
```
To update:
1. Replace the JotForm URL with your form's URL
2. Update button text between the `<a>` tags
3. Modify button styling using Tailwind classes

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To add proper links:
1. Create privacy.html and terms.html files in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Ensure section IDs match navigation links exactly
   - Check for typos in href attributes
   - IDs must start with a letter and contain no spaces

2. **Responsive Design Issues**
   - Check that you're maintaining the responsive classes:
     - `md:` prefix for medium screens
     - `lg:` prefix for large screens
   - Don't remove the `container` class from main sections

3. **Icon Not Showing**
   - Verify Font Awesome is properly loaded in the header
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

Remember to test all changes across different screen sizes using your browser's developer tools (F12 key).

For additional help or specific issues, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.