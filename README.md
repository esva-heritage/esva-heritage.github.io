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
   3. [Adding Menu Pages](#adding-menu-pages)
   4. [Posts](#posts)
   5. [Layouts](#layouts)
   6. [YAML Front Block Matter](#yaml-front-block-matter)
6. [Features](#features)
   1. [Design Considerations](#design-considerations)
   2. [Disqus](#disqus)
   3. [Google Analytics](#google-analytics)
   4. [RSS Feeds](#rss-feeds)
   5. [Social Media Icons](#social-media-icons)
   6. [MathJax](#mathjax)
   7. [Syntax Highlighting](#syntax-highlighting)
   8. [Markdown](#markdown)
7. [Making a change to the Millennial Layout](#Making-a-change-to-the-Millennial-Layout)
8. [Questions?](#questions)
8. [Credits](#credits)
9. [License](#license)




1. [Introduction](#introduction)
   1. [What is Jekyll](#what-is-jekyll)
   2. [Never Used Jeykll Before?](#never-used-jekyll-before)
2. [Installation](#installation)
   1. [GitHub Pages Installation](#github-pages-installation)
   2. [Local Installation](#local-installation)
   3. [Directory Structure](#directory-structure)
   4. [Starting From Scratch](#starting-from-scratch)
3. [Configuration](#configuration)
   1. [Sample Posts](#sample-posts)
   2. [Site Variables](#site-variables)
   3. [Adding Menu Pages](#adding-menu-pages)
   4. [Posts](#posts)
   5. [Layouts](#layouts)
   6. [YAML Front Block Matter](#yaml-front-block-matter)
4. [Features](#features)
   1. [Design Considerations](#design-considerations)
   2. [Disqus](#disqus)
   3. [Google Analytics](#google-analytics)
   4. [RSS Feeds](#rss-feeds)
   5. [Social Media Icons](#social-media-icons)
   6. [MathJax](#mathjax)
   7. [Syntax Highlighting](#syntax-highlighting)
   8. [Markdown](#markdown)
5. [Everything Else](#everything-else)
6. [Contributing](#Contributing)
7. [Questions?](#questions)
8. [Credits](#credits)
9. [License](#license)


## About the Project

This repository contains the source code and content for the Eastern Shore of Virginia (ESVA) National Heritage Area website. The site documents and supports the community-driven feasibility study exploring whether the Eastern Shore of Virginia should become a **National Heritage Area (NHA)**.

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
├── assets                     # Style sheets and images are found here
|  ├── css                     # Style sheets go here
|  |  └── _sass                # Folder containing SCSS files
|  |  └── main.scss            # Main SCSS file
|  |  └── syntax.css           # Style sheet for code syntax highlighting
|  └── img                     # Images go here
├── pages                      # Category pages
├── _config.yml                # Site build settings
├── Gemfile                    # Ruby Gemfile for managing Jekyll plugins
├── index.md                   # Home page
├── LICENSE.md                 # License for this theme
├── README.md                  # Includes all of the documentation for this theme
└── rss-feed.xml               # Generates RSS 2.0 file which Jekyll points to
```

## Configuration

### Sample Posts

Visit the [the demo site](https://lenpaul.github.io/Millennial/) to find sample posts that show what different types of text formatting look like. You can find these posts in the `_posts` folder, which show what the best practices for setting up your own site are.

### Site Variables

To change site build settings, edit the `_config.yml` file found in the root of your repository, which you can tweak however you like. More information on configuration settings and plugins can be found on [the Jekyll documentation site](https://jekyllrb.com/docs/configuration/). This is also where you will be able to customize the title, description, and the author/owner of your site.

If you are hosting your site on GitHub Pages, then committing a change to the `_config.yml` file will force a rebuild of your site with Jekyll. Any changes made should be viewable soon after. If you are hosting your site locally, then you must run `jekyll serve` again for the changes to take place.

In the `settings.yml` file found in the `_data` folder, you will be able to customize your site settings, such as setting Disqus comments, Google Analytics, what shows up in your menu, and social media information.

### Adding Menu Pages

The menu pages are found in the `menu` folder in the root directory, and can be added to your menu in the `settings.yml` file.

### Posts

You will find example posts in your `_posts` directory. Go ahead and edit any post and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention of `YYYY-MM-DD-name-of-post.md` and includes the necessary front matter. Take a look at any sample post to get an idea about how it works. If you already have a website built with Jekyll, simply copy over your posts to migrate to Millennial.

### Layouts

There are two main layout options that are included with Millennial: post and page. Layouts are specified through the [YAML front block matter](https://jekyllrb.com/docs/frontmatter/). Any file that contains a YAML front block matter will be processed by Jekyll. For example:

```
---
layout: post
title: "Example Post"
---
```

Examples of what posts looks like can be found in the `_posts` directory, which includes this post you are reading right now. Posts are the basic blog post layout, which includes a header image, post content, author name, date published, social media sharing links, and related posts.

Pages are essentially the post layout without any of the extra features of the posts layout. An example of what pages look like can be found at the [documentation page](https://lenpaul.github.io/Millennial/pages/documentation.html).

In addition to the two main layout options above, there are also custom layouts that have been created for the [home page](https://lenpaul.github.io/Millennial/) and the [contacts page](https://lenpaul.github.io/Millennial/pages/contact.html). These are simply just page layouts with some [Liquid template code](https://shopify.github.io/liquid/). Check out the `index.html` file in the root directory for what the code looks like.

### YAML Front Block Matter

The recommended YAML front block is:

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

## Features

### Design Considerations

Millennial was designed to be a minimalist theme in order for the focus to remain on your content. For example, links are signified mainly through an underline text-decoration, in order to maximize the perceived affordance of clickability (I originally just wanted to make the links a darker shade of grey).

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

## Everything Else

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

## Making a change to the Millennial Layout

If you would like to make a feature request, or report a bug or typo in the documentation, then please [submit a GitHub issue](https://github.com/LeNPaul/Millennial/issues/new) with the creator of the theme. If you would like to make a contribution, then feel free to [submit a pull request](https://help.github.com/articles/about-pull-requests/). If this is your first pull request, it may be helpful to read up on the [GitHub Flow](https://guides.github.com/introduction/flow/) first.

Millennial has been designed as a base for users to customize and fit to their own unique needs. Please keep this in mind when requesting features and/or submitting pull requests. Some examples of changes that I would love to see are things that would make the site easier to use, or better ways of doing things. Please avoid changes that do not benefit the majority of users.

## Questions?

This theme is completely free and open source software. You may use it however you want, as it is distributed under the [MIT License](http://choosealicense.com/licenses/mit/). If you are having any problems, any questions or suggestions, feel free to [tweet at the creator](https://twitter.com/intent/tweet?text=My%question%about%Millennial%is:%&amp;via=paululele), or [file a GitHub issue](https://github.com/lenpaul/Millennial/issues/new).

## Credits

### Creator

#### Paul Le

* [www.lenpaul.com](http://lenpaul.com)

* [Twitter](https://twitter.com/paululele)

* [GitHub](https://github.com/LeNPaul)

### Contributors

* [b-morawiec](https://github.com/b-morawiec)

* [JainVikas](https://github.com/JainVikas)

* [mschaeffner](https://github.com/mschaeffner)

* [cfe316](https://github.com/cfe316)

* [JeremyGonzales](https://github.com/JeremyGonzales)

### Icons + Demo Images

* [Death to Stock](https://deathtothestockphoto.com/)

* [Font Awesome](http://fontawesome.io/)

### Other

* [Jekyll](https://jekyllrb.com/)

* [Free Code Camp](https://www.freecodecamp.org)

* [Khan Academy](https://www.khanacademy.org/)

## License

Open sourced under the [MIT license](https://github.com/LeNPaul/Millennial/blob/gh-pages/LICENSE.md).
