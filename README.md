This is the repo for the Swinux website. It's using Hugo and we use the Re-Terminal theme with modifications. 

**Before contributing, please read this documentation and look at existing examples, or contact the relevant committee member for guidance.**

<h1>Running the Website</h1>

This repo uses the Re-Terminal theme. After cloning this repo locally, if the Re-Terminal theme is not added, it will be on build. You can get the theme here:

https://github.com/mirus-ua/hugo-theme-re-terminal

Clone this repo:

`git clone https://github.com/SwinuxOrg/swinux.org`

Enter the directory:

`cd swinux.org`

You can run the site using:

`hugo server -D --disableFastRender`

The above enables all posts marked as draft, and fully recreates the site on changes to ensure accuracy.

If you're using Cloudflare to deploy the site, you will not need to build the files. Instead you may push the changes to GitHub to be made live for the public. If you aren't using Cloudflare, to build the static files for deployment, run the following:

`hugo build`

This will provide you with the generated files to be served via a webserver, such as Caddy.

If you've deleted the theme, you can remove the `go.sum` and `go.mod` files. Then, run the following commands to re-add the theme.

`hugo mod init swinux.org`

`hugo mod tidy`

`hugo mod get github.com/mirus-ua/hugo-theme-re-terminal/v2`

<h2>Post Structure</h2>

Posts are saved to the content directory. The about and content pages are self-contained. Any post to the site should be placed in the posts folder.

A post should be self-contained in it's own folder, with any images being placed in an /images subfolder. A post should have the following structure and be placed in the /posts directory:

Page:
- `oct-01-my-first-post/index.md`
- `oct-01-my-first-post/images/my-first-post-image1.png`
- `oct-01-my-first-post/images/my-first-post-cutekittens.png`

**Note that the markdown file must be named index.md. In addition, our naming convention requires that the date is in the format year-month-day-title such as jul-13-first-blog-post. Please keep as close to this as possible.**

<h2>Markdown Post Structure</h2>

All posts should have the following in the top of the index.md Markdown file to allow Hugo to publish the site:

+++<br>
title = "My First Post"<br>
date = "2025-07-28T14:19:18+10:00"<br>
author = "The Author"<br>
description = "This is the description of my first post!"<br>
readingTime = true<br>
draft = true<br>
tags = ["tag1","tag2", "linux"]<br>
+++<br>

**description = "string"**<br>
Setting the description sets the bottom text for posts on the main page. We reccomend leaving it blank and it will autofill.

**readingTime = true|false**<br>
readingTime enables reading estimation to give our readers an estimate at how long the article is.

**draft = true|false**<br>
Setting draft to true disables the article from being published to the site. This is useful when articles are a work in progress.

To maintain site consistency, please only use the following tags:
- event
- article
- guide
- linux
- hardware
- code
- student-submission > For student contributed submissions
- stem-social > For STEM Social events, organised by the SESS

Images can be referenced in the post (markdown file) with the following directory structure:
- `images/my-first-post-image1.png`
- `images/my-first-post-cutekittens.png`

So that an image can be inserted with:

Square:
`{{< inset-img src="images/my-first-post-image1.png" alt="Your alt text.">}}`
Rectangular:
`{{< inset-img-rect src="images/my-first-post-image-rectangle1.png" alt="Your alt text.">}}`


The above is the preferred method for attaching images, as they are automatically compressed on site build and results in faster loading of the webpage. The image will be automatically cropped to either a square or rectangle aspect ratio.

However, you can also use the below method for non-standard images. We discourage this as we preference site load times.

`[Alt Text For Image](/posts/my-first-post/images/my-first-post-cutekittens.png)`

You can use markdown formatting to edit the style and general format of the post. You can view a guide here:

https://www.craftmarkdown.com/markdown-cheat-sheet

<h2>Theme Modifications</h2>

Modifications to the existing theme can be put in the root hugo directory matching the structure provided by the Re-Terminal themes. This will overwrite css and html changes without needing to modify the theme directly. See below for changes made:

`assets/css/variables.scss`<br>
This recolours the background to a darker black to increase contrast for easier reading.

`assets/css/color/red.scss`<br>
This recolours the red accent to match the Swinburne colour scheme.

`assets/css/logo.scss`<br>
This is modified to remove the coloured background in the default theme.

`shortcodes/inset-img.html`<br>
This is the code used to crop and compress images which enables fast page loading.

`partials/logo.html`<br>
This is modified to implement a clickable club logo and title in html.


<h2>Deploying the Site to Cloudflare Pages</h2>

**This is the preferred (and current) method to deploy the website.**

Cloudflare pages is an excellent tool to host the swinux.org site, as it is free under 100,000 requests/month.

View the documentation here:

https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/

You attach the Github repository to Cloudflare which builds and deploys the site on changes to the repository automatically. Failed builds are not deployed, but mistakes can be pushed live.

If you are inheriting this repository, chances are you will not need to configure Cloudflare, as this is already done for you. Just pushing changes to the GitHub will allow you to publish articles and make site changes live for everyone.

**Please double check the accuracy and quality of your posts by using the debug server.**

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

A reminder that a domain must be configured (if not swinux.org) and a DNS record must point swinux.org to the public VPS IP you are allocated.
