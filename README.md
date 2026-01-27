# Ekdant's Cafe Private Limited - Website

Welcome to the official website for **Ekdant's Cafe Private Limited**! This is a modern, responsive, and visually stunning website designed to showcase our cafe's offerings, location, and contact information.

## 🌟 Features

### 1. **Dynamic Daily Menu**
- Menu items can be updated daily through an admin panel
- Four categories: Starters, Main Course, Desserts, and Beverages
- Menu data is stored locally in the browser (localStorage)
- Beautiful card-based layout with hover effects

### 2. **Admin Panel**
- Secure password-protected admin access
- Easy-to-use interface for updating menu items
- Password: `ekdant2026`
- Format: `Item Name | Price` (one per line)

### 3. **Beautiful UI/UX**
- Premium color palette with gold (#d4af37) and dark brown (#2c1810) theme
- Smooth animations and transitions
- Glassmorphism effects
- Responsive design for all devices
- Professional typography using Playfair Display and Inter fonts

### 4. **Sections**
- **Hero Section**: Eye-catching landing with call-to-action buttons
- **Today's Menu**: Dynamic menu display with daily updates
- **About Section**: Cafe story and values with feature highlights
- **Gallery**: Beautiful food photography showcase
- **Location**: Interactive map and detailed location information
- **Contact**: Contact form and social media links

### 5. **Interactive Elements**
- Smooth scrolling navigation
- Active nav link highlighting on scroll
- Mobile-friendly hamburger menu
- Contact form with validation
- Hover effects on all interactive elements
- Scroll-triggered animations

## 🚀 How to Use

### Opening the Website
1. Simply open `index.html` in any modern web browser
2. The website works completely offline (no server required)

### Updating the Daily Menu
1. Scroll to the "Today's Menu" section
2. Click the **"Admin Panel"** button
3. Enter the password: `ekdant2026`
4. Click **"Verify"**
5. Edit the menu items in the text areas
   - Format: `Item Name | Price`
   - Example: `Butter Chicken | ₹350`
6. Click **"Save Menu"**
7. The menu will update immediately and persist in the browser

### Customizing Content

#### Changing Contact Information
Edit `index.html` and find the contact section:
```html
<div class="contact-card">
    <h4>Phone</h4>
    <p>+91 98765 43210</p>
    <p>+91 98765 43211</p>
</div>
```

#### Updating Location
1. Find the location section in `index.html`
2. Update the address in the info-card
3. To change the map, replace the Google Maps embed URL

#### Changing Images
Replace the following image files with your own:
- `cafe-interior.jpg` - About section image
- `food-1.jpg` to `food-6.jpg` - Gallery images

#### Modifying Colors
Edit `styles.css` and change the CSS variables at the top:
```css
:root {
    --primary-color: #d4af37;
    --secondary-color: #2c1810;
    /* ... other colors */
}
```

## 📱 Responsive Design

The website is fully responsive and works perfectly on:
- Desktop computers (1920px and above)
- Laptops (1024px - 1920px)
- Tablets (768px - 1024px)
- Mobile phones (320px - 768px)

## 🎨 Design Features

### Color Palette
- **Primary Gold**: #d4af37 (Luxury and premium feel)
- **Dark Brown**: #2c1810 (Warmth and elegance)
- **Accent Orange**: #e67e22 (Energy and appetite)
- **Light Cream**: #f8f5f0 (Clean background)

### Typography
- **Headings**: Playfair Display (Elegant serif)
- **Body**: Inter (Modern sans-serif)

### Animations
- Fade-in on scroll
- Hover effects on buttons and cards
- Smooth transitions
- Bouncing scroll indicator

## 🛠️ Technical Details

### Technologies Used
- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS Grid and Flexbox
- **JavaScript**: Vanilla JS (no frameworks)
- **LocalStorage**: For menu data persistence
- **Font Awesome**: For icons
- **Google Fonts**: For typography

### Browser Compatibility
- Chrome (recommended)
- Firefox
- Safari
- Edge
- Opera

### File Structure
```
EKDANT'S CAFE PRIVATE LIMITED/
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # JavaScript functionality
├── cafe-interior.jpg   # About section image
├── food-1.jpg         # Gallery image
├── food-2.jpg         # Gallery image
├── food-3.jpg         # Gallery image
├── food-4.jpg         # Gallery image
├── food-5.jpg         # Gallery image
├── food-6.jpg         # Gallery image
└── README.md          # This file
```

## 📝 SEO Optimized

The website includes:
- Proper meta tags
- Descriptive title and description
- Semantic HTML5 elements
- Optimized heading hierarchy
- Alt text for images (when you add your own)

## 🔒 Admin Panel Security

**Important**: The current admin password is stored in the JavaScript file for demonstration purposes. For production use:
1. Implement server-side authentication
2. Use a proper backend (Node.js, PHP, etc.)
3. Store menu data in a database
4. Use HTTPS for secure connections

## 📞 Support

For any questions or customization requests, please contact:
- **Email**: info@ekdantscafe.com
- **Phone**: +91 98765 43210

## 📄 License

© 2026 Ekdant's Cafe Private Limited. All rights reserved.

---

**Enjoy your beautiful new website! 🎉**

## Quick Start Checklist

- [ ] Open `index.html` in a browser
- [ ] Test the admin panel with password `ekdant2026`
- [ ] Update menu items for today
- [ ] Replace images with your own cafe photos
- [ ] Update contact information
- [ ] Update location and map
- [ ] Customize colors if needed
- [ ] Test on mobile devices
- [ ] Share with your customers!

---

*Built with ❤️ for Ekdant's Cafe*
