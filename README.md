# SETUP
### Running the site locally
I recommend beginning by forking my repository (https://github.com/aivillage/aiv) and then cloning the repository to begin setup locally.  The site should be hosted in the gh-pages branch of the repository to be hosted on GitHub pages.

Once the site is cloned locally, cd into the directory of the site and run ```docker run -p 4000:4000 -v $(pwd):/site bretfisher/jekyll-serve``` and the site should be running locally at localhost:4000/.

# MAINTENANCE 
### Main Pages and Navigation
The main pages of the site can be found in the _"_pages"_ folder as markdown files.  In the YAML front matter of each markdown file I have set a permalink for each page.  These links are then used in the site navigation.  To alter the navigation of the site, change the key/value pairs in "_data/navigation.yml"

### Images and Variables
When linking to images or other files, I recommend using site variables to keep the links changing dynamically between local development and the public site.  For example, {{ site.url }}{{ site.baseurl }}/assets/images/default.jpeg will link to https://yourusername.github.io/yourrepo/ assets/images/default.jpeg  when running on GitHub Pages and https://localhost:4000/yourrepo/ assets/images/default.jpeg  when running locally.

### Posts and Authors
To add new articles to the website, drop the markdown file in the "_posts" folder named in the format "YYYY-MM-DD-title-content.md" so Jekyll can sort the posts by recency.  This will update the posts on the Press page.

Each post has an author tab displayed on the left by default, this can be disabled in the YAML front matter by adding author_profile: false. To assign an author to the article, set author: Author Name in the front matter of the post. Add and edit author information in "_data/authors.yml".  I added some default incomplete author information in that file already, but it needs to be updated.

### Events
To add events, include the event as a markdown file in the "/_events" folder. 
Make sure to include the following in the front-matter of the markdown file:
- the date in the format "YYYY-MM-DD" under "date" 
- short description of the event under "description"
- location in the format "City, State/Country" 

### Leadership Team
To add to the leadership team page, include a markdown file under "_volunteers" in the format "firstname_lastname.md" and a profile picture under "_volunteers/profiles".
Make sure to include the following in the front-matter of the markdown file:
- first name
- last name
- position
- expertise
- affiliation
- profile: filename of the profile picture 
- bio: "true/false"
Add a bio in the body of the markdown file if bio: true.

## 📁 Site Structure

```
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page templates
│   ├── default.html     # Base layout
│   ├── post.html        # Blog post layout  
│   └── event.html       # Event page layout
├── _posts/              # Blog posts
├── _events/             # Event pages
├── _volunteers/         # Team member profiles
├── assets/
│   └── css/
│       └── main.scss    # Main stylesheet
├── index.markdown       # Homepage
├── events.markdown      # Events listing
├── blog.markdown        # Blog listing
├── leadership.markdown  # Team page
├── discord.markdown     # Discord community
└── conduct.markdown     # Code of conduct
```

## 🎨 Styling & Theme

The site uses a dark, terminal-inspired theme with:

- **Colors**: Green (#00ff00) primary, red (#ff0000) accents, yellow (#ffff00) highlights
- **Fonts**: JetBrains Mono for headers/code, Inter for body text
- **Aesthetic**: DEFCON/hacker conference vibes with terminal-style elements

### Key CSS Classes

- `.card` - Content cards with hover effects
- `.event-item` - Event listing components  
- `.text-mono` - Monospace font utility
- `.glitch` - Glitch text effect
- `.cursor` - Blinking cursor animation

## 📝 Content Management

### Adding Blog Posts

Create new files in `_posts/` following the naming convention:
```
YYYY-MM-DD-title.md
```

Example frontmatter:
```yaml
---
layout: post
title: "Your Post Title"
author: "Author Name"
date: 2024-01-15 09:00:00 +0900
category: "AI Security"
description: "Brief description of the post"
---
```

### Adding Events

Create new files in `_events/` with:

```yaml
---
title: "Event Name"
date: 2024-08-15
description: "Event description"
location: "City, State"
layout: event
---
```

### Adding Team Members

Create files in `_volunteers/` with:

```yaml
---
first_name: "First"
last_name: "Last"  
position: "Role Title"
expertise: "Area of expertise"
affiliation: "Company/Organization"
profile: "photo.jpg"  # Place in volunteers/profiles/
bio: true
---

Bio content goes here...
```

## 🛠️ Customization

### Colors

Edit the SCSS variables in `assets/css/main.scss`:

```scss
$bg-dark: #0a0a0a;
$text-primary: #00ff00;
$accent: #ff0000;
// etc.
```

### Navigation

Update the navigation menu in `_layouts/default.html`:

```html
<nav class="nav-menu">
  <a href="/">Home</a>
  <a href="/events/">Events</a>
  <!-- Add more links -->
</nav>
```

### Site Configuration

Modify `_config.yml` for:
- Site title and description
- Social media links  
- SEO settings
- Plugin configuration

## 🚀 Deployment

### GitHub Pages

1. Push to GitHub repository
2. Go to Settings → Pages
3. Select source branch (usually `main`)
4. Site will be available at `https://username.github.io/repository-name`

### Custom Domain

1. Add `CNAME` file with your domain
2. Configure DNS settings
3. Enable HTTPS in GitHub Pages settings

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally with `bundle exec jekyll serve`
5. Submit a pull request

### Content Guidelines

- Use the established dark theme colors
- Keep the hacker/security aesthetic
- Test on mobile devices
- Optimize images before adding
- Follow existing content structure

## 📄 License

[Add your license information here]

## 🆘 Support

- Join our [Discord](https://discord.com/invite/GX5fhfT)
- Create an issue for bugs or feature requests
- Check existing documentation and issues first

---

Built with ❤️ by the AI Village community for hackers, researchers, and AI security enthusiasts worldwide.