Check out all the features of canvas` here.

===

## Page Templates

`canvas` has support for `default`, `blog`, `item`, `error`, `form` and `modular`. It can also handle without breaking most, if not all, templated content that you used with previous themes thanks to a coded fallback support for page collections in the `default` template. 

`Modular` templates only have fallback support in `canvas`. Meaning it can show your `modular` content with markdown, but it will not carry over the styles and looks that relied on your old theme.

`Form` template support is only minimal and only covers what is documented in the `form` plugin repository. General `forms` should work, but highly specialized ones as well as `modular` forms may break.

If you are a first time user, `default`, `blog`, and `item` are your friends. `default` is equivalent to a Wordpress page. `blog` is equivalent to a Wordpress loop or list of pages. 

`item` is equivalent to a Wordpress blog post. It is `item` that supports the `category` and `tag` taxonomies. It also shows `page` and `author` metadata.

## Template Aliases

The base templates are also aliased as the following:

+ `default`
    - aliases: `page`
+ `blog` - creates a list of its child pages
    - aliases: `folder`, `archive`, `index`
+ `item` - intended as a child page of `blog` directories.
    - aliases: `post`, `article`

Grav uses by default your text file's filename as your page's template, such as `pages/site-slug/templatename.md`. If you want to force a specific template on a markdown file, you may do so on the [frontmatter](https://learn.getgrav.org/17/content/headers). Add the following to your file header if your want your `this-is-my-text-title.md` page to use the `item` template:

```yaml
template: item
```

## Customizations

### Colors

`canvas` has support for device light and dark modes. You can also customize how your site uses its colors, or even force it to use light or dark mode only.

Make sure that after installing your ``canvas`` theme and activating it, you have copied `canvas.yaml` to `user/config/themes`. The theme will then use your color choices from the following attributes in the file.

```yaml
color:
  theme:
    behavior: 'theme_default' # can be 'light' or 'dark' only
  custom:
    light:
      bg: '#ffffff'
      accent-bg: '#f5f7ff'
      text: '#212121'
      text-light: '#585858'
      border: '#d8dae1'
      accent: '#004d40'
      code: '#795548'
      preformatted: '#444444'
      disabled: '#efefef'
    dark:
      bg: '#212121'
      accent-bg: '#2b2b2b'
      text: '#dcdcdc'
      text-light: '#ababab'
      border: '#666666'
      accent: '#00bcd4'
      code: '#ea80fc'
      preformatted: '#cccccc'
      disabled: '#111111'
```

The `Admin` panel will make this easier for you. Just select `canvas` as your theme, and below its metadata attributes you will find the Color tab.

### SEO

`canvas` has baked-in support for basic JSON-LD, Opengraph, Twitter Cards, and Breadcrumb schemas. You may also customize your Favicon image on a sitewide level, and your Opengraph preview image on a sitewide and per-page basis. 

We recommend using `Admin` for this. 

For sitewide preview images, login to your `admin` page, go to the `canvas` settings, and open the `Media` tab. Upload your preferred favicon and preview image.

For per-page preview images, open your page on the `admin` page, go to the `customize` page tab, and look for the `Preview Image` settings. Upload your preferred preview image for the site.

Clear your cache and view your page.

### Page Summary

`canvas` recommends using [page summaries](https://learn.getgrav.org/17/content/content-pages#summary-size-and-separator). It is used as your SEO description and is shown in the header of your page. Custom summaries have a specific location in the markdown file:

```markdown
---
# frontmatter here.
---

Page summary here.

===

Page content here.

```

You may disable page summaries from showing in your header by adding the following header to your page:

```yaml
enable_subtitle: false
```

### Layouts

#### Navigation

Navigation may be set sitewide, either as a set of buttons on the header or as a list on the footer. To toggle this, customize the following attribute on `config/canvas.yaml`:

```yaml
navigation: 'header' # or 'footer'
```

#### Item metadata

`item` templates can show their page metadata in the bottom of the content instead of the top.

To change the sitewide behavior, change the following attribute in `config/canvas.yaml`:

```yaml
item_place_attributes: 'header' # or 'content_footer'
```

To change this by page, add the following to your page header:

```yaml
place_attributes: 'header' # or 'content_footer'
```

## Pagination

Adding pagination support to your `blog` or collection templates requires adding and customizing the following page headers:

```yaml
content:
  items: '@self.children'
  order:
    by: header.date
    dir: desc
  pagination: true
  limit: 10
```

Pagination will not work without adding or customizing these attributes.