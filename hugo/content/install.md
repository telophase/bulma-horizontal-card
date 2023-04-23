+++
title = 'Install Extension'
+++

How to install the extension.

## Via NPM for Bulma SASS
Install `bulma-horizontal-card` via NPM CLI.
```sh
npm i @telophase/bulma-horizontal-card
```

<br><br>

You can then integrate the extension into your Bulma SASS project by importing the `index.sass` file in your SCSS *after* importing Bulma.
```scss
@import "./node_modules/@telophase/bulma-horizontal-card/src/sass/index.sass";
```

## Via CDN as precompiled
The `bulma-horizontal-card` extension's compiled CSS is available via jsDeliver's global CDN. Be sure you are also importing Bulma's CSS as well.

**Import in CSS**

```css
/* unminified */
@import "https://cdn.jsdelivr.net/npm/@telophase/bulma-horizontal-card/@latest/css/bulma-horizontal-card.css"

/* minified */
@import "https://cdn.jsdelivr.net/npm/@telophase/bulma-horizontal-card/@latest/css/bulma-horizontal-card.min.css"
```

<br><br>

**Import in HTML**
```html
<!-- unminified -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@telophase/bulma-horizontal-card/@latest/css/bulma-horizontal-card.css">

<!-- minified -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@telophase/bulma-horizontal-card/@latest/css/bulma-horizontal-card.min.css">
```

## From Github as precompiled
Download the repository tarball/ZIP and extract anywhere. Move the files to the location of your choice.
