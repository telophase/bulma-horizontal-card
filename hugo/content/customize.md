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
Depedening on your `NODE_ENV` settings, development dependencies for `bulma-horizontal-card` may not have been installed. Run the following code to install them explicitly. This will install Bulma, [Dart SASS](https://www.npmjs.com/package/sass), and CSS-Minify.

```sh
npm i @telophase/bulma-horizontal-card --only=dev
```
<br>

You can find the raw SASS at `../node_modules/@telophase/bulma-horizontal-card/sass/index.sass`. You can then build the SASS from that directory using the included scripts `css-build` and `css-min`.

{{% message color="warning" %}}
**NOTE**: Node-SASS has been deprecated. The included scripts use Dart SASS command syntax in order to compile CSS. If you wish to use node-SASS anyway, you'll need to edit the scripts in `package.json`.
{{% /message %}}

## Variables

### Unique to `bulma-horizontal-card`
| Syntax | Description | Default Value |
| --- | ----------- | ---- |
| `$hcard-image-default-size` | Default width of the `.card-image` in horizontal cards | `12.5%` |

{{% message color="primary" %}}
**TO-DO**: Add abstraction variables to horizontal cards to allow more granular customization.
{{% /message %}}