# CanberraJS code samples #
All code is technology neutral and is displayed in HTML and CSS.
1. [Write HTML according to specifications](https://canaxess.github.io/presentations/CanberraJS/1-html-according-spec.html)<br>
Two of the buttons on the page are created from `SPAN` and `DIV` elements. Attributes are added to make the generic elements behave as buttons whereas the `BUTTON` element just works and there is no need to add any further attributes.
1. [Make elements focusable from the keyboard](https://canaxess.github.io/presentations/CanberraJS/2-make-elements-focusable.html)<br> 
The bottom two links have an artifically set `TABINDEX` attribute which forces the elements to appear earlier in the keyboard tab sequence than their visual order.
1. [Updates need to be announced]()<br>Understand how using the `aria-live` attribute can help screen reader users understand dynamic changes in the content.
## Suggested downloads and further information ##
* Download [NVDA Screen reader](https://www.nvaccess.org/download/)
* Understand how to use [the accessibility pane](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference#pane) in Chrome and interpret the accessibility tree.
## NVDA 2018.2.1 and User Agent compatibility ##

&nbsp;        | Internet Explorer 11 | Edge | Chrome 72 | FireFox Quantum 65
:-------------: |:-------------:| :-----:| :-----:| :-----:
`tabindex`    | YES | YES | YES | NO*
`aria-live`    | ? | ? | ? | ?

*Firefox Quantum defaults to the first link on load
