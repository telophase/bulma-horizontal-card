+++
title = 'bulma-horizontal-card'
date = "2023-04-22"
+++
![](hcard.png)
{.has-text-centered}

# bulma-horizontal-card
{.has-text-centered}

[![npm](https://img.shields.io/npm/v/@telophase/bulma-horizontal-card)](https://www.npmjs.com/package/@telophase/bulma-horizontal-card) [![npm downloads](https://img.shields.io/npm/dw/@telophase/bulma-horizontal-card)](https://www.npmjs.com/package/@telophase/bulma-horizontal-card) [![support development](https://img.shields.io/static/v1?label=support&color=blueviolet&message=@%20ko-fi&logo=ko-fi)](https://ko-fi.com/gimon)
{.has-text-centered}

A [Bulma CSS](https://github.com/jgthms/bulma) extension to support horizontal cards. Built for the latest version of Bulma (0.9.4)! You'll need it in order for this code to work.
{.has-text-centered}


## notices

{{% message color="danger" title="WARNING: potential compatibility issues" %}}
This extension makes use of the [CSS pseudo-class `:has()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:has) in order to achieve automatic/contextual control of the `.card-image`'s `border-radius`. Specifically, it is used in a single case to control the removal of the bottom `border-radius` from the `.card-image` when a `footer.card-footer` element is present as a child of `.card`. This was the best way I could think to implement this.

`:has()` is supported in Chrome, Edge, Opera, and Safari by default, and major mobile browers, but [not in Firefox without enabling a special flag](https://caniuse.com/css-has) (as of writing). It is NOT supported in any version of Internet Explorer.

So, this extension includes an additional utility class that can force the `.card-image` to be correct. See [usage](usage/#fix-block-footers-on-firefox-with-is-radiusless-bottom) for more information.
{{% /message %}}

## contributing
Contributions to this extension are always welcome!

Though this project officially lives at [dev.gimon.zone](https://dev.gimon.zone/bulma-horizontal-card/~files), there is a [mirror on Github](https://github.com/telophase/bulma-horizontal-card) that accepts contributions. 

Fork this project on Github and file a pull request, and I'll merge it back into main. :)

## license
&#169; [Alex H.](https://gimon.zone) 2023-present. <br> MIT License.

Initial code and CSS class syntax based on the work/input of contributors in [this Bulma pull request](https://github.com/jgthms/bulma/pull/1596). Thank you!


