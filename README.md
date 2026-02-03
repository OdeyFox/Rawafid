# Rawafid Alssalb Factory Website

A bilingual (English/Arabic) responsive website for a steel fabrication company built with pure HTML, CSS, and JavaScript - no PHP required!

## Features

- 🌐 **Bilingual Support**: Full English and Arabic translations with RTL (Right-to-Left) support
- 📱 **Fully Responsive**: Desktop, tablet, and mobile optimized
- 🏗️ **Product Showcase**: 8 complete product detail pages with comprehensive specifications
- 📧 **Contact**: Direct email and phone links (no form submission)
- 🎨 **Modern Design**: Steel industry themed with smooth animations and professional layout
- ⚡ **High Performance**: Static HTML files for fast loading and easy hosting

## Project Structure

```
rawafid/
├── index.html                    # Main homepage
├── css/
│   └── styles.css               # Main stylesheet (responsive)
├── js/
│   └── main.js                  # JavaScript (language switching, translations)
├── products/
│   ├── steel-bridges.html       # Steel Bridges & Gantry Structures
│   ├── heavy-duty-buildings.html # Heavy Duty Industrial Buildings
│   ├── storage-tanks-silos.html # Storage Tanks, Silos & Pressure Vessels
│   ├── turbine-houses.html      # Turbine Houses & Power Structures
│   ├── high-tension-towers.html # High Tension Towers & Transmission
│   ├── aircraft-hangars.html    # Aircraft Hangars & Aviation Structures
│   ├── cargo-terminals.html     # Cargo Terminals & Logistics
│   └── pre-engineered-buildings.html # Pre-Engineered Metal Buildings
├── README.md                    # This file
└── products.pdf                 # Product catalog reference
```

## Installation

### 1. Requirements

- Any web server (Apache, Nginx, IIS) OR simply open HTML files directly
- No PHP required - pure static HTML!
- Modern web browser with JavaScript enabled

### 2. Run Locally

**Option A - Python (Recommended):**
```bash
python -m http.server 8000
```
Then open: http://localhost:8000

**Option B - PHP built-in server:**
```bash
php -S localhost:8000
```
Then open: http://localhost:8000

**Option C - Open directly:**
Simply open `index.html` in your web browser (some features may require a local server)

### 3. Deployment

Deploy to any static hosting service:
- **GitHub Pages**: Push to repository, enable Pages in settings
- **Netlify**: Drag and drop project folder
- **Vercel**: Connect your repository
- **Traditional Hosting**: Upload via FTP/SFTP

## Usage

### Language Switching

Click the **EN / عربي** button in the navigation to switch between English and Arabic. The preference is automatically saved in localStorage and persists across pages.

### Product Detail Pages

Access product details by clicking on any product card from the homepage or directly via:
- `products/steel-bridges.html`
- `products/heavy-duty-buildings.html`
- `products/storage-tanks-silos.html`
- `products/turbine-houses.html`
- `products/high-tension-towers.html`
- `products/aircraft-hangars.html`
- `products/cargo-terminals.html`
- `products/pre-engineered-buildings.html`

### Contact

The contact section provides direct links:
- **Email**: Click to open email client with pre-filled address
- **Phone**: Click to dial directly on mobile devices
- **Address**: View location information

## Products Available

1. **Steel Bridges & Gantry Structures** - Highway, railway, and pedestrian bridges
2. **Heavy Duty Industrial Buildings** - Multi-story factories and warehouses
3. **Storage Tanks & Silos** - API/ASME certified pressure vessels and storage
4. **Turbine Houses & Power Structures** - Power generation facilities
5. **High Tension Towers** - Transmission line infrastructure up to 500kV
6. **Aircraft Hangars** - Aviation maintenance and storage facilities
7. **Cargo Terminals** - Logistics and freight handling structures
8. **Pre-Engineered Metal Buildings** - Rapid construction PEB systems

## Customization

### Colors

Edit `css/styles.css`:
```css
:root {
    --primary-red: #9f0921;      /* Main accent color */
    --dark: #272727;             /* Background */
    --gray: #6b6b6b;             /* Secondary text */
    --white: #ffffff;            /* Text color */
}
```

### Company Information

Edit in `index.html`:
- Phone numbers
- Email addresses
- Address
- Company name variations

### Add New Products

1. Create new HTML file in `products/` folder (copy existing product page as template)
2. Add card to `index.html` products section
3. Add translation keys to `js/main.js` translations object

### Add New Translations

Edit `js/main.js` translations object:
```javascript
const translations = {
    en: {
        newKey: "English text",
    },
    ar: {
        newKey: "النص العربي",
    }
}
```

Then add `data-i18n="newKey"` attribute to any HTML element.

## Technical Details

### Bilingual Implementation

- **Language Detection**: Automatically detects saved preference from localStorage
- **RTL Support**: Automatically switches layout direction for Arabic
- **Font Selection**: Uses Montserrat (English) and Cairo (Arabic) fonts
- **Dynamic Content**: All text updates instantly without page reload

### Responsive Design Breakpoints

- **Mobile**: < 768px
- **Tablet**: 768px - 1024px  
- **Desktop**: > 1024px

### Performance Features

- Static HTML files (no server-side processing)
- Optimized SVG illustrations
- Efficient CSS selectors
- Minimal JavaScript footprint
- No external dependencies (no frameworks, pure vanilla JS)

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## Deployment to GitHub Pages

1. Push changes to your GitHub repository
2. Go to Repository Settings → Pages
3. Select source branch (main)
4. Click Save
5. Your site will be live at: `https://yourusername.github.io/rawafid/`

## Support

For questions about:
- **Customization**: Modify CSS and translations as needed
- **Deployment**: Consult your hosting provider
- **Adding features**: Pure HTML/CSS/JS - anything is possible!

## License

This project is proprietary to Rawafid Alssalb Factory.

## Company Information

**Rawafid Alssalb Factory**
- Specializes in design, fabrication, painting, delivery, and erection of steel structural works
- ISO 9001:2015 certified quality
- AWS D1.1 welding standards
- State-of-the-art machinery and equipment

---

Built with ❤️ using pure HTML, CSS, and JavaScript
