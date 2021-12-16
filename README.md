# SETUP
### Running the site locally
I recommend beginning by forking my repository (https://github.com/csdevrie/aiv) and then cloning the repository to begin setup locally.  The site should be hosted in the gh-pages branch of the repository to be hosted on GitHub pages.

Once the site is cloned locally, cd into the directory of the site and run ```docker compose up``` and the site should be running locally at localhost:4000/aiv/.

### Running the site on GitHub Pages
To run on GitHub Pages, a few settings need to be changed in _config.yml.
In Site Settings, change `url: "https://csdevrie.github.io"` to your GitHub account in the form of `url: "https://yourusername.github.io"`.

Directly below that line, change `baseurl: "/aiv"` to the name of the repository so it is in the form `baseurl: "/yourrepo".` If you forked my repository, you likely won't need to change this because it will keep the same name.

Lastly, in the footer section, change the url for Discord.  Where it currently says `url: "http://localhost:4000/aiv/discord/"`, this should be changed to the url of the site, which would be in the form url: "https://yourusername.github.io/yourrepo/discord/".  The reasoning for this is that you cannot use variables in the config file, but you can use them everywhere else in the site.  Elsewhere in the site you can dynamically set the file path with the exception of the config file where you set the footer links.

With those changes made, push the changes to the gh-pages branch.  Now navigate to Settings->Pages on in the repo on github.com. Set the source to "gh-pages" branch and the folder to "/ (root)".  The site should now be running on GitHub Pages.

# MAINTENANCE 
### Main Pages and Navigation
The main pages of the site can be found in the _"_pages"_ folder as markdown files.  In the YAML front matter of each markdown file I have set a permalink for each page.  These links are then used in the site navigation.  To alter the navigation of the site, change the key/value pairs in "_data/navigation.yml"

### Images and Variables
When linking to images or other files, I recommend using site variables to keep the links changing dynamically between local development and the public site.  For example, {{ site.url }}{{ site.baseurl }}/assets/images/default.jpeg will link to https://yourusername.github.io/yourrepo/ assets/images/default.jpeg  when running on GitHub Pages and https://localhost:4000/yourrepo/ assets/images/default.jpeg  when running locally.

### Posts and Authors
To add new articles to the website, drop the markdown file in the "_posts" folder named in the format "YYYY-MM-DD-title-content.md" so Jekyll can sort the posts by recency.  This will update the posts on the Press page.

Each post has an author tab displayed on the left by default, this can be disabled in the YAML front matter by adding author_profile: false. To assign an author to the article, set author: Author Name in the front matter of the post. Add and edit author information in "_data/authors.yml".  I added some default incomplete author information in that file already, but it needs to be updated.

### Events
To add events, manually paste in the new event schedule table to "events.markdown".  Adding a \<h2> header above the table will automatically create an anchor for the navigation on the right for ease of navigation.  Older events that did not follow the table format also have a \<h2> header followed by a link to the markdown file describing the event.  These older schedules can be found in the "schedules" folder.

### Leadership Team
The leadership team page is currently full of default entries.  This page is simply laid out with two two-column tables.  In the first column, link to the portrait image that will be held in "/assets/images" and use site variables to keep the linking dynamic.  Change the name of the member in the same column of the table directly below the image.  In the second column, add information about each member.
