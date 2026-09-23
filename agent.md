# AGENT.MD — Developer & AI Agent Guide

Welcome to the **Abhiram Financial Solutions** codebase repository. This document serves as the single source of truth for AI agents and human developers maintaining, enhancing, or extending this project.

---

## 1. Project Overview & Business Profile

- **Brand:** Abhiram Financial Solutions
- **Role:** Loan Facilitator & Direct Selling Agent (DSA)
- **Primary Market:** Pune, Maharashtra, India
- **Office Address:** Office No: T9-A1-A-1207, Floor No: 12, BramhaCorp Business Park, Vadgaonsheri, Pune - 411014
- **Primary Contact Number:** `+91 90224 88094`
- **Primary Email:** `contact@abhiramfinance.com`
- **WhatsApp Integration Endpoint:** `https://wa.me/919022488094`
- **Deployment Platform:** GitHub Pages (`abhiramloancode.github.io`) / custom domain (`abhiramfinance.com`)

---

## 2. Technology Stack & Architecture

This is a lightweight, high-performance static Single Page Application (SPA) requiring zero build steps or heavy node frameworks:

| Component | Technology | Implementation Details |
| :--- | :--- | :--- |
| **Markup** | Semantic HTML5 | Structured with accessibility in mind, SEO meta tags, and Schema.org JSON-LD |
| **Styling** | Tailwind CSS CDN | Loaded via `https://cdn.tailwindcss.com` with custom theme configuration |
| **Typography** | Google Fonts | `Plus Jakarta Sans` font family loaded via Google Fonts CDN |
| **Icons** | Lucide Icons | Loaded via `https://unpkg.com/lucide@latest` (`lucide.createIcons()`) |
| **Interactivity** | Vanilla JavaScript | Self-contained in `<script>` at the bottom of [index.html](file:///Users/rahul/codes/abhiramloancode.github.io/index.html) |
| **Hosting** | Static Web Server | Python `http.server`, Nginx, GitHub Pages, or any static host |

### Color Design System
Tailwind configuration (`tailwind.config`) defines the following brand palette:
- `brand-navy`: `#0F172A` (deep dark slate/navy background and headings)
- `brand-navyLight`: `#1E293B`
- `accent`: `#059669` (emerald-600 — primary call-to-action color)
- `accent-hover`: `#047857` (emerald-700)
- `accent-light`: `#ECFDF5` (emerald-50)
- `gold`: `#D97706` (amber-600)
- `gold-light`: `#FEF3C7` (amber-50)

---

## 3. Repository Structure

```
abhiramloancode.github.io/
├── assets/
│   └── image.png          # Primary brand logo & website favicon
├── index.html             # Entire website markup, styles, logic, SEO & Schema.org JSON-LD
├── robots.txt             # Search crawler directives and sitemap pointers
├── sitemap.xml            # XML sitemap for Google & search indexing
├── README.md              # Repository header
└── agent.md               # This specification and instructions file
```

---

## 4. Key Page Sections & Component Details

### 1. Sticky Navigation Bar (`<nav>`)
- Brand logo linked to scroll-to-top.
- Desktop navigation links with smooth-scrolling anchors (`#products`, `#partners`, `#calculator`, `#comparison`, `#testimonials`, `#eligibility`, `#faqs`).
- Header CTA with click-to-call (`tel:+919022488094`) and WhatsApp application button.
- Responsive mobile hamburger menu with dropdown drawer.

### 2. Ambient Hero Section (`#apply-section`)
- Deep navy background with ambient blurred radial glows (`bg-emerald-500/15`).
- Social proof badge: `⭐ 4.8/5 Rating • 10,000+ Pune Borrowers`.
- Key trust pills: 24-48h Disbursal, 100% Digital KYC, Rates from 8.40% p.a.
- **Two-Step Application Card:**
  - **Step 1:** Loan type radio selection (Personal, Business, Home, LAP, Used Car, BT), loan amount input with preset chips (₹1L, ₹3L, ₹5L, ₹10L, ₹25L), and income/turnover field. Contextual labels update automatically when selecting Business/LAP.
  - **Step 2:** Full Name (as per PAN), Mobile Number (+91 validation), Employment status, Pune Pincode, and consent checkbox.
  - **Submission:** Formats application data into a WhatsApp message and redirects to `wa.me/919022488094`.

### 3. Partner Network & Lending Ecosystem (`#partners`)
- Showcases 10 premier Indian banking and NBFC partners: HDFC Bank, ICICI Bank, SBI Bank, Axis Bank, Kotak Bank, Bajaj Finserv, Tata Capital, IDFC FIRST Bank, Aditya Birla Capital, and L&T Finance.
- Metrics summary: ₹50+ Cr Disbursed, 24-48h Disbursals, 25+ Partners, 256-bit Security.

### 4. Loan Products Section (`#products`)
- 6 product cards with distinct badges and rate callouts:
  - Personal Loans (`Most Popular`, from 10.25% p.a.)
  - Business Loans (`Express Business`, from 13.50% p.a.)
  - Home Loans (`Lowest Rates`, from 8.40% p.a.)
  - Loan Against Property (`High Sanction`, from 9.25% p.a.)
  - Used Car Loan (`Quick Valuation`, from 11.00% p.a.)
  - Balance Transfer + Top-Up (`Max Savings`, save up to 3% APR)
- Each card has a `prefillForm(type)` button that auto-selects the radio button in the hero form and smoothly scrolls to it.

### 5. Interactive EMI Calculator (`#calculator`)
- Dynamic sliders for:
  - **Loan Amount:** ₹50,000 to ₹50,00,000 (step ₹50,000)
  - **Interest Rate:** 8.5% to 24.0% p.a. (step 0.5%)
  - **Tenure:** 1 to 7 Years (step 1 Year)
- Real-time recalculation of Monthly EMI, Principal Amount, Total Interest, and Total Payable.
- **Visual Breakdown Gauge:** Live two-tone bar showing percentage distribution of Principal vs. Interest.
- Direct CTA: "Apply for [Selected Amount]".

### 6. 3-Step Borrowing Workflow
- 1. Submit Requirement (60-sec form / WhatsApp)
- 2. Digital Verification & Lenders Comparison
- 3. Sanction & Disbursal

### 7. "Why Choose Us vs Direct Bank Visit" Comparison Matrix (`#comparison`)
- Side-by-side comparison table contrasting Abhiram's multi-lender DSA advantage against visiting a single bank branch across:
  - Lender Choices (25+ vs 1)
  - Interest Rate Bidding (Lowest Market APR vs Standard Rack Rate)
  - Credit Score Safety (Zero CIBIL impact soft pull vs Multiple hard inquiries)
  - Approval Probability (95%+ match rate vs High rejection risk)
  - Paperwork & Convenience (100% Digital / Doorstep vs Branch queues)
  - Consultation Fee (100% Free Consultation vs Hidden cross-selling)

### 8. Verified Pune Customer Testimonials (`#testimonials`)
- 3 authentic Pune borrower experiences featuring loan amounts, ratings, and locations (Hinjawadi Phase 2, Baner, Viman Nagar).

### 9. Eligibility Criteria & Documents Checklist (`#eligibility`)
- Tabbed interface switching between **Salaried Employee** and **Self-Employed / Business** with detailed document checklists.

### 10. Frequently Asked Questions (`#faqs`)
- Interactive accordions addressing CIBIL impact, upfront fees, disbursal timeline, and cash salary eligibility.

### 11. Footer & Disclaimers
- Office address, contact links, legal DSA disclaimer, and copyright.

### 12. Persistent Floating CTAs
- **Desktop Floating WhatsApp Pill (`hidden md:flex`):** Fixed bottom-right with pulsating online badge.
- **Mobile Bottom Action Bar (`md:hidden`):** Fixed bottom bar with "Call Now" and "Apply on WA". Sits flush with `bottom-0` without bottom padding or lines.

---

## 5. WhatsApp Lead Routing Format

When a user submits the hero form, `handleFormSubmit()` generates the following message template and opens `https://wa.me/919022488094?text=...`:

```text
*New Loan Inquiry — Abhiram Financial Solutions*
────────────────────────────
• *Name:* [Full Name]
• *Mobile:* [Mobile Number]
• *Loan Type:* [Selected Loan Type]
• *Required Amount:* ₹[Formatted Amount]
• *Income/Turnover:* ₹[Formatted Income]
• *Employment:* [Salaried / Self-Employed]
• *Pincode:* [Pune Pincode]
────────────────────────────
_Submitted via abhiramfinance.com_
```

---

## 6. Development & Maintenance Guidelines

### Running Locally
To test the site locally, launch any static HTTP server in the repository root:
```bash
python3 -m http.server 8080
```
Open `http://localhost:8080/` in your browser.

### Rules for Editing [index.html](file:///Users/rahul/codes/abhiramloancode.github.io/index.html)
1. **Preserve Dynamic Icon Rendering:**
   - Lucide renders icons using `<i data-lucide="icon-name"></i>`.
   - Any dynamic DOM changes or step transitions MUST trigger `lucide.createIcons()` so newly rendered elements display their SVG icons.
2. **Mobile Layout & Z-Index Hierarchy:**
   - Sticky navbar: `z-50`, `sticky top-0`.
   - Mobile action bar: `z-50`, `fixed bottom-0`.
   - Floating desktop WhatsApp pill: `z-40`, `fixed bottom-6 right-6`, with `hidden md:flex`.
   - **Crucial:** Never add bottom margins or safe-area padding to `#mobile-action-bar` that exposes the background as a white line beneath the buttons. The buttons must remain flush to the viewport bottom.
3. **Number Formatting:**
   - Always format currency using `new Intl.NumberFormat('en-IN')` to adhere to Indian numbering standards (e.g., `₹ 5,00,000`).
4. **Anchor Offsets:**
   - Sections must include `scroll-mt-20` (or `scroll-mt-24`) so scrolling to an anchor does not conceal headings under the `h-20` sticky navbar.
5. **Favicon & Brand Assets:**
   - The favicon and logo both reference [assets/image.png](file:///Users/rahul/codes/abhiramloancode.github.io/assets/image.png). Do not remove or relocate this asset without updating all `<link rel="icon">` and `<img>` tags.
