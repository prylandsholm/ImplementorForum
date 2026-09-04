# Semantic4iop.org – Implementor Forum

A content management system for the Implementor Forum for Industrial Semantic Interoperability, built with Jekyll and GitHub Pages.

## 📋 Quick Start

This site is powered by **Jekyll**, a static site generator that separates content from design. This means:
- ✅ Non-technical members can add and update content
- ✅ No HTML editing required
- ✅ Simple file formats (Markdown and YAML)
- ✅ Free hosting via GitHub Pages

## 🎯 How to Add Content

### Option 1: Edit Files Directly on GitHub (Easiest)

You don't need to install anything! Just use GitHub's web editor:

1. Go to the repository on GitHub
2. Click on the file you want to edit
3. Click the ✏️ **Edit** button
4. Make your changes
5. Click **Commit changes** at the bottom

The site will automatically rebuild within 2 minutes.

### Option 2: Edit Locally (Advanced)

If you prefer to work on your computer:

```bash
# Clone the repository
git clone https://github.com/prylandsholm/ImplementorForum.git
cd ImplementorForum

# Install dependencies
bundle install

# Start local server (view at http://localhost:4000)
bundle exec jekyll serve

# Make your edits, then commit and push
git add .
git commit -m "Update content"
git push
```

---

## 📚 Adding Different Types of Content

### 1️⃣ Add Summit Recordings

**File to edit:** `_data/recordings.yml`

```yaml
- title: "Your Presentation Title"
  speaker: "Speaker Name"
  date: 2026-06-15
  brightcove_id: "your-video-id-here"
  description: "Brief description of the presentation"
  tags: [keynote, topic1, topic2]
```

**What each field means:**
- `title`: The presentation name
- `speaker`: Who gave the talk
- `date`: When it happened (format: YYYY-MM-DD)
- `brightcove_id`: Video ID from Brightcove player (ask if unsure)
- `description`: 1-2 sentence summary
- `tags`: Labels to organize content (optional)

These recordings appear on the homepage in a grid.

---

### 2️⃣ Add Industry Use Cases

**File to edit:** `_data/use_cases.yml`

```yaml
- title: "Smart Manufacturing with Semantic Standards"
  organization: "Example Corp"
  industry: "Manufacturing"
  description: "How Example Corp implemented semantic interoperability in their manufacturing pipeline."
  link: "https://example.com"
  tags: [manufacturing, iot, industry-4.0]
```

**What each field means:**
- `title`: Name of the use case
- `organization`: Company or institution name
- `industry`: What sector (Manufacturing, Supply Chain, etc.)
- `description`: 2-3 sentences about the implementation
- `link`: URL to learn more
- `tags`: Keywords for discovery

Visit `/use-cases/` page to see all use cases.

---

### 3️⃣ Add Working Groups / Focus Groups

**File to edit:** `_data/working_groups.yml`

```yaml
- name: "Manufacturing IoT Working Group"
  description: "Focused on semantic standards for industrial IoT environments."
  leader: "Jane Smith"
  status: "Active"
  members: 25
  contact: "group-email@example.com"
```

**What each field means:**
- `name`: Group name
- `description`: What the group does
- `leader`: Who leads the group
- `status`: Active / Forming / Paused
- `members`: How many people in the group
- `contact`: Email or contact method

Visit `/focus-groups/` page to see all working groups.

---

### 4️⃣ Add Events (Workshops, Conferences, Meetings)

**File to edit:** `_data/events.yml`

```yaml
- title: "Semantic Interoperability Workshop Q3 2026"
  date: 2026-09-15
  location: "Oslo, Norway"
  description: "Hands-on workshop on implementing semantic standards in your organization."
  registration_link: "https://forms.office.com/..."
  type: "workshop"
```

**What each field means:**
- `title`: Event name
- `date`: When (YYYY-MM-DD format)
- `location`: Where or "Online"
- `description`: What will be covered
- `registration_link`: URL to sign up
- `type`: workshop / conference / meeting

Visit `/events/` page to see all events.

---

### 5️⃣ Add Team Members

**File to edit:** `_data/team.yml`

```yaml
- name: "John Doe"
  title: "Forum Chair"
  organization: "Tech Company"
  bio: "Expert in semantic interoperability with 15 years of industry experience."
  photo: "/images/john-doe.jpg"
  social:
    linkedin: "https://linkedin.com/in/johndoe"
    website: "https://example.com"
```

---

### 6️⃣ Create New Pages (About, Resources, etc.)

**To create a new page:** Add a `.md` file to the `pages/` folder

**Template for new page** (`pages/your-page.md`):

```markdown
---
layout: default
title: Your Page Title
permalink: /your-page/
---

# Your Heading

This is your content. You can use **bold**, *italic*, and [links](https://example.com).

## Subheading

More content here.
```

**What each field means:**
- `layout`: Always use `default` for regular pages
- `title`: The page title (appears in browser tab and nav)
- `permalink`: The URL path (e.g., `/your-page/` becomes yoursite.com/your-page/)

After creating the file:
1. Add a link to it in `_includes/navigation.html` if you want it in the menu
2. Commit and push
3. The page appears on the site

---

## 🎨 Edit the Navigation Menu

**File to edit:** `_includes/navigation.html`

To add a new link to the top menu:

```html
<a href="{{ site.baseurl }}/your-page/" class="{% if page.url contains '/your-page' %}active{% endif %}">Your Page</a>
```

---

## 🎯 Edit Site-Wide Settings

**File to edit:** `_config.yml`

Common things to change:
```yaml
title: Semantic4iop.org – Implementor Forum
description: Community platform for Industrial Semantic Interoperability
url: "https://prylandsholm.github.io/ImplementorForum"
```

---

## 🎨 Edit the Styling / Colors

**File to edit:** `styles.css`

Example - change the green accent color:
```css
.topnav a.active {
  background-color: #04AA6D;  /* Change this hex color */
}
```

Common colors to customize:
- `#04AA6D` - Green accent color (links, buttons, active nav)
- `#333` - Dark gray (headings, nav background)
- `#f9f9f9` - Light gray background
- `#f5f5f5` - Medium gray backgrounds

---

## 📝 Content Format Tips

### Markdown Syntax

You can use markdown in page content for nice formatting:

```markdown
# Heading 1
## Heading 2
### Heading 3

**Bold text**
*Italic text*

- Bullet point
- Another point
  - Sub-point

1. Numbered item
2. Another item

[Link text](https://example.com)

![Image alt text](image.png)
```

### YAML Format (for data files)

- Use `- ` to start a new item
- Use `key: value` format
- Keep proper indentation (spaces, not tabs)
- Text with special characters should go in quotes: `"Text with: special chars"`
- Dates: `2026-09-15` (not in quotes)
- Numbers: `25` (not in quotes)

---

## 🔄 How GitHub Pages Publishing Works

1. You edit a file on GitHub
2. You click "Commit changes"
3. GitHub automatically runs Jekyll to build the site
4. The site updates within 2 minutes
5. No manual deployment needed!

To see build status/errors:
1. Go to your repository
2. Click **Settings** → **Pages** → **Build and deployment**
3. Look at recent deployments

---

## ❓ Troubleshooting

### Changes aren't showing up

- **Wait 2-3 minutes** – GitHub needs time to rebuild
- **Clear browser cache** – Press Ctrl+Shift+Delete (or Cmd+Shift+Delete on Mac)
- **Check build status** – Settings → Pages → see if build failed

### Error in YAML/Markdown

- Check indentation (4 spaces per level, no tabs)
- Check quotes around text with special characters
- Check date format (YYYY-MM-DD)

### Need help?

1. Check the examples in `_data/*.yml` files
2. Copy an existing entry and modify it
3. Look at `pages/*.md` for page examples

---

## 🚀 Next Steps

1. **Add your first recording** – Edit `_data/recordings.yml`
2. **Build your team page** – Edit `_data/team.yml`
3. **Create a resources page** – Pages already exist, just edit them
4. **Customize colors** – Edit `styles.css`
5. **(Optional) Add visual editor** – Request Decap CMS setup for non-technical users

---

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Help](https://docs.github.com/en/pages)
- [YAML Syntax](https://yaml.org/refcard.html)

---

## 📞 Support

For questions about content management or setup:
1. Check this README first
2. Look at existing examples in `_data/` files
3. Review file structure above
4. Visit the resources links above

---

## Purpose

- Share summit recordings
- Build the community
- Manage working groups, events, and use cases
- Provide a foundation for future platform expansion

---

*Last updated: 2026-09-04*
