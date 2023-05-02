<div align="center">
<img src="hugo/static/hcard.png" style="max-width: 80%;">
<h1>bulma-horizontal-card</h1>
<p>
<a href="https://www.npmjs.com/package/@telophase/bulma-horizontal-card"><img src="https://img.shields.io/npm/v/@telophase/bulma-horizontal-card?logo=npm" alt="npm"></a>
<a href="https://www.npmjs.com/package/@telophase/bulma-horizontal-card?activeTab=dependencies"><img src="https://img.shields.io/npm/dependency-version/@telophase/bulma-horizontal-card/bulma?label=bulma%20version&logo=bulma"></a>
<a href="https://www.npmjs.com/package/@telophase/bulma-horizontal-card"><img src="https://img.shields.io/npm/dw/@telophase/bulma-horizontal-card?logo=npm" alt="npm downloads"></a> 
<a href=""><img src="https://img.shields.io/github/last-commit/telophase/bulma-horizontal-card?label=last%20commit&logo=github"></a>
<a href="https://www.npmjs.com/package/@telophase/bulma-horizontal-card"><img src="https://img.shields.io/npm/l/@telophase/bulma-horizontal-card"></a>
<a href="https://ko-fi.com/gimon"><img src="https://img.shields.io/static/v1?label=support&amp;color=blueviolet&amp;message=@%20ko-fi&amp;logo=ko-fi" alt="support development"></a></p>
<p>
</div>

An extension for [Bulma CSS framework](https://github.com/jgthms/bulma)  to support responsive horizontal cards, since [the project owner is not interested in maintaining the feature](https://github.com/jgthms/bulma/pull/1596#issuecomment-429735282).  The syntax and classes of vanilla ("normal") cards are reused and preserved, so you can still use headers and footers! It is also highly customizable; horizontal cards can be styled independently of normal ones via distinct SASS variables.

**Documentation, installation instructions, and demonstrations can be found here: https://dev.gimon.zone/bulma-horizontal-card/~site**.

## important notice!
This extension makes use of the [CSS pseudo-class `:has()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:has) in order to achieve automatic/contextual control of the `.card-image`'s `border-radius`. Specifically, it is used in a single case to control the removal of the bottom `border-radius` from the `.card-image` when a `footer.card-footer` element is present as a child of `.card`. This was the best way I could think to implement this.

`:has()` is supported in Chrome, Edge, Opera, and Safari by default, and major mobile browers, but [not in Firefox without enabling a special flag](https://caniuse.com/css-has) (as of writing). It is NOT supported in any version of Internet Explorer.

An additional utility class is included that can force the `.card-image` to be correct. See [usage](https://dev.gimon.zone/bulma-horizontal-card/~site/usage/#fix-block-footers-on-firefox-with-is-radiusless-bottom) for more information.

## to do
- [ ] Add classes for defining `.card-image` width
- [ ] Fine-tune responsiveness of horizontal cards
- [ ] Improve responsiveness of the sticky inline-footer

## contributing
Contributions to this extension are always welcome, be they new code, small fixes, or edits to the documentation!

Though this project officially lives at [my OneDev instance](https://dev.gimon.zone/bulma-horizontal-card/~files) for local CI jobs, [the main mirror on Github](https://github.com/telophase/bulma-horizontal-card) accepts contributions.  Any changes are synced between the two repos via CI.

Fork this project on Github and file a pull request (or simply file an issue), and I'll merge it back into main.

## license
&#169; [Alex H.](https://gimon.zone) ([@telophase](https://github.com/telophase)) 2023-present.<br>
MIT License.

Initial code and CSS class syntax based on the work/input of contributors in [this Bulma pull request](https://github.com/jgthms/bulma/pull/1596). Thank you!

