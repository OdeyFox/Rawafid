# Rawafid Alssalb Factory Website

A bilingual (English/Arabic) responsive website for a steel fabrication company built with HTML, CSS, JavaScript, and PHP.

## Features

- 🌐 **Bilingual Support**: Full English and Arabic translations with RTL support
- 📱 **Fully Responsive**: Desktop, tablet, and mobile optimized
- 🏗️ **Product Showcase**: 8 product detail pages with specifications
- 📧 **Contact Form**: Email notifications via PHPMailer
- 🎨 **Modern Design**: Steel industry themed with smooth animations

## Project Structure

```
rawafid/
├── index.php           # Main homepage
├── send-email.php      # Contact form email handler
├── nav.html            # Navigation component
├── footer.html         # Footer component
├── css/
│   └── styles.css      # Main stylesheet
├── js/
│   └── main.js         # JavaScript (language switching, form handling)
├── products/
│   └── product-detail.php  # Dynamic product detail pages
├── README.md           # This file
└── products.pdf        # Product catalog reference
```

## Installation

### 1. Requirements

- Web server (Apache, Nginx, or IIS)
- PHP 7.4 or higher
- Composer (recommended for PHPMailer)

### 2. Install PHPMailer

**Option A - Using Composer (Recommended):**
```bash
composer require phpmailer/phpmailer
```

**Option B - Manual Installation:**
```bash
# Download PHPMailer from: https://github.com/PHPMailer/PHPMailer
# Extract to: PHPMailer/ folder in project root
```

### 3. Configure Email Settings

Edit `send-email.php` and configure these settings:

```php
// SMTP Server Configuration
$mail->Host = 'smtp.gmail.com';        // Your SMTP server
$mail->SMTPAuth = true;
$mail->Username = 'your-email@gmail.com';  // Your email
$mail->Password = 'your-app-password';     // App password (NOT regular password)
$mail->SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS;
$mail->Port = 587;

// Recipients
$mail->setFrom('your-email@gmail.com', 'Rawafid Website');
$mail->addAddress('admin@rawafid.com', 'Admin');  // Where to receive emails
```

### 4. Email Setup Examples

**Gmail:**
1. Enable 2-Factor Authentication on your Google account
2. Go to: https://myaccount.google.com/apppasswords
3. Create an app password
4. Use that password in `$mail->Password`

**Office 365 / Outlook:**
```php
$mail->Host = 'smtp.office365.com';
$mail->Port = 587;
$mail->SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS;
```

**Custom SMTP Server:**
```php
$mail->Host = 'mail.yourdomain.com';
$mail->Port = 465; // or 587
$mail->SMTPSecure = PHPMailer::ENCRYPTION_SMTPS; // for SSL
```

### 5. Run Locally

**Using PHP built-in server:**
```bash
php -S localhost:8000
```
Then open: http://localhost:8000

**Using Python:**
```bash
python -m http.server 8000
```

**Using XAMPP/WAMP:**
- Place project in `htdocs` or `www` folder
- Open: http://localhost/rawafid

## Usage

### Language Switching

Click the **EN / عربي** button in the navigation to switch languages. The preference is saved in localStorage.

### Product Detail Pages

Access product details by clicking on any product card or directly via:
- `products/product-detail.php?product=bridges`
- `products/product-detail.php?product=heavy-duty-buildings`
- `products/product-detail.php?product=storage-tanks`
- And more...

### Contact Form

The contact form sends emails with:
- Customer name, email, phone
- Product interest (optional)
- Message content
- Timestamp

## Available Products

1. Steel Bridges
2. Heavy Duty Buildings
3. Storage Tanks & Silos
4. Turbine Houses
5. High Tension Towers
6. Aircraft Hangars
7. Cargo Terminals
8. Pre-Engineered Buildings
9. Passenger Terminals
10. Steel Platforms
11. Equipment Support Structures
12. Petrol Station Structures

## Customization

### Colors

Edit `css/styles.css`:
```css
:root {
    --primary-red: #9f0921;      // Main accent color
    --dark: #272727;             // Background
    --gray: #6b6b6b;             // Secondary text
    --white: #ffffff;            // Text color
}
```

### Company Information

Edit in `index.php`:
- Phone numbers
- Email addresses
- Address
- Company name variations

### Add New Products

1. Add product data to `products/product-detail.php` `$products` array
2. Add card to `index.php` products section
3. Add translation keys to `js/main.js` translations object

## Production Deployment

1. **Email Configuration:**
   - Use a dedicated business email
   - Consider using transactional email services (SendGrid, Mailgun, AWS SES)

2. **Security:**
   - Enable HTTPS/SSL
   - Validate all form inputs server-side
   - Consider adding CAPTCHA

3. **Performance:**
   - Enable PHP OPcache
   - Minify CSS/JS for production
   - Use CDN for static assets

## Support

For questions about:
- **Email setup**: Contact your email provider for SMTP settings
- **Customization**: Modify CSS and translations as needed
- **Deployment**: Consult your hosting provider

## License

This project is proprietary to Rawafid Alssalb Factory.
