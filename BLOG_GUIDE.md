# Blog Management Guide

This guide will help you add new blog posts, edit existing content, and manage your blog effectively.

## 📝 Adding New Blog Posts

### Method 1: Using Hugo's Built-in Command (Recommended)
```bash
# Navigate to your website directory
cd /Users/mohtasimhafiz/my-website

# Create a new blog post
hugo new blog/your-blog-title.md
```

### Method 2: Manual Creation
1. Create a new file in the `content/blog/` directory
2. Name it with a descriptive filename (e.g., `my-awesome-post.md`)
3. Add the frontmatter (see template below)

## 📋 Blog Post Template

Copy this template for new blog posts:

```markdown
---
title: "Your Blog Post Title"
description: "A brief description of your post (appears in search results and social media)"
date: 2024-10-15
draft: false
tags: ["tag1", "tag2", "tag3"]
categories: ["Category Name"]
author: "Mohtasim Hafiz"
featured: true
---

# Your Blog Post Title

Your content goes here...

## Section Headers

Use markdown for formatting:

- **Bold text**
- *Italic text*
- [Links](https://example.com)
- `Code snippets`

## Images

To add images:
1. Place images in `static/images/` directory
2. Reference them in your post: `![Alt text](/images/your-image.jpg)`

## Code Blocks

```javascript
// Your code here
console.log("Hello, world!");
```

---

*Add your thoughts or call-to-action here*
```

## 🖼️ Adding Images

### Step 1: Add Images to Your Site
1. Create an `images` folder in the `static/` directory:
   ```bash
   mkdir -p static/images
   ```

2. Copy your images to this folder:
   ```bash
   cp /path/to/your/image.jpg static/images/
   ```

### Step 2: Use Images in Blog Posts
```markdown
![Image description](/images/your-image.jpg)
```

### Step 3: Featured Images
To add a featured image that appears in blog listings:
```markdown
---
title: "Your Post"
featured_image: "/images/featured-image.jpg"
---
```

## ✏️ Editing Existing Posts

1. **Find the post**: Navigate to `content/blog/`
2. **Open the file**: Use any text editor (VS Code, Sublime Text, etc.)
3. **Edit content**: Modify the markdown content
4. **Save changes**: Hugo will automatically rebuild the site

## 🏷️ Managing Tags and Categories

### Tags
- Add relevant tags to help readers find related content
- Use lowercase, hyphenated format: `web-development`, `personal-growth`
- Keep tags consistent across similar posts

### Categories
- Use broader categories to organize content
- Examples: `Technology`, `Personal`, `Reflections`, `Tutorials`

## 📅 Publishing Workflow

### Draft Posts
- Set `draft: true` to keep posts private
- Set `draft: false` to publish

### Publishing Steps
1. Write your post
2. Set `draft: false`
3. Save the file
4. Hugo automatically rebuilds the site
5. Your post appears on the blog page

## 🎨 Customizing Blog Appearance

### Blog Page Settings
Edit `content/blog/_index.md` to customize:
- Page title and description
- Introduction text
- Any special formatting

### Theme Customization
The Blowfish theme handles most styling automatically, but you can:
- Modify `config/_default/params.toml` for theme settings
- Add custom CSS in `assets/css/` if needed

## 📊 Blog Statistics

Hugo automatically generates:
- **Blog listing page**: Shows all posts with summaries
- **Tag pages**: Group posts by tags
- **Category pages**: Group posts by categories
- **RSS feed**: For subscribers

## 🔧 Troubleshooting

### Common Issues

1. **Post not appearing**: Check if `draft: false`
2. **Images not loading**: Verify path starts with `/images/`
3. **Formatting issues**: Check markdown syntax
4. **Date problems**: Use format `YYYY-MM-DD`

### Getting Help
- Check Hugo documentation: https://gohugo.io/
- Blowfish theme docs: https://blowfish.page/
- Validate markdown: https://dillinger.io/

## 📁 File Structure

```
content/
├── blog/
│   ├── _index.md          # Blog page content
│   ├── post-1.md          # Individual blog posts
│   ├── post-2.md
│   └── ...
├── _index.md              # Homepage
└── about.md               # About page

static/
└── images/                # Your images go here
    ├── featured-1.jpg
    ├── post-image.png
    └── ...
```

## 🚀 Quick Start Checklist

- [ ] Create new post: `hugo new blog/my-post.md`
- [ ] Edit frontmatter (title, description, date, tags)
- [ ] Write your content in markdown
- [ ] Add images to `static/images/`
- [ ] Set `draft: false` to publish
- [ ] Save and view at `http://localhost:1313/blog/`

Happy blogging! 🎉
