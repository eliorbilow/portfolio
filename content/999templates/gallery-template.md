---
title: Gallery Template
description: A template for creating image galleries in your Quartz website
tags: gallery, template, images
draft: false
layout: default
gallery:
  columns: 3
  spacing: medium
  lightbox: true
---

# Gallery Template

This template provides a structured way to organize and display image galleries in your Quartz website.

## How to Use This Template

1. **Copy this file** and rename it to your gallery name (e.g., `my-photo-gallery.md`)
2. **Edit the frontmatter** at the top to customize title, description, and gallery settings
3. **Add images** using the gallery image syntax below
4. **Customize sections** as needed for your content

---

## Gallery Settings Reference

The `gallery` section in frontmatter controls the appearance:

- **columns**: Number of columns (2, 3, 4, or auto)
- **spacing**: Gap between images (small, medium, large)
- **lightbox**: Enable lightbox/modal view (true/false)

---

## Simple Gallery

The simplest way to display images is using standard markdown image syntax:
<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem;">

![[gallery-template-1781878787050.webp]]
![[gallery-template-1781878809094.webp]]
![[gallery-template-1781878829259.webp]]

</div>
---

## Gallery with Captions

For images with captions, you can use this enhanced HTML structure:

```html
<div class="gallery-grid">
  <figure class="gallery-item">
    <img src="../assets/images/image1.jpg" alt="Description">
    <figcaption>Image Caption or Title</figcaption>
  </figure>
  <figure class="gallery-item">
    <img src="../assets/images/image2.jpg" alt="Description">
    <figcaption>Image Caption or Title</figcaption>
  </figure>
  <figure class="gallery-item">
    <img src="../assets/images/image3.jpg" alt="Description">
    <figcaption>Image Caption or Title</figcaption>
  </figure>
</div>
```

---

## Organized Gallery with Multiple Sections

You can organize images into thematic sections:

### Landscapes

![Mountain Vista](../assets/images/landscape-1.jpg)
![Forest Path](../assets/images/landscape-2.jpg)
![Ocean Sunset](../assets/images/landscape-3.jpg)

### Portraits

![Portrait 1](../assets/images/portrait-1.jpg)
![Portrait 2](../assets/images/portrait-2.jpg)
![Portrait 3](../assets/images/portrait-3.jpg)

### Details & Close-ups

![Texture 1](../assets/images/detail-1.jpg)
![Texture 2](../assets/images/detail-2.jpg)
![Texture 3](../assets/images/detail-3.jpg)

---

## Tips for Best Results

### Image Organization
- Store images in a dedicated folder: `content/assets/images/`
- Use descriptive filenames: `landscape-mountain-1.jpg` instead of `img1.jpg`
- Keep image sizes consistent within a gallery section

### File Paths
- Use relative paths: `../assets/images/filename.jpg`
- If your gallery is deep in folders, adjust `../` accordingly
- Quartz will process and optimize images during build

### Alt Text
- Always include descriptive alt text for accessibility
- Example: `![Sunset over the Pacific Ocean](../assets/images/sunset.jpg)`

### Image Optimization
- For web, keep images under 2MB
- Recommended dimensions: 1200x800px to 1920x1280px
- Quartz will generate thumbnails automatically

---

## CSS Customization

If you need custom styling, add a style block to your note. Add this to your Quartz CSS files:

```css
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(var(--gallery-columns, 3), 1fr);
  gap: var(--gallery-spacing, 1.5rem);
  margin: 2rem 0;
}

.gallery-item {
  margin: 0;
  overflow: hidden;
  border-radius: 8px;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.02);
}

.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
}

.gallery-item figcaption {
  padding: 1rem;
  background: var(--light);
  font-size: 0.95rem;
  text-align: center;
}

/* Responsive design */
@media (max-width: 1024px) {
  .gallery-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .gallery-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
}
```

---

## Image Sources & Attribution

When using external images, remember to:
- Check license requirements (Creative Commons, paid, etc.)
- Include attribution if required
- Link to source images when appropriate
- Store originals in your vault if they're important

---

## Alternative: Using Links for External Images

If your images are hosted elsewhere (Imgur, Cloudinary, etc.):

```markdown
![Alt text](https://example.com/image.jpg)
```

However, **self-hosting images is recommended** for:
- Better site performance
- Offline compatibility
- Full control and privacy
- Avoiding broken images from external services

---

## Related Template Notes

Link to other galleries or templates you create:
- [[another-gallery]]
- [[image-processing-guide]]

---

## Metadata

- **Created**: [Today's Date]
- **Last Updated**: [Last Edit Date]
- **Status**: Template
- **Category**: Web Design

