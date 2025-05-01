# Landing Page Maintenance Guide

This guide will help you maintain and customize the BrisbaneDev landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    BrisbaneDev  <!-- Replace this text -->
</a>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be updated here -->
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
</div>
```

### Hero Section
To update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8">
    Best Websites In Brisbane  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Custom Websites For Your Business  <!-- Subheading -->
</p>
```

### Understanding Tailwind Classes
Key classes explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `mb-8`: Bottom margin spacing
- `text-gray-300`: Light gray text color
- `hover:text-white`: White text on hover

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes following this pattern:
   - Size: `text-sm`, `text-base`, `text-lg`, `text-xl`
   - Colors: `text-gray-100`, `text-blue-400`, `text-white`
   - Spacing: `p-4` (padding), `m-4` (margin)
   - Responsive: Add `sm:`, `md:`, or `lg:` prefix

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, keep the `#` prefix
2. For external links, use full URLs:
```html
<a href="https://your-domain.com/page">Link Text</a>
```

### Call-to-Action Links
Update the "Get Started" links:
```html
<!-- Find these lines -->
<a href="https://sigmaseo.io" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full">
    Get Started
</a>
```
Replace `https://sigmaseo.io` with your desired URL.

## Linking Privacy and Terms Pages

### Footer Links Setup
1. Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

3. Create matching privacy.html and terms.html files in the same directory as index.html

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - Verify that sections have the correct ID attribute:
```html
<section id="features"> <!-- ID must match the href in navigation -->
```

2. **Responsive Design Issues**
   - Check responsive classes (sm:, md:, lg:)
   - Test on different screen sizes
   - Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Animation Problems**
   - Verify AOS script is loaded
   - Check data-aos attributes
   - Ensure AOS is initialized:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true
    });
</script>
```

Remember to:
- Always backup files before making changes
- Test all links after updating
- View changes on multiple devices and browsers
- Keep consistent styling throughout the page

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [AOS Documentation](https://michalsnik.github.io/aos/)