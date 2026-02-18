This is the repo for the Swinux website. It's using Hugo and we use the Re-Terminal theme with modifications. 

<h1>Running the Website</h1>

This repo uses the Re-Terminal theme. After cloning this repo locally, add the Re-Terminal theme to your ./themes/ directory to successfully build and run the site. You can get the theme here:

https://github.com/mirus-ua/hugo-theme-re-terminal

Clone this repo:

`git clone https://github.com/swinuxclub/swinux.org`

Enter themes directory:

`cd themes`

Download Re-Terminal theme:

`git clone https://github.com/mirus-ua/hugo-theme-re-terminal`

Rename the file:

`mv hugo-theme-re-terminal re-terminal`

Once this is completed, you can run the site using:

`hugo server`

Afterwards, to build the static files, run the following:

`hugo build`

<h2>Post Structure</h2>

Posts are saved to the content directory. The about and content pages are self-contained. Any post to the site should be placed in the posts folder.

A post should be self-contained in it's own folder, with any images being placed in an /images subfolder. A post should have the following structure and be placed in the /posts directory:

Page:
- `my-first-post/my-first-post.md`
- `my-first-post/images/my-first-post-image1.png`
- `my-first-post/images/my-first-post-cutekittens.png`

<h2>Markdown Post Structure</h2>

All posts should have the following in the top of the Markdown file to allow Hugo to publish the site:

+++<br>
title = "My First Post"<br>
date = "2025-07-28T14:19:18+10:00"<br>
author = "The Author"<br>
description = "This is the description of my first post!"<br>
readingTime = true<br>
draft = true<br>
tags = ["tag1","tag2", "hi"]<br>
+++<br>

**description = "string"**<br>
Setting description sets the bottom text for posts on the main page. You can set an image as a description to be shown instead of text.

**readingTime = true|false**<br>
readingTime enables reading estimation to give our readers an estimate at how long the article is.

**draft = true|false**<br>
Setting draft to true disables the article from being published to the site. This is useful when articles are in progress.


To maintain site consistency, please only use the following tags:
- event
- article
- guide
- linux
- hardware
- code

Images can be referenced in the post (markdown file) with the following directory structure:
- `/posts/my-first-post/images/my-first-post-image1.png`
- `/posts/my-first-post/images/my-first-post-cutekittens.png`

So that an image can be inserted with:

`[Alt Text For Image](/posts/my-first-post/images/my-first-post-cutekittens.png)`

<h2>Theme Modifications</h2>

Modifications to the existing theme can be put in the root hugo directory matching the structure provided by the Re-Terminal themes. This will overwrite css and html changes without needing to modify the theme directly. See below for changes made:

`assests/css/main.scss`<br>
This recolours the background & increases the article width to increase page density.

`assests/css/button.scss`<br>
This slightly increases the size of the read more button.

`assests/css/color/color.scss`<br>
This changes the red theme to match the shade of the Swinux club colour.

`layouts/partials/footer.html`<br>
This changes the footer to link to Re-Terminal & Hugo, and our contact and about pages.

`layouts/partials/logo.html`<br>
This changes the logo text (top of page) to the Swinux club + record.

`layouts/partials/header.html`<br>
This changes the header to integrate menus for events, articles about etc. at the top of the page.

`layouts/partials/_default/index.html`<br>
This changes the home page to add text below the header, providing a brief description about the webpage.

`/static/img/theme-colors/red.png`<br>
This replaces the default icon with the Swinux logo.

<h2>Deploying the Site to a VPS</h2>

Running a Linux system, install docker compose. On Ubuntu, you may use:

`sudo apt install docker-compose`

Next, create a data folder & caddy folder in your home directory.

`mkdir data`

`mkdir data/caddy`

Create a caddyfile in the data/caddy/ directory with the Caddyfile found in this repo.

Next, copy the compose.yaml file to the home directory (~/).

Lastly, you can copy the files built by `hugo build` in the public directory to the VPS' ~/data/site directory.

Once this is completed, you can run the site using `docker-compose up -d`.

The site should be publicly available to view using HTTPS.

A reminder that a domain must be configured and a DNS record must point swinux.org to the VPS IP you have.
