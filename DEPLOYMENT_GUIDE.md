# 🚀 Deployment & Contact Form Setup Guide

## 📧 Contact Form Setup (Formspree)

### Step 1: Create Formspree Account
1. Go to [formspree.io](https://formspree.io)
2. Sign up for a free account
3. Create a new form
4. Copy your form ID (looks like `xpzgkqwe`)

### Step 2: Update Your Website
1. Open `index.html`
2. Find line 294: `action="https://formspree.io/f/YOUR_FORM_ID"`
3. Replace `YOUR_FORM_ID` with your actual form ID
4. Save the file

### Step 3: Test the Form
1. Deploy your website
2. Fill out the contact form
3. Check your email for the message

## 🌐 Deployment Options

### Option 1: GitHub Pages (Recommended - Free)
1. **Create GitHub Repository:**
   - Go to [github.com](https://github.com)
   - Click "New repository"
   - Name it: `ahmed-assaf-resume`
   - Make it public
   - Click "Create repository"

2. **Upload Files:**
   - Click "uploading an existing file"
   - Drag and drop your 3 files: `index.html`, `styles.css`, `script.js`
   - Commit changes

3. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: "main"
   - Click "Save"
   - Your site will be live at: `https://yourusername.github.io/ahmed-assaf-resume`

### Option 2: Netlify (Easiest - Free)
1. Go to [netlify.com](https://netlify.com)
2. Click "Add new site" → "Deploy manually"
3. Drag and drop your folder containing the 3 files
4. Get instant deployment with custom URL
5. Optional: Add custom domain

### Option 3: Vercel (Fast - Free)
1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Import your repository
4. Deploy automatically

## 🔧 Alternative Contact Form Solutions

### Option A: EmailJS (No Backend Required)
```html
<!-- Add this to your <head> -->
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>

<!-- Update your form -->
<form id="contact-form">
    <input type="text" name="from_name" placeholder="Your Name" required>
    <input type="email" name="from_email" placeholder="Your Email" required>
    <input type="text" name="subject" placeholder="Subject" required>
    <textarea name="message" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
</form>

<script>
emailjs.init("YOUR_PUBLIC_KEY");
document.getElementById('contact-form').addEventListener('submit', function(e) {
    e.preventDefault();
    emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this)
        .then(function() {
            alert('Message sent successfully!');
        }, function(error) {
            alert('Error sending message');
        });
});
</script>
```

### Option B: Netlify Forms (If using Netlify)
```html
<!-- Add netlify attribute to your form -->
<form name="contact" method="POST" data-netlify="true">
    <input type="text" name="name" placeholder="Your Name" required>
    <input type="email" name="email" placeholder="Your Email" required>
    <input type="text" name="subject" placeholder="Subject" required>
    <textarea name="message" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
</form>
```

## 📱 Custom Domain (Optional)

### For GitHub Pages:
1. Buy domain from Namecheap, GoDaddy, etc.
2. In repository Settings → Pages
3. Add custom domain
4. Update DNS records

### For Netlify:
1. Go to Site Settings → Domain Management
2. Add custom domain
3. Update DNS records

## 🎯 Quick Start Checklist

- [ ] Create Formspree account and get form ID
- [ ] Update `index.html` with your form ID
- [ ] Choose deployment platform
- [ ] Upload files to platform
- [ ] Test contact form
- [ ] Share your resume website!

## 📞 Support

If you need help with deployment or contact form setup, feel free to ask!
