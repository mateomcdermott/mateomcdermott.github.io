# Mateo McDermott — Portfolio

Personal portfolio site. Built with plain HTML, CSS, and vanilla JS. No frameworks, no build step.

## Live Site

`https://mateomcdermott.github.io`

## File Structure

```
├── index.html                          ← Main portfolio page
├── resume.pdf                          ← Your resume (add this)
├── case-studies/
│   ├── financial-dashboard.html
│   ├── opm-meg-helmet.html
│   └── prosthetics.html
└── README.md
```

## Deploying to GitHub Pages

### 1. Create the repository

Go to [github.com/new](https://github.com/new) and create a repo named **`mateomcdermott.github.io`** (replace with your actual GitHub username). This special naming convention tells GitHub to serve it as your user site.

- Set it to **Public**
- Do NOT initialize with a README (we already have one)

### 2. Push your code

Open your terminal in this project folder and run:

```bash
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/mateomcdermott/mateomcdermott.github.io.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Set branch to `main` and folder to `/ (root)`
4. Click **Save**

Your site will be live at `https://mateomcdermott.github.io` within a minute or two.

### 4. Custom domain (optional)

If you own a domain like `mateomcdermott.com`:

1. In repo Settings → Pages, enter your custom domain
2. Add a CNAME record with your DNS provider pointing to `mateomcdermott.github.io`
3. Check "Enforce HTTPS"

## Customizing

### Adding images to case studies

Replace the placeholder `<div class="placeholder-img">` blocks with actual images:

```html
<!-- Replace this: -->
<div class="placeholder-img"><span>Screenshot — replace</span></div>

<!-- With this: -->
<img src="../images/dashboard-screenshot.png" alt="Financial dashboard overview"
     style="width:100%; border:1px solid var(--border); margin:2rem 0;" />
```

Create an `images/` folder and add your screenshots, renders, and photos there.

### Adding your resume

Drop your `resume.pdf` file in the root directory alongside `index.html`.

### Contact form

The current form uses `mailto:` which opens the user's email client. For a proper backend, consider:
- [Formspree](https://formspree.io) (free tier available)
- [Netlify Forms](https://docs.netlify.com/forms/setup/) (if you move to Netlify)

To use Formspree, replace the form action:
```html
<form class="contact-form" action="https://formspree.io/f/YOUR_ID" method="POST">
```

## Tech

- Zero dependencies
- Dark mode with system preference detection + localStorage persistence
- Scroll-triggered animations via IntersectionObserver
- Fully responsive
