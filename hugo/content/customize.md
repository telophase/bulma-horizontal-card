+++
title = "Customize Extension"
+++

How to customize the extension and use it in your Bulma project.

## Install Bulma
If you don't already have Bulma installed, it should have been installed when you installed [`bulma-horizontal-card` via NPM](../install/#via-npm-for-bulma-sass) as it is a dependency.

You can install Bulma manually with:
```sh
npm i bulma
```

## Import into your SASS/CSS
After you've installed [`bulma-horizontal-card` via NPM](../install/#via-npm-for-bulma-sass) into your Bulma project directory, you can integrate it into your SCSS/SASS by adding the following line. Place this line *after* the line(s) that import Bulma (or at minimum, Bulma's `components/card.sass`)

```scss
// scss
@import '@telophase/bulma-horizontal-card'
```

```sass
// sass
@import @telophase/bulma-horizontal-card
```

## Variables

### Unique to `bulma-horizontal-card`
| Syntax | Description | Default Value |
| --- | ----------- | ---- |
| `$hcard-image-default-size` | Default width of the `.card-image` in horizontal cards | `12.5%` |

## Build CSS from SASS