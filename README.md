# Vivian W. — Personal Website

A personal website showcasing Vivian's passions: **Rhythmic Gymnastics**, **Art**, and **Mathematics**.

Live at: **https://vivianw.github.io** (once GitHub Pages is enabled)

---

## Project Structure

```
vivanw/
├── index.html              ← Main page (all sections)
├── css/
│   └── style.css           ← All styles (organized with table of contents)
├── js/
│   └── main.js             ← Navigation, scroll effects, animations
├── images/
│   ├── hero.jpg            ← Hero background (optional)
│   ├── profile.jpg         ← About section photo
│   ├── gymnastics/         ← Gymnastics photos
│   ├── art/                ← Artwork images
│   ├── awards/             ← Award/certificate photos
│   ├── math/               ← Math-related images
│   └── stories/            ← Story images
├── pages/
│   └── story-template.html ← Template for individual story pages
└── README.md
```

## How to Add Content

### Adding Photos (Gymnastics or Art)

1. Put your image in the appropriate folder (`images/gymnastics/` or `images/art/`)
2. Open `index.html`
3. Find the section (search for `gymnastics-gallery` or `art-gallery`)
4. Add this block inside the gallery div:

```html
<div class="gallery-item">
  <img src="images/gymnastics/photo-name.jpg" alt="Description" loading="lazy" />
  <div class="gallery-caption">
    <p>Your caption here</p>
  </div>
</div>
```

### Adding an Award

1. Open `index.html`, find `awards-timeline`
2. Add this block:

```html
<div class="timeline-item">
  <div class="timeline-marker"></div>
  <div class="timeline-content">
    <span class="timeline-date">Month Year</span>
    <h3>Award Name</h3>
    <p>Description of the award.</p>
    <!-- Optional photo: -->
    <img src="images/awards/photo.jpg" alt="Award" loading="lazy" />
  </div>
</div>
```

### Adding a Math Highlight

Find `math-grid` in `index.html` and add:

```html
<div class="math-card">
  <div class="math-icon">🏆</div>
  <h3>Title</h3>
  <p>Description</p>
</div>
```

### Adding a Story

**Short story (on main page):**
Find `stories-grid` in `index.html` and add:

```html
<article class="story-card">
  <img src="images/stories/photo.jpg" alt="Story title" loading="lazy" />
  <div class="story-body">
    <span class="story-date">Month Day, Year</span>
    <h3>Story Title</h3>
    <p>A short preview...</p>
    <a href="pages/my-story.html" class="story-link">Read more →</a>
  </div>
</article>
```

**Full story page:**
1. Copy `pages/story-template.html` → `pages/my-story.html`
2. Edit the content in the new file
3. Link to it from the main page story card

### Updating the About Section

Find `<!-- ✏️ EDIT BIO HERE -->` in `index.html` and modify the text.

### Adding a Profile Photo

1. Save photo as `images/profile.jpg`
2. In `index.html`, find the About section
3. Remove the `<div class="photo-placeholder">...</div>` block
4. Uncomment the `<img>` line below it

## Customizing Colors

Open `css/style.css` and change the CSS variables at the top:

```css
:root {
  --color-primary: #b8336a;     /* Main accent color */
  --color-secondary: #6c63ff;   /* Secondary accent */
  --color-accent: #f4a261;      /* Warm highlight */
}
```

## Deploying

This site uses GitHub Pages. Any push to the `main` branch will automatically update the live site.
