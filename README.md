# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. Change the brand name:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Claude</a>
```
Replace "Claude" with your brand name.

### Hero Section
Located at the top of the page with the main headline:

1. Update the main headline:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight mb-8">
    Create stunning landing pages in minutes
</h1>
```
Replace the text while keeping the HTML tags intact.

2. Modify the subtitle:
```html
<p class="text-xl text-gray-600 mb-12 leading-relaxed">
    Transform your web presence with professional landing pages that convert visitors into customers.
</p>
```

### Working with Tailwind Classes

Important classes explained:
- `text-4xl`: Controls text size
- `md:text-5xl`: Applies different text size on medium screens
- `font-bold`: Makes text bold
- `mb-8`: Adds margin bottom (spacing)
- `text-gray-900`: Sets text color

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Modify existing classes or add new ones

Example - changing text color:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4 text-gray-900">

<!-- Modified to blue -->
<h3 class="text-xl font-semibold mb-4 text-blue-600">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Change the value to your desired destination:
   - For same-page sections, use `#section-name`
   - For other pages, use the full URL or relative path

Example:
```html
<!-- Change this -->
<a href="#features">Features</a>

<!-- To this -->
<a href="/features.html">Features</a>
```

### Call-to-Action (CTA) Links
Current CTA buttons point to "https://fixrr.online". Update these:

1. Find all instances:
```html
<a href="https://fixrr.online" class="inline-flex items-center...">
```

2. Replace with your destination URL:
```html
<a href="https://your-website.com" class="inline-flex items-center...">
```

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links in footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link properly:

1. Create your policy pages:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the links:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

Common issues and solutions:

### Text Changes Not Visible
- Check if you preserved all HTML tags
- Verify you didn't accidentally delete any closing tags
- Ensure proper nesting of elements

### Links Not Working
1. Check for typos in URLs
2. Verify file names match exactly
3. Confirm files are in the correct directory
4. Test that linked pages actually exist

### Styling Issues
1. Check for missing class names
2. Verify Tailwind CDN link is present:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
3. Ensure responsive classes (md:, lg:) remain intact

Need more help? Contact your development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).