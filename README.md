# Theme Name

## Development

```
npm install
npm run serve
```

To use recommended Hugo version, run `npx hugo`.

## Features

- [x] mobile-first
- [x] tags
- [x] categories
- [x] scss (libsass)
- [x] full-text RSS (enabled by default)
- [x] show translations
- [x] customize date format
- [x] language selector
- [x] paginator
    - [x] homepage
    - [x] section
- [x] author in single page (single or list)
- [x] 404 page
- [x] lastmod in homepage, single page, section, and term
- [x] CSS BEM (Block, Element, Modifier)
- [x] gruvbox color scheme (automatic dark mode)
- [x] customize styles via scss
- [x] copyright notice (author and year span can be set)
- [x] RSS link
- [x] [Open Graph](https://ogp.me/)
- [x] [Microdata](https://developer.mozilla.org/en-US/docs/Web/HTML/Microdata)

## Installation

## Configuration

### customize styles

To customize styles, create `/assets/sass/_custom-start.scss` (applied first) and `/assets/sass/_custom-end.scss` (applied last) in your site. You can override variables in `_custom-start.scss`. Vanilla CSS is also valid in SCSS.

### title of `/tags` and `/categories`

If your website is not in English, you probably want to customize title of `/tags`.

For example, to customize `/tags` title of `zh-CN` website, create `content/zh-CN/tags/_index.md` and add the following content into the file.

```
---
title: 标签
---
```
