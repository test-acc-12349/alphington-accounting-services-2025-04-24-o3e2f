# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington accounting services landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Alphington</a>
```
- Replace "Alphington" with your company name
- Adjust font size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main banner section contains your primary message:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight mb-8">
    We transform numbers into opportunities
</h1>
```
- Update the heading text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Dedicated Manager</h3>
    <p class="text-gray-600">Your personal financial expert...</p>
</div>
```
To modify:
1. Update the heading text in `<h3>` tags
2. Change the description in `<p>` tags
3. Adjust spacing with `p-8` (padding) or `mb-4` (margin-bottom)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Use `#section-name` format
   - Ensure section IDs match exactly
   - Example: `<a href="#services">Services</a>`

2. External links:
   - Replace `href="#"` with full URL
   - Example: `<a href="https://your-domain.com/services">Services</a>`

### Call-to-Action Buttons
Current placeholder link:
```html
<a href="https://theaccountants.com" class="inline-flex items-center px-6 py-3...">
```
Replace with your actual booking or contact page URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - Example: `href="#services"` needs `id="services"` on target section

2. **Responsive Design Problems**
   - Keep Tailwind's responsive prefixes:
     - `md:` for medium screens
     - `lg:` for large screens
   - Don't remove `hidden md:flex` from navigation - it controls mobile menu

3. **Animation Issues**
   - Check data-aos attributes are present:
```html
data-aos="fade-up"
data-aos-delay="100"
```
   - Verify AOS script is loaded at bottom of page

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify all external links start with `https://`
- Test all changes across different screen sizes
- Keep original class names when updating content

Remember to always backup your files before making changes and test thoroughly after updates.