# Landing Page Maintenance Guide

This guide will help you maintain and customize the DP Ventures landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<!-- Located in header section -->
<a href="/" class="text-xl font-bold tracking-tight hover:text-indigo-400 transition-colors duration-300">
    DP Ventures  <!-- Change this text -->
</a>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#portfolio" class="text-gray-300 hover:text-white transition-colors duration-300">Portfolio</a>
    <!-- Update text within each <a> tag -->
</div>
```

### Hero Section
The main welcome section at the top of the page:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold leading-tight tracking-tighter mb-8">
    The journey of an entrepreneur and innovator. <!-- Update heading -->
</h1>
<p class="text-xl sm:text-2xl text-gray-300 mb-12 leading-relaxed">
    Entrepreneurship and Innovation Redefined <!-- Update subheading -->
</p>
```

### Tailwind CSS Class Guide
Common classes explained:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right
- `bg-[color]`: Sets background color

To modify responsive design:
```html
<!-- Example of responsive text sizing -->
<h1 class="text-4xl sm:text-5xl lg:text-6xl">
<!-- Breaks down to: -->
<!-- Mobile: text-4xl -->
<!-- Small screens (sm): text-5xl -->
<!-- Large screens (lg): text-6xl -->
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#portfolio">Portfolio</a>
    <a href="#expertise">Expertise</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, use `#section-id`
2. For external pages, use full URL:
```html
<a href="https://example.com">External Link</a>
```

### Footer Links
Located at the bottom of the page:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <!-- Quick Links Section -->
    <ul class="space-y-2">
        <li><a href="#portfolio">Portfolio</a></li>
        <!-- Add or modify links here -->
    </ul>
</div>
```

### Email Link
To update the email address:
```html
<a href="mailto:perezdenmar@gmail.com">perezdenmar@gmail.com</a>
<!-- Change both the href and visible text -->
```

## Adding Privacy and Terms Pages

### Current Footer Legal Section
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Ensure consistent styling by copying these classes:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. Broken Internal Links
- Check that section IDs match exactly:
```html
<!-- Navigation link -->
<a href="#portfolio">Portfolio</a>

<!-- Must match section ID -->
<section id="portfolio">
```

2. Responsive Design Issues
- Verify breakpoint classes are in order:
  - Mobile (default): No prefix
  - Small screens: `sm:`
  - Medium screens: `md:`
  - Large screens: `lg:`

3. Style Inconsistencies
- Copy existing classes for new elements
- Maintain color scheme:
  - Primary: `indigo-600`
  - Background: `gray-900`
  - Text: `gray-100`, `gray-300`, `gray-400`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools (F12)

Remember to always test changes across different screen sizes and browsers before deploying to production.