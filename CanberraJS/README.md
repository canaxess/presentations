# CanberraJS code samples #
All code is technology neutral and is displayed in HTML and CSS.
1. [Write HTML according to specifications](https://canaxess.github.io/presentations/CanberraJS/1-html-according-spec.html)<br>Observe how `span` and `div` elements can trigger actions but have no semantic meaning.
1. [Make elements focusable from the keyboard](https://canaxess.github.io/presentations/CanberraJS/2-make-elements-focusable.html)<br> Understand how artificially setting a `tabindex` on HTML elements can affect the keyboard focus sequence of the page.
1. [Updates need to be announced]()<br>Understand how using the `aria-live` attribute can help screen reader users understand dynamic changes in the content.
## Suggested downloads and further information ##
* Download [NVDA Screen reader](https://www.nvaccess.org/download/)
* Understand how to use [the accessibility pane](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference#pane) in Chrome and interpret the accessibility tree.
## NVDA 2018.2.1 and User Agent compatibility ##

&nbsp;        | Internet Explorer 11 | Edge | Chrome 72 | FireFox Quantum 65
:-------------: |:-------------:| :-----:| :-----:| :-----:
`tabindex`    | YES | YES | YES | NO*
`aria-live`    | ? | ? | ? | ?

*Firefox Quantum defaults to the first link on load, this requires further investigation
