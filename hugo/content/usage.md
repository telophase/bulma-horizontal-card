+++
title = 'How to Use'
+++
How to use this extension.

{{% message color="info" %}}
**Note**: Horizontal cards are expected to have at least a `.card-image` element *and* a `.card-content` element. This extension relies on this assumption to correctly style horizontal cards. Do not use `.is-horizontal` with  cards that do not contain both elements. Vertical (normal) cards will work best.
{{% /message %}}

# Basic Usage

To make any card horizontal, add the class `.is-horizontal` to your `.card` element.

{{% card %}}
This is a card.
{{% /card %}}


## Image Alignment
By default, the `.card-image` element is aligned to the left. The `.card-image` can also be placed on the right by adding the class `.is-right` to the `.card-image` element.

{{% card  image-classes="is-right" %}}
This is a card with a right card image.
{{% /card %}}

## Image Size
The size of `.card-image` can be controlled by adding the classes `.is-small`, `is-normal` (default), `is-medium`, or `is-large` to the `.card-image` element.
{{% card image-classes="is-small" %}}
This card image is small using class `.is-small`.
{{% /card %}}
{{% card image-classes="is-normal" %}}
If you do not include a image size class, the card image will be this size. You can force it with the `.is-normal` class.
{{% /card %}}
{{% card image-classes="is-medium" %}}
This card image is medium using class `.is-medium`.
{{% /card %}}
{{% card image-classes="is-large" %}}
This card image is large using class `.is-large`.
{{% /card %}}


## Headers and Footers
Horizontal cards fully support the use of card header (`header.card-header`) and card footer (`footer.card-footer`) elements. Depending on where they are placed inside the `.card` div element, they will render as *inline* or *block*. You can mix and match inline and block headers/footers on the same card.

{{% message color="info" %}}
**Note**: Header and footer behaviour relies on what element the header and footer are. Make sure your headers are `<header>` elements, and your footers are `<footer>` elements.
{{% /message %}}

### Block
If you place your `.card-header` *outside* of `.card-content` and *before* `.card-image`, and/or you place your `.card-footer` *outside* of and *after* `.card-content`, you will get a full-width header or footer. It will appear outside of your `.card-image`, above or below, and span the full width of the card.

{{% card  outline-header="yes" outline-footer="yes" %}}
This card has a block header and a block footer.
{{% /card %}}

#### Fix Block Footers on Firefox with `.is-radiusless-bottom`
The removal of the bottom border radius on the `.card-image` when a block footer is used makes use of the [CSS pseudo-class `:has()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:has).

`:has()` is supported in Chrome, Edge, Opera, and Safari by default, and major mobile browers, but [not in Firefox without enabling a special flag](https://caniuse.com/css-has) (as of writing). It is NOT supported in any version of Internet Explorer.

To counteract this, special class `.is-radiusless-bottom` can be added to the `.card-image`. 

{{% message color="info" %}}
It is strongly recommended to add this class to all horizontal cards with block footers to ensure they display correctly on Firefox and other derived browsers.
{{% /message %}}

{{% card outline-footer="yes" %}}
This card has a block footer. On Firefox, the `.card-image` may still have a rounded bottom edge.
{{% /card %}}

{{% card outline-footer="yes" image-classes="is-radiusless-bottom" %}}
This card has a block footer. This card has class `.is-radiusless-bottom` applied to the `.card-image`. On Firefox, there should be no rounded edges on the `.card-image`.
{{% /card %}}

### Inline
If you place your `.card-header` or `.card-footer` elements *inside* `.card-content`, you will get an inline header or footer. It will be inline with your content and next to the `.card-image`.

{{% card  inline-header="yes" inline-footer="yes" force-bottom="yes" %}}
This card has an inline header and an inline footer.
{{% /card %}}

#### Special Class `.is-forced-bottom`
If your card is too tall, the `.card-footer` may appear to float inside the card. You can add the class `.is-force-bottom` to your `.card-footer`; this will cause it to stick to the bottom of the card. However, because this uses `position: absolute;`, the forced inline card footer will ignore internal margins and may appear too close to your other `.card-content`. 

The sticky effect of the class `.is-forced-bottom` is only active *after* the tablet breakpoint. It will not apply any unique styles or have a sticky effect on collapsed horizontal cards, even on forced cards with class `.is-collapsed`.

See the examples below. Check card behaviour per screen size before using this class.

{{% card-compare %}}

----

# Use with Image Ratio Classes
Bulma has several [responsive image aspect ratio classes (ratio modifiers)](https://bulma.io/documentation/elements/image/#responsive-images-with-ratios) that define how images are displayed responsively based only on dimensional ratio. 

By default, very long or very wide images may appear too large/small as `.card-image`. For horizontal `.card-image`s, these classes alter the apparent height without altering the image's actual dimensions (ie. no distortion).

These classes can be used to manipulate the height of the `.card-image`. Simply apply these classes to the `figure.image` element inside the `.card-image` div element. (See below)

```
<div class="card-image">
    <figure class="image is-XbyX">
        <img src="" alt=""/>
    </figure>
</div>
```

{{% card-compare-imageratios %}}

# Responsiveness
Horizontal cards are based on CSS flexboxes, just like the rest of Bulma. Horizontal cards try to follow Bulma's vertical-first philosophy, and so on smaller screens (below the tablet breakpoint) horizontal cards collapse back into "vertical" cards. 

Horizontal cards do not have interchangable syntax with normal cards. Dedicated CSS classes are used to maintain the different structure of horizontal cards while making them look just like normal vertical cards when collapsed. If you are using Javascript to toggle a horizontal card between vertical and horizontal orientations, **DO NOT remove the `.is-horizontal` class!**