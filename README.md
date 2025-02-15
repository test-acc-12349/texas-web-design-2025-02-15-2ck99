# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Written for beginners, it provides step-by-step instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To modify:

1. **Logo Text**: Find this line in the header:
```html
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

2. **Navigation Menu Items**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
Replace the text between `<a>` tags to change menu items.

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```

#### Tailwind CSS Class Guide
- Text sizes: `text-4xl`, `text-5xl`, `text-6xl`
- Colors: `text-gray-900`, `text-blue-600`
- Spacing: `mb-6`, `py-4`, `px-8`
- Responsive design: Classes starting with `md:` or `lg:` apply at medium/large screens

## Managing Links

### Internal Links
The page uses anchor links to scroll to sections. Update these in the navigation:

1. Find all `href="#section-name"` attributes
2. Ensure they match the `id` attributes of corresponding sections
3. Example:
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Matching section -->
<section id="features" class="py-24 bg-white">
```

### External Links
Replace placeholder links with actual URLs:

1. Update the main CTA button:
```html
<a href="https://twd.com" class="inline-block bg-blue-600...">Get Started</a>
```

2. Update social media links in the footer:
```html
<a href="#" class="hover:text-white transition-colors duration-300">
    <i class="fab fa-twitter"></i>
</a>
```
Replace `#` with actual social media URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new HTML files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section `id` attributes match exactly with `href` values
- IDs are case-sensitive
- Remove any spaces in ID names

2. **Responsive Design Issues**
- If elements look wrong on mobile:
  - Check for `md:` prefixed classes
  - Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Missing Icons**
- If Font Awesome icons don't appear:
  - Verify the Font Awesome CSS link is present:
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
```

### Getting Help
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling issues
- Verify all links using your browser's developer tools (F12)
- Test the page on multiple devices and browsers

Remember to always make a backup of your files before making significant changes.