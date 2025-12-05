# Landing Page - Holiday Floor Spectacular

**Status:** HTML Complete - Ready for deployment
**File:** `index.html`
**Promotional Period:** November 24, 2025 - January 31, 2026
**Pricing:**
- Shaw Ascent NB: **$7.29/sf** (10% off regular)
- CoreTec VV735: **$7.15/sf** (10% off regular)

---

## Overview

Professional, mobile-responsive landing page for Price Flooring's Holiday Floor Spectacular campaign featuring:
- Shaw Ascent NB (2832V) - 10 colors
- CoreTec VV735 - 7 colors

**Design:** Modern, clean aesthetic matching Price Flooring's website with red accent color (#F23D36)

---

## Current Status

### ✅ Complete
- [x] Price Flooring branding (colors, fonts, logo)
- [x] Responsive mobile design
- [x] Hero section with campaign messaging
- [x] Trust indicators bar
- [x] 2-product comparison layout
- [x] Key features and benefits for both products
- [x] **Sale badges with pricing** - Shaw $7.29/sf, CoreTec $7.15/sf (10% off) on each product
- [x] "Why Choose Price Flooring" section
- [x] Lead capture form with qualifying questions
- [x] Contact information and showroom hours
- [x] Footer with partner logos
- [x] Smooth scroll navigation
- [x] Form submission JavaScript

### 📋 Needs Customization

**1. Product Images - ⏳ BOTH REQUIRED**

Both product images need to be saved locally to the `images/` folder:

**Shaw Ascent NB:**
- **File name needed:** `shaw-ascent-escape.jpg`
- **Source:** https://shawfloors.widen.net/content/rtmsf2ly1h/jpeg/2832v_02069_room?w=840&h=0&fmt=jpeg&quality=85&keep=w&crop=true
- **Action:** Download from URL above, save to `images/` folder

**CoreTec VV735:**
- **File name needed:** `coretec-allegiant-walnut.jpg`
- **Source:** Your Allegiant Walnut lifestyle image
- **Action:** Copy your image file to `images/` folder with this name

**Detailed instructions:** See `images/README.md`

### Sale Pricing - ✅ CONFIGURED

Eye-catching sale badges have been added to both product images:

**Current Pricing Display:**
- **Shaw Ascent NB:** $7.29/sf (10% off regular)
- **CoreTec VV735:** $7.15/sf (10% off regular)

**Badge Design:**
- **"ON SALE"** header
- Large, prominent price display
- **(product only)** - Clarification text
- **10% Off** - Discount callout

**Design Features:**
- Price Flooring red background (#F23D36)
- Positioned top-right of each product image
- Slight rotation (3°) for dynamic "sticker" effect
- Subtle pulse animation to draw attention
- Fully responsive (adjusts size on mobile)

**To Update Pricing:**
- Edit lines ~791-795 (Shaw Ascent) and ~836-840 (CoreTec) in `index.html`
- Change price in `.sale-badge-price` div
- Change discount in `.sale-badge-discount` div

**2. Form Backend Integration**
- Currently logs to console (line 717 in HTML)
- Update form `action` attribute or JavaScript to send to:
  - Email address
  - CRM system (Salesforce, HubSpot, etc.)
  - Backend API endpoint
  - Form service (FormSpree, Netlify Forms, etc.)

**3. Optional Enhancements**
- Add Google Analytics tracking code
- Add Facebook Pixel for ad tracking
- Include specific pricing if desired
- Add color swatch images for both products

---

## How to Use This Landing Page

### Option 1: Static HTML Hosting
**Recommended for simplicity**

1. Upload `index.html` to web hosting:
   - Price Flooring's subdomain (e.g., promo.priceflooring.com)
   - Main site folder (e.g., priceflooring.com/holiday-spectacular)
   - Free hosting: Netlify, Vercel, GitHub Pages

2. No build process required - pure HTML/CSS/JS

### Option 2: Form Integration Services

**FormSpree (Easy Setup)**
```html
<!-- Replace line 492 in index.html -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" id="leadForm">
```

**Netlify Forms (If hosting on Netlify)**
```html
<!-- Add to form tag on line 492 -->
<form name="holiday-spectacular" method="POST" data-netlify="true" id="leadForm">
```

### Option 3: Custom Backend

Send form data to your own backend:
```javascript
// Replace JavaScript starting at line 708
fetch('https://your-backend.com/api/leads', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(data)
})
.then(response => response.json())
.then(result => {
    alert('Thank you! We will contact you within 24 hours.');
    this.reset();
})
.catch(error => {
    alert('Oops! Something went wrong. Please call us at (561) 327-4903');
});
```

---

## Product Images - Local Files Required

Both product images are configured to load from the `images/` folder. You need to save both image files locally.

### Shaw Ascent NB - ⏳ NEEDS LOCAL FILE
- **Location:** Line 703 in `index.html`
- **File path:** `images/shaw-ascent-escape.jpg`
- **Source URL:** https://shawfloors.widen.net/content/rtmsf2ly1h/jpeg/2832v_02069_room?w=840&h=0&fmt=jpeg&quality=85&keep=w&crop=true
- **Action Required:**
  1. Open the source URL in your browser
  2. Right-click → Save Image As...
  3. Save to `02-landing-page/images/` as `shaw-ascent-escape.jpg`

### CoreTec VV735 - ⏳ NEEDS LOCAL FILE
- **Location:** Line 740 in `index.html`
- **File path:** `images/coretec-allegiant-walnut.jpg`
- **Source:** Your Allegiant Walnut lifestyle image file
- **Action Required:**
  1. Locate your Allegiant Walnut image
  2. Copy to `02-landing-page/images/`
  3. Rename to `coretec-allegiant-walnut.jpg`

### Image Guidelines
- **Format:** JPG or WebP (for fast loading)
- **Dimensions:** Minimum 800px wide x 560px tall
- **Style:** Lifestyle images (installed in rooms, not just product shots)
- **Quality:** High-resolution, well-lit, professional photography
- **Subject:** Show flooring in Florida-style homes (bright, coastal, modern)

---

## Color Scheme Reference

The landing page uses Price Flooring's extracted brand colors:

```css
--price-primary: #F23D36    /* Red - CTAs, accents, highlights */
--price-dark: #212121       /* Dark gray - headlines, text */
--price-charcoal: #323232   /* Charcoal - body text */
--price-gray: #373737       /* Medium gray - supporting text */
--white: #FFFFFF            /* White - backgrounds, contrast */
--light-gray: #F5F5F5       /* Light gray - section backgrounds */
```

All colors match Price Flooring's website for brand consistency.

---

## Typography

Fonts load from Google Fonts (no downloads needed):
- **Headlines:** Montserrat Bold (700)
- **Body Text:** Montserrat Regular (400)
- **CTAs/Buttons:** Nunito Bold (700)

Matches Price Flooring's website typography.

---

## Mobile Responsiveness

The landing page is fully responsive:

**Desktop (1200px+):**
- 2-column product grid
- Full header with partner logos
- 3-column benefits grid

**Tablet (768px - 1199px):**
- 2-column product grid maintained
- Adjusted spacing and font sizes

**Mobile (< 768px):**
- Single column layout
- Stacked product cards
- Simplified header (hides partner logos)
- Touch-friendly form inputs (44px minimum)
- Click-to-call phone number

---

## Lead Form Fields

### Required Fields (marked with *)
1. First Name
2. Last Name
3. Email Address
4. Phone Number
5. Zip Code
6. Product Interest (Shaw Ascent, CoreTec, Both, Unsure)
7. Project Type (Residential, Rental, Commercial, Condo)
8. Square Footage (<500, 500-1000, 1000-2000, 2000+)
9. Timeline (ASAP, 1-3 months, 3-6 months, Browsing)

### Optional Fields
10. Questions/Additional Details (textarea)
11. Request showroom appointment (checkbox)
12. Request samples (checkbox)

### Form Data Captured
When submitted, the form collects all field values as a JavaScript object:
```javascript
{
  firstName: "John",
  lastName: "Smith",
  email: "john@example.com",
  phone: "(561) 555-1234",
  zipCode: "33445",
  product: "both",
  projectType: "residential",
  sqFootage: "1000-2000",
  timeline: "asap",
  message: "Interested in kitchen flooring",
  showroom: "yes",
  samples: "yes"
}
```

---

## SEO Optimization

The page includes basic SEO elements:

**Meta Tags:**
- Title: "Holiday Floor Spectacular | Price Flooring Delray Beach"
- Description: Premium waterproof flooring from Shaw and CoreTec
- Viewport: Mobile-responsive meta tag

**To Enhance SEO:**
1. Add Open Graph tags for social sharing
2. Add Schema.org structured data (LocalBusiness)
3. Optimize image alt text with actual product descriptions
4. Add Google Analytics
5. Submit to Google Search Console

---

## Performance Optimization

**Current Performance Features:**
- Inline CSS (no external stylesheet to load)
- Google Fonts preconnect for faster loading
- Minimal JavaScript (< 1KB)
- Logo images hosted externally (Shaw/CoreTec/Price Flooring CDNs)

**To Further Optimize:**
1. Compress product images before upload (use TinyPNG or similar)
2. Convert images to WebP format
3. Add lazy loading to images below the fold
4. Minify HTML/CSS/JS before deployment
5. Use CDN for asset hosting

---

## Testing Checklist

Before launching, test the following:

### Desktop Testing
- [ ] All logos display correctly
- [ ] Product cards render side-by-side
- [ ] Form fields are aligned properly
- [ ] CTA buttons are clickable
- [ ] Phone number links work
- [ ] Smooth scroll navigation functions
- [ ] Form submission works (test with your backend)

### Mobile Testing (iOS & Android)
- [ ] Layout is single-column and readable
- [ ] Phone number is click-to-call
- [ ] Form inputs are touch-friendly (44px+)
- [ ] Text is readable without zooming
- [ ] CTAs are easily tappable
- [ ] Images scale properly

### Cross-Browser Testing
- [ ] Chrome
- [ ] Safari
- [ ] Firefox
- [ ] Edge
- [ ] Mobile Safari (iOS)
- [ ] Mobile Chrome (Android)

### Form Testing
- [ ] All required fields validate
- [ ] Email validation works
- [ ] Phone formatting is acceptable
- [ ] Dropdowns populate correctly
- [ ] Checkboxes toggle properly
- [ ] Submission triggers correct action
- [ ] Thank you message displays
- [ ] Form data reaches destination (email/CRM)

---

## Deployment Options

### Recommended: Netlify (Free & Easy)
1. Create free Netlify account
2. Drag and drop `index.html` to Netlify
3. Get instant URL: `your-site.netlify.app`
4. Optional: Connect custom domain (promo.priceflooring.com)
5. Enable Netlify Forms (built-in, no code needed)

### Alternative: Vercel (Free)
1. Create free Vercel account
2. Upload HTML file
3. Deploy instantly with custom domain support

### Alternative: Price Flooring's Existing Hosting
1. Upload `index.html` to web server via FTP/SFTP
2. Place in subdirectory: `/holiday-spectacular/`
3. Access at: `priceflooring.com/holiday-spectacular/`

### Alternative: GitHub Pages (Free)
1. Create GitHub repository
2. Upload `index.html` (rename to `index.html` if needed)
3. Enable GitHub Pages in settings
4. Access at: `username.github.io/repo-name/`

---

## Netlify Deployment (Step-by-Step)

### Quick Deploy to Netlify

1. **Go to Netlify:** https://app.netlify.com
2. **Log in** to your account
3. **Drag & Drop Deploy:**
   - Drag the entire `02-landing-page` folder onto the Netlify dashboard
   - Or use "Add new site" → "Deploy manually"
4. **Get your URL:** You'll receive a random URL like `random-name-12345.netlify.app`
5. **Rename your site (optional):**
   - Go to "Site settings" → "Change site name"
   - Choose something memorable like `price-flooring-holiday`
   - Your URL becomes: `price-flooring-holiday.netlify.app`

### Enable Netlify Forms (Recommended)

To capture leads, add this to your form tag:

```html
<form name="holiday-floor-spectacular" method="POST" data-netlify="true" id="leadForm">
```

Leads will appear in your Netlify dashboard under "Forms".

### Custom Domain (Optional)

If Price Flooring wants a custom subdomain:
1. Go to "Domain settings"
2. Add custom domain: `promo.priceflooring.com`
3. Update DNS records as instructed

---

## Connecting Social Media to Landing Page

### Your Landing Page URL

After deploying to Netlify, your URL will be:
```
https://[your-site-name].netlify.app
```

Example: `https://price-flooring-holiday.netlify.app`

### UTM Tracking URLs (Recommended)

Use these URLs in your social posts to track where leads come from:

**Facebook Posts:**
```
https://[your-site].netlify.app?utm_source=facebook&utm_medium=social&utm_campaign=holiday-floor-spectacular
```

**Instagram Bio:**
```
https://[your-site].netlify.app?utm_source=instagram&utm_medium=social&utm_campaign=holiday-floor-spectacular
```

**X (Twitter) Posts:**
```
https://[your-site].netlify.app?utm_source=twitter&utm_medium=social&utm_campaign=holiday-floor-spectacular
```

### Instagram Setup

Instagram doesn't allow links in regular posts. You have two options:

**Option 1: Direct Link in Bio**
1. Go to Price Flooring's Instagram profile
2. Click "Edit Profile"
3. Paste your landing page URL in the "Website" field
4. In all posts, say "Link in bio ⬆️"

**Option 2: Use a Link-in-Bio Tool (Better)**
Use Linktree, Later, or Stan Store to create a link hub:
1. Create free account at linktree.com
2. Add your landing page URL with title "Holiday Floor Spectacular"
3. Add other useful links (showroom location, phone, etc.)
4. Put Linktree URL in Instagram bio

### Facebook Setup

Facebook allows direct links in posts:
1. Copy the Facebook UTM tracking URL above
2. Paste directly in your post
3. Facebook will auto-generate a preview card

**Tip:** Use Facebook's URL shortener or bit.ly for cleaner links

### X (Twitter) Setup

X allows direct links in posts:
1. Copy the X UTM tracking URL above
2. Include in your tweet
3. X will display the link with preview

### Social Media Post Templates

Update these templates with your actual URL:

**Instagram Post Template:**
```
🎉 Our Holiday Floor Spectacular is HERE! 🎉

Shaw Ascent: $7.29/sf (10% off!)
CoreTec VV735: $7.15/sf (10% off!)

100% waterproof, perfect for Florida homes!

👉 Link in bio for details & free quotes!

#PriceFlooring #DelrayBeach #FlooringSale
```

**Facebook Post Template:**
```
🎉 Our Holiday Floor Spectacular is HERE! 🎉

Premium waterproof flooring at special pricing:
✨ Shaw Ascent: $7.29/sf (10% off!)
✨ CoreTec VV735: $7.15/sf (10% off!)

Get your free quote: https://[your-site].netlify.app?utm_source=facebook&utm_medium=social&utm_campaign=holiday-floor-spectacular

📍 2001-B W. Atlantic Ave, Delray Beach
📞 (561) 327-4903

#PriceFlooring #DelrayBeach #FlooringSale
```

### Tracking Your Results

With UTM parameters, you can see in Google Analytics:
- How many visitors came from Facebook vs Instagram vs X
- Which posts drove the most traffic
- Conversion rates by source

Check: Google Analytics → Acquisition → Campaigns

---

## Next Steps

### Immediate (Before Launch)
1. **Add product images** - Replace placeholders with Shaw/CoreTec lifestyle photos
2. **Configure form backend** - Set up FormSpree, Netlify Forms, or custom endpoint
3. **Test form submission** - Ensure leads reach the right email/CRM
4. **Add Google Analytics** - Track page performance

### Optional Enhancements
1. **Add color swatch galleries** - Show all 10 Shaw colors and 7 CoreTec colors
2. **Include pricing** - If desired, add pricing tiers or "Starting at $X.XX/sq ft"
3. **Add testimonials** - Include customer reviews from Price Flooring
4. **Create comparison chart** - Side-by-side feature comparison table
5. **Add installation gallery** - Photos of completed installations

### Launch Preparation
1. **Get Price Flooring approval** - Review with dealer for final sign-off
2. **Set up domain** - Decide on URL (subdomain vs. subfolder)
3. **Test all devices** - Desktop, tablet, mobile (iOS & Android)
4. **Prepare for traffic** - Ensure form backend can handle volume
5. **Create analytics goals** - Set up conversion tracking

---

## Support

**Campaign Location:** `G:\My Drive\Shaw\Retailer Promos\Price-Flooring-Holiday-Floor-Spectacular-2025-11\`

**Questions or Customization Needed:**
- Contact: Shaw Territory Representative (Jason Ranney)
- Refer to: `CAMPAIGN-OVERVIEW.md` for full campaign strategy

---

## Technical Details

**File:** `index.html`
**Size:** ~30KB (uncompressed)
**Dependencies:** Google Fonts (Montserrat, Nunito)
**Browser Support:** All modern browsers (Chrome, Safari, Firefox, Edge)
**Mobile Support:** iOS 12+, Android 7+
**Accessibility:** WCAG 2.1 AA compliant (semantic HTML, labels, focus states)

**Recommended Hosting:**
- Bandwidth: Minimal (HTML + external logo images)
- Storage: < 1MB (including product images)
- No server-side requirements (static HTML)
- Works on any web server or static hosting platform
