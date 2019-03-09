# CanberraJS code samples #
All code is technology neutral and is displayed in HTML and CSS.
1. [Write HTML according to specifications](https://canaxess.github.io/presentations/CanberraJS/1-html-according-spec.html)<br>
Two of the buttons on the page are created from `SPAN` and `DIV` elements. Attributes are added to make the generic elements behave as buttons whereas the `BUTTON` element just works and there is no need to add any further attributes.
1. [Make elements focusable from the keyboard](https://canaxess.github.io/presentations/CanberraJS/2-make-elements-focusable.html)<br> 
The bottom two links have an artifically set `TABINDEX` attribute which forces the elements to appear earlier in the keyboard tab sequence than their visual order.
1. [Updates need to be announced](https://canaxess.github.io/presentations/CanberraJS/3-updates-need-announcing.html)<br>
When the button is clicked the `DIV` element which has aria live region attributes updates and is audibly announced via a screen reader.

## HTML and User Agent compatibility ##

&nbsp;        | Internet Explorer 11 | Edge | Chrome 72 | FireFox Quantum 65
:-------------: |:-------------:| :-----:| :-----:| :-----:
`tabindex`    | YES | YES | YES | NO*

*Firefox Quantum defaults to the first link on load

## NVDA<sup>i</sup> and User Agent compatibility ##

&nbsp;        | Internet Explorer 11 | Edge | Chrome 72 | FireFox Quantum 65
:-------------: |:-------------:| :-----:| :-----:| :-----:
`aria-live`    | ? | ? | YES | ?

<sup>i</sup>NVDA version 2018.2.1<br>

## Suggested downloads ##
* [NVDA Screen reader](https://www.nvaccess.org/download/)
