Welcome to Canvas, a minimalist yet feature-packed starter theme for GravCMS.

## Why Canvas

Though I long wanted to make use of Grav as my CMS of choice, I often found my options lacking or confusing. Skeletons are too different. Themes can break your site. And the features I missed in WordPress had to be plugged in and be actually supported by the theme. As once an end-user of Grav, I found it irritating that I had to dig into theme files, documentation, and repositories just to get the site that I want working.

Going into theme development in the first time, I wanted to create a scaffolding theme that has all the features I wanted, that is loosely coupled (does not break down right away), and can be personalized with ease. I wanted it to be usable with a single installation. I wanted what Canvas has successfully accomplished.

## Inspirations

The core inspiration for Canvas was [hypertext](http://hypertext.artofthesmart.com/). I couldn't really put my finger on it, but I found hypertext to be way more comfortable to use than so many Grav themes out there. It does not rely on a skeleton. It feels complete. It feels easy to use. It does not force you to have a specific set of pages or configurations to get started right away. But I wanted more customizability and visual distinctiveness from it. In fact, the use of [simple.css](https://simplecss.org/) and the visual layout carries over from hypertext.

The accented border and wider left margin of Canvas were also taken from [Practical Typography](https://practicaltypography.com/).

<aside>
Here is the <code>aside</code> component that I also took from Practical Typography. To use it, just wrap your paragraph in an <code>aside</code> html tag. 
</aside>

I also included an `aside` component similar to Practical Typography. When viewing in desktop, it should occupy its own space in the left. Best to put the `aside` tag above the paragraph it refers to in the markdown file.

## Features

- Support for the following templates:
    + `default`
        * aliases: `page`
    + `error`
    + `blog` - creates a list of its child pages
        * aliases: `folder`, `archive`, `index`
    + `item` - intended as a child page of `blog` directories.
        * aliases: `post`, `article`
    + `form`
- Supports `category` and `tag` taxonomies for `item` templates.
- SEO-Friendly
    + natively supports and generates basic OpenGraph, Twitter Card, and Schema.org metadata for your content
    + allows you to customize your preview image for social sharing on a site and page level.
- Light and dark themes
- Color customization
- Favicon customization
- Switch navigation between the header and footer.

## Plugin Requirements

- Grav >= 1.7
- Sitemap
- Feed
- Form
- Admin
- Pagination
- Breadcrumbs

Note: Support for `feed` and `form` is still basic and will be improved in the future. `blog` templates must explicitly define `content.item` attributes in their frontmatter for the feed to show. See [feed plugin repo](https://github.com/getgrav/grav-plugin-feed) for more details.

## Installation

The recommended way to install Canvas is via cloning the [repository](https://github.com/acezalba/canvas.git) or downloading and extracting the latest [zip file](https://github.com/acezalba/canvas/archive/refs/heads/main.zip) to your `user/themes` directory. Canvas also has [releases](https://github.com/acezalba/canvas/releases) for future integration into Grav Package Manager.

Activate it by editing or adding the following line in your `user/config/system.yaml`.

```yaml
pages:
    theme: canvas
```

Clear your cache via the Admin panel or through `bin/grav cache` in your project terminal. Load your page to see your Canvas site come to life.

Copy the default `canvas.yaml` bundled with the theme to your `user/config/themes` to start customizing the colors of your site using hex codes.

However, editing the theme settings via the Grav Admin panel is recommended to use features not included in the default theme config file, such as favicon and preview image customization.