# BizFlow Solutions - Business Software & POS Portfolio Website

A simple, modern, minimal, and responsive portfolio website for **BizFlow Solutions**, providing affordable digital solutions for small businesses, retail shops, supermarkets, mobile stores, and meat shops.

Built with **React**, **Vite**, and **Tailwind CSS**. Designed with a clean white background, dark typography, subtle blue accents, and a premium SaaS-style aesthetic.

---

## 🚀 Key Features

- **Tagline & Hero Section**: "Smart Tools. Simpler Business." with clear value propositions and trust badges.
- **Interactive Billing Dashboard Mockup**:
  - 🧾 **Live POS Counter Simulator**: Add items, adjust quantities, calculate discounts, break down GST (CGST + SGST), toggle payment methods (Cash, UPI QR, Card), and test thermal receipt printing.
  - 📊 **Sales & GST Ledger**: Real-time sales metrics, payment split (UPI vs Cash), and invoice logs.
  - 📦 **Live Inventory & Low-Stock Alerts**: Stock health bars and threshold warnings.
- **6 Core Small-Business Services**:
  1. Billing & POS Software (barcode scanning, thermal printers, UPI/Cash)
  2. Inventory & Stock Management (real-time alerts, expiry tracking, purchase orders)
  3. GST Invoicing, Sales & Expense Tracking (B2B & B2C tax invoices, GSTR reports)
  4. Mobile Shop & Meat Shop Billing Systems (IMEI warranty tracking & electronic scale sync)
  5. Business Websites & E-Commerce (modern showcase with WhatsApp ordering)
  6. Custom Software Solutions (tailored ERPs, order tracking, internal portals)
- **Specialized Demo Systems**: Interactive showcases for Retail Groceries, Mobile Stores, Butcheries, GST Portals, and Online Catalogs with sample receipt generation.
- **Interactive "Get a Quote" Engine**:
  - On-page interactive quote builder with business-type selector and module checkboxes.
  - Generates a pre-filled, professional WhatsApp enquiry message in one click.
  - Global popup modal accessible from every button across the site.
- **WhatsApp Integration**:
  - One-click click-to-chat links pre-filled with context-aware service queries.
  - Floating WhatsApp action button in the bottom-right corner.
- **100% Authentic & Transparent**:
  - Zero fake client claims or fabricated testimonials.
  - Highlighting real technical advantages: offline-first operation, hardware compatibility, and no expensive monthly fees.
- **Zero Paid APIs**: Completely self-contained, lightweight, and beginner-friendly.

---

## 📁 Project Structure

```
portfolio/
├── index.html                   # HTML template with SEO tags & Inter font
├── tailwind.config.js           # Tailwind CSS configuration with light SaaS palette
├── vite.config.js               # Vite bundler config
├── package.json                 # Project dependencies & scripts
├── public/                      # Static assets & icons
└── src/
    ├── main.jsx                 # React root mount
    ├── App.jsx                  # Main application container
    ├── config.js                # Central company info & WhatsApp URL helper
    ├── index.css                # Base Tailwind styles & clean scrollbars
    ├── data/
    │   ├── servicesData.js      # 6 core service definitions & features
    │   ├── demoProjectsData.js  # 5 specialized demo systems & sample bills
    │   └── whyChooseUsData.js   # Value propositions & comparison matrix
    └── components/
        ├── Navbar.jsx           # Responsive header with quote & WhatsApp CTAs
        ├── Hero.jsx             # Tagline, value chips, and dashboard preview
        ├── DashboardPreview.jsx # Interactive POS billing simulator & reports
        ├── Services.jsx         # 6 core service cards with feature checkmarks
        ├── DemoProjects.jsx     # Tabbed demo systems with hardware specs & bills
        ├── WhyChooseUs.jsx      # 6 value pillars & ERP comparison table
        ├── About.jsx            # Mission, philosophy, and engineering metrics
        ├── QuoteSection.jsx     # Interactive quote calculator & WhatsApp builder
        ├── QuoteModal.jsx       # Reusable pop-up modal for all "Get a Quote" buttons
        ├── Contact.jsx          # Direct contact info, enquiry form, and FAQs
        ├── Footer.jsx           # Clean footer with quick links & back-to-top
        └── WhatsAppButton.jsx   # Floating WhatsApp button
```

---

## 🛠️ Local Development Setup

### 1. Prerequisites
Ensure you have **Node.js** (version 18 or higher) installed on your computer. You can check by running:
```bash
node -v
```

### 2. Install Dependencies
Open your terminal in the project directory and install the necessary packages:
```bash
npm install
```

### 3. Run the Development Server
Start the local Vite development server:
```bash
npm run dev
```
Open your browser and navigate to the local URL (usually `http://localhost:5173`).

### 4. Build for Production
To create an optimized production bundle:
```bash
npm run build
```
The output files will be generated in the `dist/` directory.

---

## ⚙️ Customization Guide

### Changing Company Details & WhatsApp Number
Open `src/config.js` to update:
```javascript
export const COMPANY_CONFIG = {
  name: "BizFlow Solutions",
  whatsappNumber: "+919876543210", // Enter your 10-digit WhatsApp number with country code
  whatsappDisplay: "+91 98765 43210",
  phoneDisplay: "+91 98765 43210",
  email: "bizflowsolutions@gmail.com",
  location: "Pan-India Remote Support & On-Site Setup",
  workingHours: "Monday – Saturday: 9:00 AM – 8:00 PM IST",
};
```
All WhatsApp links, contact cards, modals, and footer details across the entire website will automatically reflect your changes.

---

## 🌐 100% Free Deployment Steps

You can host this website completely for free using any of the following platforms:

### Option A: Deploy to Vercel (Recommended - Easiest)

1. **Via GitHub (Automated CI/CD)**:
   - Push your code to a GitHub repository.
   - Go to [vercel.com](https://vercel.com/) and sign in with GitHub.
   - Click **Add New Project** and select your repository.
   - Framework Preset will automatically detect **Vite**.
   - Click **Deploy**. Your website will be live with a free SSL certificate in under 1 minute!

2. **Via Vercel CLI (Direct from Terminal)**:
   ```bash
   npm install -g vercel
   vercel
   ```
   Follow the simple prompts in your terminal.

---

### Option B: Deploy to Netlify

1. **Via Netlify Drop (No Git required)**:
   - Run `npm run build` locally.
   - Open [app.netlify.com/drop](https://app.netlify.com/drop).
   - Drag and drop the generated `dist` folder into the browser window.
   - Netlify will immediately publish your website with a free `.netlify.app` subdomain.

2. **Via Netlify Git Integration**:
   - Push your code to GitHub/GitLab.
   - Go to [netlify.com](https://www.netlify.com/) and click **Add new site > Import an existing project**.
   - Set Build command to `npm run build` and Publish directory to `dist`.
   - Click **Deploy Site**.

---

### Option C: Deploy to GitHub Pages

1. In `vite.config.js`, set `base`:
   ```javascript
   export default defineConfig({
     plugins: [react()],
     base: '/<YOUR-REPO-NAME>/', // Replace with your repository name
   });
   ```
2. Install `gh-pages`:
   ```bash
   npm install --save-dev gh-pages
   ```
3. Add deploy scripts to `package.json`:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
4. Run:
   ```bash
   npm run deploy
   ```

---

## 📄 License
This project is open-source and free to use for personal or commercial projects.
