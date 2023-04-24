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
<br>

`bulma-horizontal-card` should now be built into your SASS and any compiled CSS from it.

## Edit SASS from NPM
Depedening on your `NODE_ENV` settings, development dependencies for `bulma-horizontal-card` may not have been installed. Run the following code to install them explicitly. This will install Bulma and [Dart SASS](https://www.npmjs.com/package/sass).

```sh
npm i @telophase/bulma-horizontal-card --only=dev
```
<br>

You can find the raw SASS at `../node_modules/@telophase/bulma-horizontal-card/sass/index.sass`. You can then build the SASS from that directory using the included scripts `css-build` and `css-min`.

{{% message color="warning" %}}
**NOTE**: Node-SASS has been deprecated. The included scripts use Dart SASS command syntax in order to compile CSS. If you wish to use node-SASS anyway, you'll need to edit the scripts in `package.json`.
{{% /message %}}

## Variables

### General Variables
To provide room to style or tweak horizontal cards separately from "normal" vertical cards, horizontal cards use unique variables for colors, radii, etc.

By default, these are mapped to the [same variables that normal cards use](https://bulma.io/documentation/components/card/#variables) (the "Equivalent" column in this chart).

| Name | Description | Equivalent | Default Value
| --- | ----------- | ---- | ---- |
| `$hcard-color` | Card text color. | `$card-color` | `$text` |
| `$hcard-background-color` | Card background color. | `$card-background-color` | `$scheme-main` |
|`$hcard-shadow` | Card shadows. | `$card-shadow` | `$shadow` |
|`$hcard-radius` | Card radius (roundness). | `$card-radius` | `0.25rem` |
`$hcard-header-background-color`|Background color for card headers. | `$card-header-background-color` | `transparent` |
| `$hcard-header-color`| Card header text color. | `$card-header-color` | `$text-strong` |
| `$hcard-header-padding`| Text padding in card headers. | `$card-header-padding`| `0.75rem 1rem`|
| `$hcard-header-shadow`| Shadows for card headers. | `$card-header-shadows`| `0 0.125em 0.25em rgba($scheme-invert, 0.1)`|
| `$hcard-header-weight` | Font weight for card header text. | `$card-header-weight`| `$weight-bold`|
| `$hcard-content-background-color`| Card content background color. | `$card-content-background-color`| `transparent` |
| `$hcard-content-padding` |  Padding for internal card contents. | `$card-content-padding` | `transparent` |
| `$hcard-footer-background-color` | Background color for the card footer. | `$card-footer-background-color` | `transparent`|
| `$hcard-footer-border-top` | Definition of the card footer top border | `$card-footer-border-top` |`1px solid $border-light`|
| `$hcard-footer-padding` | Padding around card footers. | `$card-footer-padding` | `0.75rem` |
| `$hcard-media-margin` | Margin around card media | `$card-media-margin` | `$block-spacing` |

### Unique to `bulma-horizontal-card`
These variables are used by horizontal cards only and are not shared with/inherited by normal cards.

| Name | Description | Default Value |
| --- | ----------- | ---- |
| `$hcard-image-default-size` | Width of the `.card-image` in horizontal cards | `12.5%` |
