# Theme Name

## Development

```
npm install
npm run serve
```

To use recommended Hugo version, run `npx hugo`.

## Features

- [x] mobile-first
- [x] stretch `<main>` to avoid additional space below `<footer>` (demo: `/categories/`)
- [x] tags
- [x] categories
- [x] scss (libsass)
- [x] full-text RSS (enabled by default)
- [x] show translations
- [x] customize footer
- [x] customize date format
- [x] language selector

## Installation

## Configuration

### title of `/tags` and `/categories`

If your website is not in English, you probably want to customize title of `/tags`.

For example, to customize `/tags` title of `zh-CN` website, create `content/zh-CN/tags/_index.md` and add the following content into the file.

```
---
title: 标签
---
```
