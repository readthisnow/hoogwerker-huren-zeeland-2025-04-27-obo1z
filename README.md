# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Zeeland landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker Zeeland</a>
```
- Replace "Hoogwerker Zeeland" with your company name
- Adjust text size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)
- Change color using `text-blue-600` (options: `text-red-600`, `text-green-600`, etc.)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="font-medium text-gray-700 hover:text-blue-600">Voordelen</a>
    <!-- More menu items -->
</div>
```
- Replace text between `>` and `</a>` with new menu items
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Hoogwerker Huren Zeeland
    <span class="block text-blue-600 mt-2">Tijdelijk 10% Korting!</span>
</h1>
```
- Update main heading text
- Modify discount text in the `<span>` tag
- Adjust text sizes by changing `text-4xl`, `text-5xl`, etc.

### Responsive Design Tips
- Classes starting with `md:` apply to medium screens and larger
- Classes starting with `lg:` apply to large screens
- Keep both mobile and desktop classes when updating

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Voordelen</a>
<a href="#pricing">Prijzen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://hansschuiling.nl" class="...">Direct Huren</a>
```

### Updating Links
1. **Internal Links** (sections on the same page):
- Keep the `#` symbol
- Match the `id` of the target section
- Example: `<a href="#contact">Contact</a>` links to `<section id="contact">`

2. **External Links** (other websites):
- Replace the full URL
- Include `https://` or `http://`
```html
<!-- Before -->
<a href="https://hansschuiling.nl">Direct Huren</a>
<!-- After -->
<a href="https://your-new-url.com">Direct Huren</a>
```

## Linking Privacy and Terms Pages

### Adding Footer Links
Add these links to the footer section:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Hoogwerker Zeeland. Alle rechten voorbehouden.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Place them in the same folder as `index.html`
3. Use the same styling classes for consistency

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout:**
- Check for missing closing tags
- Verify Tailwind CSS classes are spelled correctly
- Ensure responsive classes (`md:`, `lg:`) are present

2. **Links Not Working:**
- Verify file names match exactly (case-sensitive)
- Check if files are in the correct folder
- Ensure `#` sections have matching `id` attributes

3. **Styles Not Applying:**
- Confirm Tailwind CSS CDN link is present in `<head>`
- Check for typos in class names
- Verify class order (responsive classes should come after base classes)

### Need More Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different screen sizes and browsers before publishing updates to your live site.