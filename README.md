# EagleiO Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the EagleiO landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
The main headline and subtext are located in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Soar Above Service Hassles with EagleiO
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    The official home of EagleiO - your trusted Hygiene Solutions delivery SaaS App.
</p>
```
To modify:
1. Locate the `<h1>` tag for the main headline
2. Replace the text between the opening and closing tags
3. For the subtext, update the content within the `<p>` tag

#### Features Section
Each feature card contains:
```html
<h3 class="text-xl font-semibold mb-4">On-demand Solutions</h3>
<p class="text-gray-400">Access professional hygiene services whenever you need them, with just a few clicks.</p>
```
To update:
1. Find the feature card you want to modify in the Features section
2. Update the `<h3>` text for the feature title
3. Modify the `<p>` text for the feature description

### Tailwind CSS Classes

#### Understanding Responsive Classes
The landing page uses Tailwind's responsive prefixes:
- `md:` applies styles on medium screens (768px and up)
- `lg:` applies styles on large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Default size: text-4xl (2.25rem)
- Medium screens: text-5xl (3rem)
- Large screens: text-6xl (4rem)

#### Common Tailwind Classes Used
- Layout: `container`, `mx-auto`, `px-6`, `py-24`
- Flexbox: `flex`, `items-center`, `justify-between`
- Grid: `grid`, `grid-cols-1`, `md:grid-cols-3`
- Colors: `bg-gray-900`, `text-gray-300`, `from-blue-500`
- Typography: `text-xl`, `font-bold`, `leading-tight`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are located in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="https://eagle360.app" class="px-6 py-2 bg-gradient-to-r from-blue-500 to-teal-400 rounded-full">Get Started</a>
</div>
```

To update:
1. Locate the `<a>` tag you want to modify
2. Update the `href` attribute with your new link
3. For internal links (same page sections), use `#section-id`
4. For external links, use the full URL including `https://`

### Footer Links
Social media and contact links are in the footer:
```html
<a href="mailto:admin@eagle360.app" class="text-gray-400 hover:text-white">admin@eagle360.app</a>
```

To update:
1. Find the relevant `<a>` tag in the footer section
2. Replace the `href` value with your new link
3. Update the displayed text between the tags if needed

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Current placeholder links in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to your policy pages:
1. Replace the `#` in the `href` with your page path:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

2. Ensure your privacy.html and terms.html files are in the correct directory
3. Maintain consistent styling by keeping the existing classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match the href values
   - Check for typos in both the link and section ID
   - Ensure section IDs are unique

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify responsive classes (md:, lg:) are correctly applied
   - Test at different screen sizes

3. **Missing Styles**
   - Confirm Tailwind CSS is properly loaded
   - Check for typos in class names
   - Verify class combinations are valid

For additional help or questions, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)