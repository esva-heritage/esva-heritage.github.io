# Eastern Shore of Virginia National Heritage Area


**Website:** [https://esva-heritage.github.io/](https://esva-heritage.github.io/)  
**Repository:** [https://github.com/esva-heritage/esva-heritage.github.io](https://github.com/esva-heritage/esva-heritage.github.io)



## Table of Contents

1. [About the Project](#about-the-project)
2. [Website Sections](#website-sections)
3. [Built With](#built-with)
4. [Repository Structure](#repository-structure)
5. [Configuration](#configuration)
   1. [Sample Posts](#sample-posts)
   2. [Site Variables](#site-variables)
   3. [Posts](#posts)
   4. [Managing navigation and site settings](#Managing-navigation-and-site-settings)
   5. [Adding images and photo credits](#Adding-images-and-photo-credits)
   6. [Updating the interactive map and engagement form](Updating-the-interactive-map-and-engagement-form)
   7. [Publishing Changes](#Publishing-Changes)
6. [Features](#features)
   1. [Disqus](#disqus)
   2. [Google Analytics](#google-analytics)
   3. [RSS Feeds](#rss-feeds)
   4. [Social Media Icons](#social-media-icons)
   5. [MathJax](#mathjax)
   6. [Syntax Highlighting](#syntax-highlighting)
   7. [Markdown](#markdown)
7. [Credits and License](#creidts-and-license)



## About the Project

This repository contains the source code and content for the Eastern Shore of Virginia (ESVA) National Heritage Area feasibility-study project. The site documents and supports the community-driven feasibility study exploring whether the Eastern Shore of Virginia should become a **National Heritage Area (NHA)**.

The website is intended to help residents, organizations, visitors, and other stakeholders learn about the study, explore the region's historic and cultural resources, and contribute local knowledge. It highlights the relationship between heritage conservation, community identity, and locally informed economic development.

**Project status:** The website documents an ongoing feasibility study. It does not indicate that the Eastern Shore of Virginia has already been designated as a National Heritage Area. Designation requires additional steps beyond the feasibility study, including federal legislation.

## Website Sections

The public website is organized around three primary sections:

- **The Study** – Explains the National Heritage Area concept, why the Eastern Shore is considering designation, what a feasibility study involves, and answers frequently asked questions.
- **The Shore** – Introduces historic and cultural places across the region through an interactive map and curated resources.
- **Community Engagement** – Describes why public participation matters, poses questions to help identify important places and underrepresented stories, and provides a way for community members to contribute to the study.

The home page introduces the project and provides access to these sections. Site navigation and social media links are configured in `_data/settings.yml`.

## Built With

The website is built with:

- **[Jekyll](https://jekyllrb.com/)** – Static site generator that converts Markdown, HTML, layouts, and data into a website.
- **[GitHub Pages](https://pages.github.com/)** – Hosting and publishing platform.
- **Liquid, HTML, and Markdown** – Used for page templates and content.
- **Sass/SCSS and CSS** – Used to style the site.

The project is based on the **[Millennial Jekyll theme](https://github.com/LeNPaul/Millennial)**. The repository's Jekyll configuration includes the `jekyll-paginate`, `jekyll-sitemap`, `jekyll-feed`, and `jekyll-seo-tag` plugins.

## Repository Structure

```bash
Millennial/
├── _data                      # Data files
|  └── settings.yml            # Theme settings and custom text
├── _includes                  # Theme includes
├── _layouts                   # Theme layouts (see below for details)
├── _posts                     # Where all your posts will go
├── sass                       # Folder containing SCSS files
├── assets                     # Style sheets and images are found here
|  ├── css                     # Style sheets go here
|  |  └── main.scss            # Main SCSS file
|  |  └── syntax.css           # Style sheet for code syntax highlighting
|  └── img                     # Images go here
├── pages                      # Category pages
├── _config.yml                # Site build settings
├── Gemfile                    # Ruby Gemfile for managing Jekyll plugins
├── index.html                 # Home page
├── LICENSE.md                 # License for this theme
├── README.md                  # Includes all of the documentation for this theme
└── rss-feed.xml               # Generates RSS 2.0 file which Jekyll points to
```

## Configuration

### Sample Posts

Visit the [the demo site](https://lenpaul.github.io/Millennial/) to find sample posts that show what different types of text formatting look like. You can find these posts in the `_posts` folder, which show what the best practices for setting up your own site are.

### Site Variables

To change site build settings, edit the `_config.yml` file found in the root of your repository, which you can tweak however you like. More information on configuration settings and plugins can be found on [the Jekyll documentation site](https://jekyllrb.com/docs/configuration/). This is also where you will be able to customize the title, description, and the author/owner of your site.

In the `settings.yml` file found in the `_data` folder, you will be able to customize your site settings, such as setting Disqus comments, Google Analytics, what shows up in your menu, and social media information.

### Posts

The primary sections are posts in _posts/, rather than files in a menu/ directory. The current examples are:
- _posts/2026-10-29-the-study.md
- _posts/2026-10-29-the-shore.md
- _posts/2026-10-29-engagement.md

Jekyll post filenames begin with a date in YYYY-MM-DD format. The remaining filename supplies the post slug used by the site's /:title permalink setting. When creating or renaming a post that appears in the main menu, make sure its resulting URL matches the corresponding url in _data/settings.yml.

A typical post front matter block in this repository looks like:

```
---
layout:
title:
author:
categories:
tags: []
image:
---
```

`layout` specifies which layout to use, `title` is the page or post title, `categories` can be used to better organize your posts, `tags` are used when generating related posts based on the topic of the post, and `image` specifies which images to use. Have a look at some posts in the `_posts` directory to see how these variables are set.


### Managing navigation and site settings

- Edit `_data/settings.yml` to change the navigation menu, social media links, contact link, and other theme settings.
- Edit `_config.yml` to change site-wide Jekyll settings, the site title and description, permalink behavior, or the configured plugins.
- When adding a new page that should appear in the main menu, add its name and URL to the `menu` list in `_data/settings.yml`.

### Adding images and photo credits

1. Add the image file to `assets/img/` (or the relevant existing asset folder).
2. Reference it from a page or post using the correct path. For example:

   ```markdown
   ![A description of what is visible in the photograph](/assets/img/example-image.jpg)
   ```

3. Write useful alternative text that conveys the image's relevant content. Avoid using a filename or generic wording as the description.
4. Add a visible photo credit near the image when a credit is required. Include the photographer, organization, archive, or other source as appropriate, and make sure the credit is accurate.
5. Check that the image loads on the published website and that it displays properly on mobile and desktop screens.

Do not assume that an image is free to reuse simply because it is available online. Confirm usage rights and retain any required attribution.

### Updating the interactive map and engagement form

The **Shore** section includes an interactive map, and the **Community Engagement** section includes an embedded contribution form. When updating either feature, preserve the provider's current embed code and confirm that the embedded content works on the live site. Test the page at desktop and mobile widths, and provide a meaningful heading or explanation so visitors understand what the embedded feature is for.

### Publishing Changes

The public website is hosted through GitHub Pages at [https://esva-heritage.github.io/](https://esva-heritage.github.io/).

A typical update workflow is:

1. Create a branch for the change.
2. Edit the relevant page, post, image, stylesheet, or configuration file.
3. Preview the site locally with `bundle exec jekyll serve`.
4. Check links, images, alternative text, photo credits, navigation, and embedded content.
5. Commit and push the changes, then open a pull request for review when appropriate.
6. Merge the approved changes into the branch configured for GitHub Pages publishing.
7. Check the repository's **Actions** tab and **Settings → Pages** if the published site does not update or a build fails.

Allow the GitHub Pages build to complete, then review the live website to confirm that the changes appear as expected.


## Features

### Disqus

Millennial supports comments at the end of posts through [Disqus](https://disqus.com/). In order to activate Disqus commenting, set `disqus.comments` to true in the `_data/settings.yml` file. If you do not have a Disqus account already, you will have to set one up, and create a profile for your website. You will be given a `disqus_shortname` that will be used to generate the appropriate comments sections for your site. More information on [how to set up Disqus](http://www.perfectlyrandom.org/2014/06/29/adding-disqus-to-your-jekyll-powered-github-pages/).

### Google Analytics

It is possible to track your site statistics through [Google Analytics](https://www.google.com/analytics/). Similar to Disqus, you will have to create an account for Google Analytics, and enter the correct Google ID for your site under `google-ID` in the `settings.yml` file. More information on [how to set up Google Analytics](https://michaelsoolee.com/google-analytics-jekyll/). Note: If you are not using Google Analytics, please change `google-ID` to an empty string.

### RSS Feeds

Atom is supported by default through [jekyll-feed](https://github.com/jekyll/jekyll-feed). With jekyll-feed, you can set configuration variables such as 'title', 'description', and 'author', in the `_config.yml` file.

RSS 2.0 is also supported through [RSS auto-discovery](http://www.rssboard.org/rss-autodiscovery). The `rss-feed.xml` file (based on the template found at [jekyll-rss-feeds](https://github.com/snaptortoise/jekyll-rss-feeds)) that the feed path points to when using RSS 2.0 is automatically generated based on the appropriate configuration variables found in `_data/settings.yml`.

To use RSS 2.0, ensure the following is done:

* Uncomment the last two lines in the `_config.yml` file.

* In `_data/settings.yml`, under 'social', comment out the rss-square that points to `feed.xml`, and uncomment the rss-square that points to `rss-feed.xml`.

* In `_includes/head.html`, comment out `{% feed_meta %}` and uncomment the line under the RSS 2.0 comment.

### Social Media Icons

All social media icons are courtesy of [Font Awesome](http://fontawesome.io/). You can change which icons appear, as well as the account that they link to, in the `settings.yml` file in the `_data` folder.

### MathJax

Millennial comes out of the box with [MathJax](https://www.mathjax.org/), which allows you to display mathematical equations in your posts through the use of [LaTeX](http://www.andy-roberts.net/writing/latex/mathematics_1).

### Syntax Highlighting

Millennial provides syntax highlighting through [fenced code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/). Syntax highlighting allows you to display source code in different colors and fonts depending on what programming language is being displayed. You can find the full list of supported programming languages [here](https://github.com/jneen/rouge/wiki/List-of-supported-languages-and-lexers). Another option is to embed your code through [Gist](https://en.support.wordpress.com/gist/).

### Markdown

As always, Jekyll offers support for GitHub Flavored Markdown, which allows you to format your posts using the [Markdown syntax](https://guides.github.com/features/mastering-markdown/). Examples of these text formatting features can be seen below. You can find this post in the `_posts` directory as well as the `README.md` file.


## Credits and License

This site is based on the Millennial Jekyll theme by Paul Le. The repository includes the theme's MIT license in LICENSE.md; retain the required copyright and license notice when redistributing the covered theme code.

The theme's MIT license should not be assumed to cover every photograph, map, document, or item of project content in the repository. Check each asset's own permissions and attribution requirements.
