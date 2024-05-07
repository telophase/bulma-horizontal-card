+++
title = 'Home'
date = "2023-04-22"
+++
![](hcard.png)
{.has-text-centered}

# bulma-horizontal-card
{.has-text-centered}

[![npm](https://img.shields.io/npm/v/@telophase/bulma-horizontal-card?logo=npm)](https://www.npmjs.com/package/@telophase/bulma-horizontal-card) [![](https://img.shields.io/npm/dependency-version/@telophase/bulma-horizontal-card/bulma?label=bulma%20version&logo=bulma)](https://www.npmjs.com/package/@telophase/bulma-horizontal-card?activeTab=dependencies) [![npm downloads](https://img.shields.io/npm/dw/@telophase/bulma-horizontal-card?logo=npm)](https://www.npmjs.com/package/@telophase/bulma-horizontal-card) [![](https://img.shields.io/github/last-commit/telophase/bulma-horizontal-card?label=last%20commit&logo=github)](https://github.com/telophase/bulma-horizontal-card/commits/main) [![](https://img.shields.io/npm/l/@telophase/bulma-horizontal-card)](https://www.npmjs.com/package/@telophase/bulma-horizontal-card) [![support development](https://img.shields.io/static/v1?label=support&color=blueviolet&message=@%20ko-fi&logo=ko-fi)](https://ko-fi.com/gimon)
{.has-text-centered}

An extension for [Bulma CSS framework](https://github.com/jgthms/bulma)  to support responsive horizontal cards, since [the project owner is not interested in maintaining the feature](https://github.com/jgthms/bulma/pull/1596#issuecomment-429735282).  The syntax and classes of vanilla ("normal") cards are reused and preserved, so you can still use headers and footers! It is also highly customizable; horizontal cards can be styled independently of normal ones via distinct SASS variables.

## notices
{{% message color="warning" title="Bulma V1 Update" %}}
As of Bulma version 1.0.0, this extension has not been superceeded by any new functionality and is still works as normal. I will add any new feature(s) to better integrate with any other Bulma updates going forward.
{{% /message %}}

{{% message color="danger" title="WARNING: potential compatibility issues" %}}
This extension makes use of the [CSS pseudo-class `:has()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:has) in order to achieve automatic/contextual control of the `.card-image`'s `border-radius`. Specifically, it is used in a single case to control the removal of the bottom `border-radius` from the `.card-image` when a `footer.card-footer` element is present as a child of `.card`. This was the best way I could think to implement this.

`:has()` is supported in Chrome, Edge, Opera, and Safari by default, and major mobile browers, but [not in Firefox without enabling a special flag](https://caniuse.com/css-has) (as of writing). It is NOT supported in any version of Internet Explorer.

So, this extension includes an additional utility class that can force the `.card-image` to be correct. See [the usage page](usage/#fix-block-footers-on-firefox-with-is-radiusless-bottom) for more information.
{{% /message %}}

## contributing
Contributions to this extension are always welcome, be they new code, small fixes, or edits to the documentation!

Fork this project on Github and file a pull request (or simply file an issue), and I'll merge it back into main.

## license
&#169; [Alex H @telophase](https://github.com/telophase) 2023-present.
MIT License.

Initial code and CSS class syntax based on the work/input of contributors in [this Bulma pull request](https://github.com/jgthms/bulma/pull/1596). Thank you!


