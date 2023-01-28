
A starter website for Tech Works For Us, built using

[Hylia](https://github.com/hankchizljaw/hylia) as a starter theme, with some tweaks

[Eleventy](https://11ty.io) static site generator

Git/Github for source control and repo hosting.

[Netlify CMS](https://www.netlifycms.org/) and Netlify to deploy


# Netlify CMS


Hylia has [Netlify CMS](https://www.netlifycms.org/) pre-configured as standard. You can customise the configuration by editing [`src/admin/config.yml`](https://github.com/hankchizljaw/hylia/blob/master/src/admin/config.yml).

To use the CMS on Live you need to have been set up with a 'Netlify Identity' through the Netlify site management console. This is seperate to your overall account signing for Netlify.

To access the CMS

- Go to `/admin/` on your site and login with your Netlify Identity details
- You’re in and ready to edit your content!

### Content that you can edit

The basic CMS setup allows you to edit the following:

- **Home page**: Edit the content on your homepage
- **Posts**: Create and edit blog posts
- **Generic pages**: Create generic pages that use a similar layout to posts
- **Global site data**: Various bits of global site data such as your url, title, posts per page and author details
- **Navigation**: Edit your primary navigation items
- **Theme**: Edit the design tokens that power the site’s theme

If you want to add a new field / data to pages or posts, you can add it to the frontmatter in the .md file, and then tell NetlifyCMS about it by adding the information to `src/admin/config.yml` 

[Netlify CMS Documentation](https://www.netlifycms.org/docs/intro/) is comprehensive, and includes information about [configuration options](https://www.netlifycms.org/docs/configuration-options/)


# How it is set up

It's using [Eleventy](https://11ty.io) , (11ty), a static site generator based on Node.js. Good [tips and help with 11ty](https://11ty.rocks)
Eleventy allows you to use many different template languages, and to use multiple languages in the same project.

Content is stored in Markdown Files.

The theme is [Hylia](https://github.com/hankchizljaw/hylia), with a few alterations (changed contact form, amended the homepage 'banner' to just show a title and strapline, added an SVG background). Look at `readme-hylia.md` for more about all the clever stuff it does.

Hylia is written in [Nunjucks templating language](https://mozilla.github.io/nunjucks/).

The page layout structure is pulled in from templates and 'partials' inside blocks, so you can specify which layout a page uses, and then configure and reuse code fragments. It's quite sweet.

There is a Styleguide page at `(website)/sytleguide/` which can be useful.




# Images

The leaf pattern is an SVG repeat that's encoded in the CSS. It is taken from here.
https://heropatterns.com under CC-By 4.0 - it is credited to HeroPatterns/Steve Schoger on the About page

I worked with 800x600 images, but you might want to look at going a little bigger, or a 16:9 aspect ratio.
Aim to keep them as small in filesize as possible. 

Dithering saves some file size for images (gif, png) whilst maintaing detail. It was used by LowTech as an aesthetic statement as much as an efficiency one. 
See writeups from:
[homebrewserver.club](https://homebrewserver.club/low-tech-website-howto.html#image-compression) 
[solar.lowtechmagazine.com](https://solar.lowtechmagazine.com/2018/09/how-to-build-a-lowtech-website.html)

There's a [lot of discussion](https://news.ycombinator.com/item?id=28696014) about how well it works as a compression tactic. I quite like it as an aesthetic signal that youre thinking about the file size.

We may want to use WebP images - they are much much more efficient but taking a while to catch on. 

[Image Compressor-Reduce PNG, JPEG, WEBP](https://redketchup.io/image-compressor) allows you to compress images and export in different formats.

### Dithering Images

You can do Photoshop Dithering in Save for Web Dialog for gifs.

https://ditherit.com offers different dithering options and algorithms. See also https://doodad.dev/dither-me-this/

**Halftone Pro** [https://halftonepro.com/app](https://halftonepro.com/app "title of this link") Does some fancy stuff with dither-like halftoning. However the images it has spit out are really big: you could use it to create the image then run them through a compressor?

The settings I liked for Halftone Pro:
Choose the Popart preset, changing colours to:
#404040
#F2CAA5

# Running Locally

To make a local version

1. Install [Github for Windows](https://desktop.github.com)
2. Download [Node.jd installer](https://nodejs.org/en/download/)
3. Install Node [instructions for Windows](https://treehouse.github.io/installation-guides/windows/node-windows.html)


Clone the repo in Git to a local folder

1. Add existing repository to GitHub Desktop `https://github.com/mildlydiverting/techworksforus`
2. In terminal `cd` into the project directory and run `npm install`
3. Once all the dependencies are installed run `npm start`
4. Open your browser at `http://localhost:8080` and away you go!

## Terminal commands

### Serve the site locally

```bash
npm start
```

### Build a production version of the site

```bash
npm run production
```

### Compile Sass

```bash
npm run sass:process
```

### Re-generate design tokens for Sass

```bash
npm run sass:tokens
```


# Design, Tokens and Styleguide

Colours currently:

    "primary": "#F27400",
    "primary-shade": "#8A4300",
    "primary-glare": "#FFB24D",
    "highlight": "#F0E0D1",
    "light": "#FFFFFF",
    "mid": "#cccccc",
    "dark": "#333333",
    "slate": "#404040"



### Design Tokens

You can configure the core design tokens that control the colours, size ratio and fonts.

To change the design tokens in the CMS, find the “Globals” in the sidebar then in the presented options, select “Theme Settings”.

To change the design tokens directly, edit [`_src/data/tokens.json`](https://github.com/hankchizljaw/hylia/blob/master/src/_data/tokens.json).

The tokens are converted into maps that the Sass uses to compile the front-end CSS, so make sure that you maintain the correct structure of `tokens.json`.

### Styleguide

A styleguide is available at '/styleguide/'





