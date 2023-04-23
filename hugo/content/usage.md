+++
title = 'How to Use'
+++
How to use this extension.

{{% message color="info" %}}
**Note**: Horizontal cards are expected to have at least a `.card-image` element *and* a `.card-content` element. This extension relies on this assumption to correctly style horizontal cards. Do not use `.is-horizontal` with  cards that do not contain both elements. Vertical (normal) cards will work best.
{{% /message %}}

## Basic Usage

To make any card horizontal, add the class `.is-horizontal` to your `.card` element.

{{% card %}}
This is a card.
{{% /card %}}



### Image Alignment
By default, the `.card-image` element is aligned to the left. The `.card-image` can also be placed on the right by adding the class `.is-right` to the `.card-image` element.

{{% card  image-classes="is-right" %}}
This is a card with a right card image.
{{% /card %}}

### Headers and Footers
Horizontal cards fully support the use of card header (`header.card-header`) and card footer (`footer.card-footer`) elements. Depending on where they are placed inside the `.card` div element, they will render as *inline* or *block*. You can mix and match inline and block headers/footers on the same card.

{{% message color="info" %}}
**Note**: Header and footer behaviour relies on what element the header and footer are. Make sure your headers are `<header>` elements, and your footers are `<footer>` elements.
{{% /message %}}

#### Block
If you place your `.card-header` *outside* of `.card-content` and *before* `.card-image`, and/or you place your `.card-footer` *outside* of and *after* `.card-content`, you will get a full-width header or footer. It will appear outside of your `.card-image`, above or below, and span the full width of the card.

{{% card  outline-header="yes" outline-footer="yes" %}}
This card has a block header and a block footer.
{{% /card %}}

#### Inline
If you place your `.card-header` or `.card-footer` elements *inside* `.card-content`, you will get an inline header or footer. It will be inline with your content and next to the `.card-image`.

{{% card  inline-header="yes" inline-footer="yes" force-bottom="yes" %}}
This card has an inline header and an inline footer.
{{% /card %}}

#### Special Class `.is-forced-bottom`
If your card is too tall, the `.card-footer` may appear to float inside the card. You can add the class `.is-force-bottom` to your `.card-footer`; this will cause it to stick to the bottom of the card. However, because this uses `position: absolute;`, the forced inline card footer will ignore internal margins and may appear too close to your other `.card-content`. 

See the examples below. Check card behaviour per screen size before using this class.

{{% card-compare %}}

{{% message color="primary" %}}
**TO-DO**: Improve responsiveness of `.is-forced-bottom`.
{{% /message %}}

----

## `border-radius` Helper Classes
{{% message color="primary" %}}
**TO-DO**: Add helper classes.
{{% /message %}}

## Use with Image Ratio Classes
Bulma has several [responsive image aspect ratio classes (ratio modifiers)](https://bulma.io/documentation/elements/image/#responsive-images-with-ratios) that define how images are displayed responsively based only on dimensional ratio. 

By default, very long or very wide images may appear too large/small as `.card-image`. For horizontal `.card-image`s, these classes alter the apparent height without altering the image's actual dimensions (ie. no distortion).

These classes can be used to manipulate the height of the `.card-image`. Simply apply these classes to the `figure.image` element inside the `.card-image` div element.

```
<div class="card-image">
    <figure class="image is-XbyX">
        <img src="" alt=""/>
    </figure>
</div>
```

{{% card-compare-imageratios %}}

## Notes on Responsiveness
Horizontal cards are based on CSS flexboxes, just like the rest of Bulma.

{{% message color="primary" %}}
**TO-DO**: Fine-tune horizontal card responsiveness.
{{% /message %}}