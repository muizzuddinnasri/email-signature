# Pusat Rehabilitasi PERKESO - Corporate Email Signature

This repository serves as the centralized Content Delivery Network (CDN) and version control for the official Pusat Rehabilitasi PERKESO HTML email signature.

## 📌 Project Overview
Many enterprise email clients and strict firewalls block images hosted on free image-sharing sites or Google Drive (via proxy blocking). To ensure our corporate branding renders consistently across all external communications, this signature framework utilizes GitHub as a free, reliable CDN to host organizational assets.

### Repository Contents
* `signature.html`: The master HTML script containing the structural table layout, inline CSS (for maximum email client compatibility), and text placeholders.
* `email signature.jpg`: The active promotional banner that appears at the bottom of the email signature.

---

## ⚙️ How It Works

### 1. The Layout Architecture
The signature is built using a strict `<table>` structure rather than modern CSS grid/flexbox, as desktop email clients (like Microsoft Outlook) do not fully support modern web standards. All styling is applied inline.

### 2. Asset Hosting (The GitHub CDN)
The banner image is hardcoded into the HTML using GitHub's raw user content delivery link. 
* **Current Banner Link:** `https://raw.githubusercontent.com/muizzuddinnasri/email-signature/refs/heads/main/email%20signature.jpg`

*Note: The social media icons are dynamically generated using the Icons8 CDN to perfectly match the PERKESO maroon branding (`#8b2323`), bypassing the need to host individual icon files.*

---

## 🛠️ Maintenance & Updates

### Updating the Promotional Banner
You **do not** need to edit the HTML code or ask staff to update their Gmail settings when the campaign banner changes. 
1. Delete the current `email signature.jpg` from this repository.
2. Upload the new banner.
3. **CRITICAL:** Ensure the new file is named *exactly* `email signature.jpg`. Because the file name and path remain identical, the raw link will stay the same, and the new banner will automatically propagate to every staff member's outgoing emails globally.

### Updating the HTML Template
If organizational details, disclaimers, or branding guidelines change:
1. Edit the `signature.html` file directly in this repository to maintain version history.
2. The code must be manually redistributed to staff or pushed via Google Apps Manager (GAM) / Google Workspace Admin API.

---

## 📋 Staff Deployment Instructions
When onboarding new staff, provide them with the rendered visual of the `signature.html` file (not the raw code) and the following instructions:

1. Copy the rendered signature layout.
2. Paste it into **Gmail > Settings > Signature**.
3. Replace the text placeholders (`[ENTER FULL NAME]`, `[JAWATAN / POSITION]`, etc.) by highlighting and typing over them. **Do not press Enter** to avoid breaking the table structure.
4. Highlight `[INSERT PROFILE PICTURE]`, delete it, and use Gmail's native "Insert Image" tool to upload a professional headshot from Google Drive.
5. Save changes.
