# Creating Website Status Updates for the Blind, the Bold and the Beautiful #
If you were blind, do you think you could understand a websites status messages? Probably not, successfully saving an update, validation errors or timeouts would all be in an unreachable mess of `DIV` and `SPAN` elements invisible to screen readers. But it doesn't need to be this way, newly updated web accessibility standards have a specific technique for making status messages visible to screen readers. I'll show you how several small additions have a big impact and make your status messages standout for all.

## NVDA and browser compatibility ##
Testing how effectively screen readers prioritise the announcements.

&nbsp;        | Internet Explorer 11 | Edge | Chrome 74 | FireFox Quantum 66
:-------------: |:-------------:| :-----:| :-----:| :-----:
`role="status"`    | NO | NO | YES* | YES*
`role="alert"`    | NO | NO | YES | YES
`role="log"`    | NO | NO | YES* | YES*

NVDA version 2018.2.1<br>

### Note ###

Content added to live region using `document.getElementById` and `.innerText` property triggered 5seconds after page load. See [ARIA alert support](https://developer.paciellogroup.com/blog/2017/04/aria-alert-support/) for details about the way elements are added _may_ affect the screen reader announcing content.<br>
*reading of page text cuts off at the word 'several'<br>
