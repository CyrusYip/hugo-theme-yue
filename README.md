# Yue

**[Demo website](https://yue.cyrusyip.org/)** | [Changelog](CHANGELOG.md)

Yue is a minimal, multilingual and customizable Hugo theme, suitable for blogging.

## Screenshots

Screenshots may be outdated, so it's better to visit the [demo website](https://yue.cyrusyip.org/).

<details open>
  <summary>Light mode on desktop</summary>
  
  ![light-desktop](https://cdn.jsdelivr.net/gh/CyrusYip/hugo-theme-yue@images/light-desktop.png)
</details>

<details>
  <summary>Dark mode on desktop</summary>
  
  ![dark-desktop](https://cdn.jsdelivr.net/gh/CyrusYip/hugo-theme-yue@images/dark-desktop.png)
</details>

<details>
  <summary>Light mode on mobile</summary>
  
  ![light-mobile](https://cdn.jsdelivr.net/gh/CyrusYip/hugo-theme-yue@images/light-mobile.png)
</details>

<details>
  <summary>Dark mode on mobile</summary>
  
  ![dark-mobile](https://cdn.jsdelivr.net/gh/CyrusYip/hugo-theme-yue@images/dark-mobile.png)
</details>


## Features

- Minimal appearance
- Easy to install (with Git and Hugo installed, create a website in a few seconds)
- Detailed documentation
- Automatic dark mode
- Multilingual
    - Translation list in single page
    - Language selector (go to corresponding page or homepage)
- Multiple authors
- Table of Content (foldable, only generated when available)
- Modification date on home page, single page, section page and term page
- Custom date format
- Pagination on home page and section page
- Full-text RSS
- Tags and categories
- Copyright notice (author and year span can be set)
- RSS link
- Heading anchor link
- Mobile-first and responsive
- SCSS
- Search engine optimization
    - [Microdata](https://developer.mozilla.org/en-US/docs/Web/HTML/Microdata)
    - meta description
- [Open Graph](https://ogp.me/)
- Page count to sections (`/posts/`, `/tags/`, etc.)
- Customization
    - Favicon
    - Styles (SCSS)
    - Contents (HTML)

To find out all features, check [hugo.yaml](hugo.yaml) (default configuration) and [exampleSite/hugo.yaml](exampleSite/hugo.yaml) (demo site's configuration).

## Get started

### Install

Install [Git](https://git-scm.com/downloads) and latest [Hugo extended](https://gohugo.io/installation/).

```shell
# Create website
git init my-website
cd my-website
# Install theme
git submodule add --depth=1 https://github.com/CyrusYip/hugo-theme-yue themes/hugo-theme-yue
git commit --message "add theme"
# Create demo content
cp --recursive themes/hugo-theme-yue/exampleSite/* .
# Preview
hugo server
```

Now we have a working demo webiste. The `content` directory contains the content, and `hugo.yaml` is configuration file. Feel free to play around with them.

### Update theme

```shell
cd my-website
git submodule update --remote
```

It's recommended to read [CHANGELOG.md](CHANGELOG.md) before updating the theme.

You can subscribe updates and the changelog in a feed aggregator (e.g. Inoreader).

- Updates: <https://github.com/CyrusYip/hugo-theme-yue/commits/main.atom>
- Changelog: <https://github.com/CyrusYip/hugo-theme-yue/commits/main/CHANGELOG.md.atom>

### Clone website

You need to use additional options when you clone your website project.

```shell
git clone --recurse-submodules --shallow-submodules git@github.com:your-user-name/my-website.git
```

### Deploy

After setting up the website, you probably want to host it on Internet. There are many methods for doing it, see [Hosting and deployment | Hugo](https://gohugo.io/hosting-and-deployment/). If you don't know what to choose, you can start from Netlify, see [Host on Netlify | Hugo](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/).

Make sure you change baseURL to your domain name (e.g. `https://my-cool-domain.org/`) in `hugo.yaml`.

```diff
-baseURL: https://yue.cyrusyip.org/
+baseURL: https://my-cool-domain.org/
```

Recommended build command:

```shell
hugo --gc --minify
```

`--gc` remove unused cache files
, and `--minify` reduce the size of the website (mainly HTML).

## Usage

Create a new post.

```
hugo new content content/en/posts/my-first-post.md
```

To learn more about usage, see:

- [Basic usage | Hugo](https://gohugo.io/getting-started/usage/)
- [Directory structure | Hugo](https://gohugo.io/getting-started/directory-structure/)

## Config

Settings are listed in [exampleSite/hugo.yaml](exampleSite/hugo.yaml) (demo site's config) and [hugo.yaml](hugo.yaml) (default config, imported by the former).

In the root of your website project, `hugo.yaml` is the config file, which is a copy of [exampleSite/hugo.yaml](exampleSite/hugo.yaml).

To learn configuration, see [Configure Hugo | Hugo](https://gohugo.io/getting-started/configuration/).

### Multilingual mode

Supported languages:

- `ar`: Arabic
- `en`: English
- `fr`: French
- `zh-CN`: Simplified Chinese

To create a multilingual website, see [Multilingual mode | Hugo](https://gohugo.io/content-management/multilingual/) and [exampleSite/hugo.yaml](exampleSite/hugo.yaml).

Translation files are located in the [i18n](i18n) directory and [data/i18n.yaml](data/i18n.yaml). Contributions for additional languages are welcome.

To contribute a new language:

1. Create a language file (e.g., `fr.yaml` for French) in the [i18n](i18n) directory.
1. Copy the content of [i18n/en.yaml](i18n/en.yaml) into the new file.
1. Remove all comments (`# ...`) and translate the content.
1. Translate the content in [data/i18n.yaml](data/i18n.yaml) as well.

If you want to keep contributing to translation, you can get latest changes by subscribing the feed of [i18n/en.yaml](i18n/en.yaml) (<https://github.com/CyrusYip/hugo-theme-yue/commits/main/i18n/en.yaml.atom>) using an RSS reader.

#### Title of tags and categories

If your website is not in English, you probably want to customize title of `/tags` and `/categories`.

For example, to customize `/tags` title of `zh-CN` website, create `content/zh-CN/tags/_index.md` and add the following content into the file.

```
---
title: Chinese Tags
---
```

## Customize

Yue allows you to customize favicon, styles (SCSS), and contents (HTML).

### Favicon

Favicon is the icon next to title in a browser tab. To use your favicon, put `favicon.ico` under `static` directory. You can create `favicon.ico` on online favicon.ico generators.

### Styles (SCSS)

Yue uses SCSS (libsass) to add styles. All files are in [assets/scss](assets/scss).To customize styles, create `assets/scss/_style-start.scss` and `assets/scss/_style-end.scss`.

`_style-start.scss` is applied first, and you can override variables in this file.

```scss
$base-font-size: 15px;
```

`_style-end.scss` is applied last, and you can add styles in this file.

Vanilla CSS is also valid in SCSS.

References:

- [CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Sass: Sass Basics](https://sass-lang.com/guide/)
- [Directory structure | Hugo](https://gohugo.io/getting-started/directory-structure/)

### Contents (HTML)

You can create these files to insert HTML code.

- `layouts/partials/head/head-start.html`
- `layouts/partials/head/head-end.html`
- `layouts/partials/single/single-end.html`
- `layouts/partials/body/body-end.html`

#### head-start.html

`head-start.html` is added near the start of the `<head>` element.

Use cases:

- Preload scripts
- Load scripts
- Load styles

Here is an example of preloading scripts:

```html
<link rel="preload" as="script" href="https://unpkg.com/@swup/head-plugin@2">
<link rel="preload" as="script" href="https://unpkg.com/@swup/preload-plugin@3">
<link rel="preload" as="script" href="https://unpkg.com/swup@4">
```

#### head-end.html

`head-end.html` is added to the end of the `<head>` element.

Use cases:

- Load scripts
- Load styles

Here is an example of adding Google Analytics and a local script:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-F46B15BRUF"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-F46B15BRUF');
</script>

<!-- Local script, path: assets/js/my-script.js -->
{{ with resources.Get "js/my-script.js" | js.Build }}
  <script defer src="{{ .RelPermalink }}"></script>
{{ end }}
```

#### single-end.html

`single-end.html` is added to the end of the `<main>` element in a post.

Use cases:

- comment services, e.g., Disqus and giscus

Here is an example of adding [Giscus](https://giscus.app/):

```html
{{ $language := "" }}
{{- /*
Workaround for lowercase LanguagePrefix,
see https://github.com/gohugoio/hugo/issues/9404
*/ -}}
{{ if eq site.LanguagePrefix "/zh-cn" }}
  {{ $language = "zh-CN" }}
{{ else }}
  {{ $language = "en" }}
{{ end }}
<script src="https://giscus.app/client.js"
        data-repo="CyrusYip/yue-test"
        data-repo-id="P_9hJMbXtqr"
        data-category="General"
        data-category-id="SIB_ldsflk712ldRsjf7"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="bottom"
        data-theme="preferred_color_scheme"
        data-lang="{{ $language }}"
        crossorigin="anonymous"
        async>
</script>
```

List of comment services: [Comments | Hugo](https://gohugo.io/content-management/comments/).

#### body-end.html

`body-end.html` is added to the end of the `<body>` element.

Use cases:

- Dynamically load scripts

## Support

To report bugs, submit an [issue](https://github.com/CyrusYip/hugo-theme-yue/issues). To ask questions, start a [discussion](https://github.com/CyrusYip/hugo-theme-yue/discussions).

## Further reading

Hugo has many features, read [Hugo Documentation](https://gohugo.io/documentation/) to learn.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## Development

This project uses [hugo-bin - npm](https://www.npmjs.com/package/hugo-bin) to manage Hugo version. Prerequisite: [Node.js](https://nodejs.org/en) and [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).

Clone this repository.

```shell
npm install
npm run clean:server:shared
```

There are other useful commands listed in [package.json](package.json). To use recommended Hugo version, run `npx hugo`.

---

If you don't have Node.js and npm installed, just install the version listed in [package.json](package.json).

```json
"hugo-bin": {
  "buildTags": "extended",
  "version": "x.yyy.z"
},
```

CHANGELOG.md should be updated in each commit.

## Websites built with Yue

If you are using Yue and source code of your website is hosted on GitHub, you can add `hugo-theme-yue` topic to your repository.

[Link to `hugo-theme-yue` topic](https://github.com/topics/hugo-theme-yue).

## Acknowledgement

I have learned a lot from many projects. Thank you, developers.

- [hugo-xmin](https://github.com/yihui/hugo-xmin/) (minimal templates)
- [hugo-theme-jane](https://github.com/xianmin/hugo-theme-jane/) ([RSS template](https://github.com/xianmin/hugo-theme-jane/blob/6bef93b29e96bcf8b5b9a86b94cdd0dce99002bc/layouts/rss.xml#L30))
- [hugo-theme-zen](https://github.com/frjo/hugo-theme-zen) ([language selector](https://github.com/frjo/hugo-theme-zen/blob/d3b2b6e1eea2bc67b3409238b9c347ab628876da/layouts/partials/language-selector.html))
- [hugo-theme-gruvbox](https://github.com/schnerring/hugo-theme-gruvbox) (color)
- [gruvbox](https://github.com/morhetz/gruvbox) (color)
- [hugo-theme-stack](https://github.com/CaiJimmy/hugo-theme-stack) (source code, documentation and config)
- [hugo-PaperMod](https://github.com/adityatelange/hugo-PaperMod) (source code, documentation and config)

## License

This project is licensed under [MIT](LICENSE).
