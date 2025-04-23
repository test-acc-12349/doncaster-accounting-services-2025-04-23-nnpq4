# Doncaster Accounting Services Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Doncaster Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
```html
<section class="relative pt-32 pb-24 bg-gradient-to-b from-gray-50 to-white">
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
        Doncaster accounting services <!-- Edit this text -->
    </h1>
    <p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">
        Where accounting expertise meets exceptional service <!-- Edit this text -->
    </p>
</section>
```

To update text content:
1. Locate the specific section in the HTML
2. Replace the text between the opening and closing tags
3. Maintain the existing HTML structure and classes

### Understanding Tailwind Classes

Key class patterns used in this landing page:

- Spacing classes: `px-4`, `py-24`, `mb-6`
  - `px-` = horizontal padding
  - `py-` = vertical padding
  - `mb-` = margin bottom

- Responsive design classes: `md:text-5xl`, `lg:text-6xl`
  - `md:` = applies at medium screens (768px+)
  - `lg:` = applies at large screens (1024px+)

Example of modifying responsive text size:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">

<!-- Modified for smaller text -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">
```

### Color Classes

The landing page uses a consistent color scheme:
- Blue: `bg-blue-600`, `text-blue-600`
- Gray: `text-gray-900`, `bg-gray-50`
- White: `text-white`, `bg-white`

To change colors, replace the color class:
```html
<!-- Original -->
<button class="bg-blue-600">

<!-- Modified to green -->
<button class="bg-green-600">
```

## 2. Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex md:space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, use `#section-id`
2. For external pages, use full URL
```html
<!-- Example external link -->
<a href="https://your-domain.com/services">Services</a>
```

### Call-to-Action Links
Replace placeholder URLs:
```html
<!-- Find this in the hero section -->
<a href="https://theaccountants.com" class="inline-flex items-center...">
```
Change to your actual URL:
```html
<a href="https://your-domain.com/get-started" class="inline-flex items-center...">
```

## 3. Linking Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

Update the href attributes:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

### Troubleshooting Tips

1. **Broken Links**
   - Use browser dev tools (F12) to check for 404 errors
   - Verify file paths are correct relative to index.html
   - Test all links after updating

2. **CSS Classes**
   - If styling breaks, check for typos in class names
   - Maintain spacing between multiple classes
   - Keep responsive classes (`md:`, `lg:`) in the correct order

3. **Layout Issues**
   - Preserve the grid structure in sections
   - Maintain padding/margin classes for spacing
   - Keep responsive design classes for proper mobile display

## Additional Notes

- Always backup your files before making changes
- Test on multiple devices and browsers
- Maintain consistent spacing and indentation
- Keep the original class structure when adding new elements
- Use browser dev tools to inspect and debug issues

For more help with Tailwind CSS classes, visit [Tailwind CSS Documentation](https://tailwindcss.com/docs).