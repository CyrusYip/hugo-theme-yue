<!-- Timezone: UTC -->

## 2025-02-26

Support Arabic and improve French translation.

## 2025-01-01

Remove leading zero in Chinese dateFormat. Example: 2019年3月09日 -> 2019年3月9日.

## 2024-10-31

Add `_index.md` for sections.

## 2024-10-25

Add `head-start.html` and `body-end.html`.

---

Rename `comments_custom.html` to `single-end.html`. If you have `comments_custom.html`, you need to rename it accordingly.

---

Rename `head/custom.html` to `head/head-end.html`. If you have `head/custom.html`, you need to rename it accordingly.

---

Rename `_custom-*.scss` to `_style-*.scss`. If you have custom SCSS files, you need to rename them accordingly.

---

Move SCSS partial for faster CSS loading.

---

Rename `/assets/sass/` to `/assets/scss/`. If you have custom SCSS files, you need to rename them accordingly.

---

Remove unused JavaScript code.

## 2024-10-24

Add the page count to sections (`/posts/`, `/tags/`, etc.).

## 2024-10-18

Fix cell alignment in the table render hook. You need to upgrade Hugo to v0.136.0 .

Relevant issue: [Markdown render hook for tables doesn't recognize unset column alignment · Issue #12886 · gohugoio/hugo](https://github.com/gohugoio/hugo/issues/12886).

## 2024-10-09

Add class names for terms of a taxonomy, e.g., tags and categories. You can arrange terms into rows using this SCSS code:

```scss
.term-list {
  &__item {
    display: inline-block;
  }

  &__link {
    text-decoration-line: underline;
  }
}
```

## 2024-09-22

Break long words in lists to avoid overflowing.

## 2024-09-20

Only break long words for headings (`<h1>~<h6>`) and paragraphs (`<p>`).

---

Replace `word-break: break-word;` with `overflow-wrap: break-word;` since the former is deprecated in [CSS Text Module Level 3](https://drafts.csswg.org/css-text-3/#valdef-word-break-break-word).

> For compatibility with legacy content, the word-break property also supports a deprecated break-word keyword. When specified, this has the same effect as word-break: normal and overflow-wrap: anywhere, regardless of the actual value of the overflow-wrap property.

---

Use table render hook to add wrapper. Users need to upgrade Hugo to 0.134.2 .

## 2024-09-11

Add support for French.

## 2024-09-06

Set padding-inline to 0.25rem for inline code.

## 2024-07-31

Set the font size of the code block to 0.875rem (85% of the base font size).

---

Add padding to code block (https://github.com/CyrusYip/hugo-theme-yue/issues/7).

## 2024-07-30

Font size of footer is set to `smaller` (about 83.33%).

## 2024-07-29

Use fullwidth colon (`：`) for zh-CN in translation list. Example: `中文：文章 3`.

---

Apply BEM naming to translation list classes.

```html
<ul class="translation-list">
  <li class="translation-list__item">
    <a class="translation-list__link" href="/en/posts/post-4/">English: Post 4 Markdown Test</a>
  </li>
</ul>
```

---

Rename `i18n_list.html` to `translation_list.html`.

---

Add classes to links inside the page nav.

```html
<nav class="page-nav">
  <a class="page-nav__previous-link" href="/en/posts/post-5/">Prev: Post 5</a>
  <a class="page-nav__next-link" href="/en/posts/post-3/">Next: Post 3</a>
</nav>
```

## 2024-07-28

Table of contents is folded by default now. If you want folded one, set `params.tocFolded` to `true` in your config file.

```yaml
# hugo.yaml
params:
  toc: true
  tocFolded: true
```
