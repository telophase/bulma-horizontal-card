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

#### Inline
If you place your `.card-header` or `.card-footer` elements *inside* `.card-content`, you will get an inline header or footer. It will be inline with your content and next to the `.card-image`.

{{% card  inline-header="yes" inline-footer="yes" force-bottom="yes" %}}
This is a card.
{{% /card %}}

#### Block
If you place your `.card-header` *outside* of `.card-content` and *before* `.card-image`, and/or you place your `.card-footer` *outside* of and *after* `.card-content`, you will get a full-width header or footer. It will appear outside of your `.card-image`, above or below, and span the full width of the card.

{{% card  outline-header="yes" outline-footer="yes" %}}
This is a card.
{{% /card %}}

## `border-radius` Helper Classes

## Notes: Image Ratio Classes

## Notes: Responsiveness