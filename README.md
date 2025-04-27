# Bethesda Glass Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Bethesda Glass landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
```html
<a href="/" class="text-2xl font-bold text-gray-800">
    Bethesda Glass
</a>
```
To update:
1. Replace "Bethesda Glass" with your company name
2. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section Text
Located under the `<!-- Hero Section -->` comment:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Textured Shower Glass That's Slip-Resistant
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Premium European glass solutions for modern bathrooms
</p>
```
To modify:
1. Replace headline text between `<h1>` tags
2. Update subheading text between `<p>` tags
3. Responsive text sizes are defined as:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)

### Feature Cards
Each feature card follows this structure:
```html
<div class="p-8 rounded-xl bg-gray-50 hover:shadow-lg transition-shadow duration-300">
    <i class="fas fa-layer-group text-3xl text-gray-800 mb-6"></i>
    <h3 class="text-xl font-bold mb-4">Luxury Thickness</h3>
    <p class="text-gray-600">Choose between 8mm or 10mm thick glass...</p>
</div>
```
To customize:
1. Change icon by updating the `fa-layer-group` class with any [Font Awesome](https://fontawesome.com/icons) icon
2. Modify heading text between `<h3>` tags
3. Update description text between `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. For internal page sections, keep the `#` prefix (e.g., `#features`)
2. For external pages, use full URLs (e.g., `https://example.com/features`)
3. For local pages, use relative paths (e.g., `./features.html`)

### Call-to-Action Links
```html
<a href="http://www.customeuroglass.com" class="inline-block bg-gray-900 text-white px-8 py-4 rounded-lg">
    Explore Our Collection
</a>
```
To modify:
1. Replace `http://www.customeuroglass.com` with your desired URL
2. Update button text between `<a>` tags
3. Maintain the existing classes for consistent styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To implement proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="./privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in IDs and href values
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Verify Tailwind responsive prefixes:
     - `md:` for tablet (768px+)
     - `lg:` for desktop (1024px+)
   - Test on different screen sizes using browser dev tools

3. **Icon Not Displaying**
   - Confirm Font Awesome CDN is properly loaded
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

4. **Style Changes Not Applying**
   - Verify Tailwind CDN is properly loaded
   - Check class name spelling
   - Ensure classes are in the correct order for proper specificity

Remember to always test your changes across different devices and browsers to ensure consistency in appearance and functionality.