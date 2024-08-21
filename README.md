# PostCSS Grid Reset

[postcss]: https://github.com/postcss/postcss

[![npm](https://img.shields.io/npm/v/postcss-grid-reset.svg)](https://www.npmjs.com/package/postcss-grid-reset) [![Build Status][ci-img]][ci]
[![npm](https://img.shields.io/npm/dt/postcss-grid-reset.svg)](https://www.npmjs.com/package/postcss-grid-reset)

[PostCSS] plugin for resetting CSS Grid. This plugin adds rule `min-width:0` to all direct descendants of element `display: grid`.

[postcss]: https://github.com/postcss/postcss

```css
.foo {
  display: grid;
}
```

```css
.foo {
  display: grid;
}

.foo > * {
  min-width: 0;
}
```

## 🔗 Links:

- [Preventing a Grid Blowout](https://css-tricks.com/preventing-a-grid-blowout/)
- [Prevent content from expanding grid items](https://stackoverflow.com/questions/43311943/prevent-content-from-expanding-grid-items)

## 🍳 Usage

**Step 1:** Install plugin:

```sh
npm install --save-dev postcss postcss-grid-reset
```

**Step 2:** Check you project for existed PostCSS config: `postcss.config.js`
in the project root, `"postcss"` section in `package.json`
or `postcss` in bundle config.

If you do not use PostCSS, add it according to [official docs]
and set this plugin in settings.

**Step 3:** Add the plugin to plugins list:

```diff
module.exports = {
  plugins: [
+   require('postcss-grid-reset'),
    require('autoprefixer')
  ]
}
```

[official docs]: https://github.com/postcss/postcss#usage

## Changelog

See [Releases history]

## License

[MIT]
