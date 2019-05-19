# Creating Website Status Updates for the Blind, the Bold and the Beautiful #
If you were blind, do you think you could understand a websites status messages? Probably not, successfully saving an update, validation errors or timeouts would all be in an unreachable mess of `DIV` and `SPAN` elements invisible to screen readers. But it doesn't need to be this way, newly updated web accessibility standards have a specific technique for making status messages visible to screen readers. I'll show you how several small additions have a big impact and make your status messages standout for all.

## NVDA and browser compatibility ##
Testing how effectively screen readers follow the expected [ARIA live region role specification](https://www.w3.org/TR/wai-aria-1.1/#live_region_roles) and prioritise announcements.

&nbsp;        | Internet Explorer 11 | Edge | Chrome 74 | FireFox Quantum 66 
:-------------: |:-------------:| :-----:| :-----:| :-----:
`role="status"`    | NO | NO | YES* | YES* 
`role="alert"`    | NO | NO | YES | YES  
`role="log"`    | NO | NO | YES | YES 

NVDA version 2018.2.1<br>

## Mobile device compatibility ##
&nbsp;        | VoiceOver iOS |TalkBack Android
:-------------: |:-------------: |:-------------:
`role="status"`    | YES | YES
`role="alert"`    | YES | YES
`role="log"`    | YES | YES

iOS version 12.2 iPad mini 2<br>
Android version 8.0 HTC 10

## Demo pages ##
All examples have content added to the live region 5 seconds after the page has loaded.

* [status.html](https://canaxess.github.io/presentations/DDD%20By%20Night%20Melbourne/status.html)
* [alert.html](https://canaxess.github.io/presentations/DDD%20By%20Night%20Melbourne/alert.html)
* [log.html](https://canaxess.github.io/presentations/DDD%20By%20Night%20Melbourne/log.html)

### Note ###

Content added to live region using `document.getElementById` and `.innerText` property triggered 5 seconds after page load. See [ARIA alert support](https://developer.paciellogroup.com/blog/2017/04/aria-alert-support/) for details about the way elements are added _may_ affect the screen reader announcing content.<p>
*reading of page text stops at the word 'several'

## Useful links
* [Accessible Rich Internet Applications (WAI-ARIA) 1.1 / live region roles](https://www.w3.org/TR/wai-aria-1.1/#live_region_roles)
* [NVDA screen reader](https://www.nvaccess.org/download/) version 2019.1.1
