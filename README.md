# TibetanLearning Landing Page Maintenance Guide

This guide will help you maintain and customize the TibetanLearning landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the site logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-indigo-600 bg-clip-text text-transparent">
    TibetanLearning
</a>
```
Simply replace "TibetanLearning" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
To modify menu items:
- Change the text between `<a>` tags
- Update the `href` attributes to match your new section IDs
- Keep the existing classes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-indigo-600 bg-clip-text text-transparent">
    Unlock the Secrets of Tibetan: Learn Alphabet & Numbers Fast
</h1>
```
- Replace the heading text while maintaining the HTML structure
- The classes control:
  - `text-4xl/5xl/6xl`: Text size at different screen sizes
  - `bg-gradient-to-r`: Creates the gradient effect
  - `mb-8`: Adds margin bottom spacing

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-105">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Interactive Lessons</h3>
    <p class="text-gray-600">Engage with dynamic content designed to make learning Tibetan intuitive and enjoyable.</p>
</div>
```
To modify:
1. Update the heading text in `<h3>`
2. Change the description in `<p>`
3. Keep the existing classes for consistent styling and animations

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://learningtibetan.com" class="inline-flex items-center...">
```

To update links:
1. Internal links (starting with #):
   - Ensure the href matches the ID of the target section
   - Example: `href="#features"` should match `id="features"` in the target section

2. External links:
   - Replace "https://learningtibetan.com" with your actual URL
   - Test the link after updating

### Common Link Locations
- Header navigation
- Hero section CTA button
- Feature section links
- Footer quick links

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Located in the footer section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To update:
1. Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

2. Create matching HTML files:
   - Create `privacy.html` in the same directory
   - Create `terms.html` in the same directory
   - Use the same styling classes for consistency

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradients**
If the gradient text disappears:
```html
<!-- Check these classes are present -->
bg-gradient-to-r from-purple-600 to-indigo-600 bg-clip-text text-transparent
```

2. **Responsive Issues**
- Classes starting with `md:` apply to medium screens and up
- Classes starting with `lg:` apply to large screens
- If elements aren't responsive, check for these prefixes

3. **Missing Hover Effects**
Ensure these classes are present for interactive elements:
```html
hover:shadow-xl hover:scale-105 transform transition duration-300
```

### Need Help?
- Double-check class names against the Tailwind CSS documentation
- Verify all section IDs match their corresponding links
- Test the page at different screen sizes
- Ensure all files are in the correct directory

Remember to always test your changes across different browsers and screen sizes before deploying to production.