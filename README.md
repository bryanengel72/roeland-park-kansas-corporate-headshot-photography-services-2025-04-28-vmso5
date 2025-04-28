# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features
- Benefits
- FAQ
- Call to Action
- Footer

### Updating Text Content

#### Header Text
To update the company name in the header:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-xl font-semibold">101Headshots</a>
```
Simply replace "101Headshots" with your desired text.

#### Hero Section
Locate the hero section (first section after `<main>`):
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Roeland Park, Kansas Corporate Headshot Photography Services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Visual branding for Roeland Park's ambitious professionals.
</p>
```
Replace the text while maintaining the HTML structure.

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
In this template, responsive classes use these prefixes:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
class="text-4xl md:text-5xl lg:text-6xl"
```
This means:
- Mobile (default): text-4xl (36px)
- Tablet (md): text-5xl (48px)
- Desktop (lg): text-6xl (60px)

#### Common Tailwind Classes Used
- Spacing: `px-4`, `py-24`, `mb-6` (padding and margin)
- Colors: `text-gray-900`, `bg-white`, `text-blue-600`
- Layout: `flex`, `grid`, `max-w-7xl`
- Typography: `text-xl`, `font-semibold`

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

To update these links:
1. For internal section links, ensure the `href` matches the section's `id`
2. For external links, replace `#` with the full URL
3. Example: `<a href="https://www.example.com/features">Features</a>`

### Call-to-Action Links
Update the booking links:
```html
<!-- Find these lines -->
<a href="https://www.101headshots.com" class="inline-flex items-center...">
```
Replace the URL with your actual booking page link.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links in the footer:
```html
<div>
    <h3 class="text-xl font-semibold text-white mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
   - Verify Tailwind responsive prefixes are correct
   - Test on multiple screen sizes
   - Common classes to check:
     ```html
     class="text-4xl md:text-5xl lg:text-6xl"
     class="grid grid-cols-1 md:grid-cols-3"
     ```

3. **Missing Styles**
   - Ensure Tailwind CDN is properly loaded
   - Check for typos in class names
   - Verify all classes are space-separated

### Best Practices
- Always test changes in multiple browsers
- Maintain consistent spacing and alignment
- Keep the responsive design intact when updating classes
- Back up files before making significant changes

Need further assistance? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).