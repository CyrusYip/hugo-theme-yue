<!-- Timezone: UTC -->

## 2024-07-29

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
