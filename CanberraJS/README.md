# CanberraJS code samples #
[Accessibility with Single Page Apps](https://www.slideshare.net/RossMullen2/accessibility-with-single-page-apps)
, all code is framework neutral and is displayed in HTML and CSS.
1. [Write HTML according to specifications](https://canaxess.github.io/presentations/CanberraJS/1-html-according-spec.html)<br>
Two of the buttons on the page are created from `SPAN` and `DIV` elements. Attributes are added to make the generic elements behave as buttons whereas the `BUTTON` element just works and there is no need to add any further attributes.
1. [Make elements focusable from the keyboard](https://canaxess.github.io/presentations/CanberraJS/2-make-elements-focusable.html)<br> 
The bottom two links have an artifically set `TABINDEX` attribute which forces the elements to appear earlier in the keyboard tab sequence than their visual order.<br> 
From CanberraJS questions - Two links with same tabindex value receive keyboard focus according to their DOM order.
1. [Updates need to be announced](https://canaxess.github.io/presentations/CanberraJS/3-updates-need-announcing.html)<br>
When the button is clicked the `DIV` element which has aria live region attributes updates and is audibly announced via a screen reader.<br> 
From CanberraJS questions - Two live regions updating simultaneoulsy.

## HTML and User Agent compatibility ##

&nbsp;        | Internet Explorer 11 | Edge | Chrome 72 | FireFox Quantum 65
:-------------: |:-------------:| :-----:| :-----:| :-----:
`tabindex`    | YES | YES | YES | NO*

## NVDA and User Agent compatibility ##

&nbsp;        | Internet Explorer 11 | Edge | Chrome 72 | FireFox Quantum 65
:-------------: |:-------------:| :-----:| :-----:| :-----:
`aria-live`    | YES | NO | YES | YES

NVDA version 2018.2.1<br>
*Firefox Quantum defaults to the first link on load

## Suggested downloads ##
* [NVDA Screen reader](https://www.nvaccess.org/download/)
