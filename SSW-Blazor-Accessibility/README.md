# Accessify Your Blazor Apps

Blazor is no different than any other framework for accessibility. It doesn’t make any web application any more or less accessible, but you still need to actively put in accessibility support.

## In This Repository
**AudibleAlert.razor** demonstrates how to use components to display consistent and accessible alerts. It uses the WCAG 2.1 alert roles for predefined alerts or use the aria attributes `aria-atomic` and `aria-relevant` for more granular control.

**How to call component**
```html
<AudibleAlert IsCustomLiveRegion="false" MessageType="alert"/> //alert, status, log
```

**Granular control**
```html
<AudibleAlert IsCustomLiveRegion="true" Assertivness="assertive" AnnounceWhole="false" WhatChanges="additions"/>
```

**HeadingFocus.razor** demonstrates how to focus on page elements using Javascript Interop. The Javascript function is called after the component has rendered.
```csharp
protected override async Task OnAfterRenderAsync(bool firstRender)
{
  await jsRuntime.InvokeAsync<object>("IDfocus", headingID);
}
```

**script.js** focuses onto a named page element using `getElementById` with a parameter passed.<br>
**site.css** optional CSS effect to identify when heading element is in focus.


## Brief Recap on Accessibility
Web Content Accessibility Guidelines (WCAG) is an accepted best practice way of making web content accessible. It's technology agnostic but ultimately presents solutions in HTML, CSS and Javascript. 

WCAG 2.1 has 3 levels of conformance (A, AA, AAA) which correspond to the degree of technical difficulty and user support.

* [Beyonce's Parkwood Entertainment Sued Over Website Accessibility](https://www.hollywoodreporter.com/thr-esq/beyonces-parkwood-entertainment-sued-1172909)
* [Supreme Court hands victory to blind man who sued Domino’s over site accessibility](https://www.cnbc.com/2019/10/07/dominos-supreme-court.html)
* [Coles to make online shopping site more accessible following disability discrimination case](https://www.smh.com.au/national/coles-to-make-online-shopping-site-more-accessible-following-disability-discrimination-case-20150218-13ig1g.html)

## Frankenstein's Monster, The `DIV` Button
We can go ahead and make custom controls but the effort to make them accessible and practically usable is significantly greater and much more effort. 

By sticking with regular HTML controls and components  apps are already more accessible than if building a custom control. That isn't to say custom controls should be avoided, but its understanding that to make those controls accessible is much more challenging.

**Things to consider when creating custom controls:**
* Make the control keyboard focusable, use `tabindex="-1"`
* Make it behave like a native element i.e. for a button use `role="button"`
* Provide a text label (if one doesn’t exist), use `aria-label="<button text>`
* Add mouse **AND** keyboard event handlers
* Add CSS focus effects

## The Difficulty With 3rd Party Control Suites
The accessibility statements vendors provide are often so narrowly defined and superficial that the accessibility support provided is extremely limited and, in some instances, non-existent.

**You cant rely on the vendor accessibility conformance claim. If you do use custom controls:**
* [Independently verify it has accessibility support](https://www.canaxess.com.au/services/audit/)
* Request information if the controls have been tested with a screen reader
* Request information if the controls have been tested with a user wtih disabilities

## Alerting the user audibly
Provide audible hints through an accessibility technique called a live region used to indicate the status of the change audibly to the screen reader. When content is added to it, the new content is communicated through to the screen reader which announces it so it’s a very convenient way to alert the user that something has changed.

### Use the WCAG 2.1 live region roles for defined message types
Role | Urgency | What is announced?
--- | --- | ---
`role="log"` | Polite | New
`role="status"` | Polite | Old & New
`role="alert"` | Assertive | New

## Reusable Components
Creating reusable components makes the design consistently repeatable. A component can be created which has a range of parameters that can be set when developing, developers aren’t having to directly code the attributes they're simply setting what type of message to display.

Taking the responsibility away from the developer to have to worry and think about these sorts of things means a stronger likelihood accessibility is being maintained and is being implemented consistently.

## Managing Focus
Managing focus is crucial to making it easier for keyboard users to navigate around the screen. When modals, or new screens are loaded and the focus isn't programmatically managed and moved to the new content, a keyboard user will have to repeatedly advance the Tab position on to this new content. 

Programmatically managing the focus means when new content is loaded and we want the user to interact with it, the focus is manually moved. The user does not have to worry about tabbing to the new content as its already there, and it has reduced a potential keyboard accessibility navigation problem.

**HeadingFocus.razor**

```csharp
protected override async Task OnAfterRenderAsync(bool firstRender)
{
  await jsRuntime.InvokeAsync<object>("IDfocus", headingID);
}
```

Javascript is called from within a Razor component from the `OnAfterRenderAsync` lifecycle method to focus any named element on the page using `getElementById()`.

**script.js**

```javascript
function IDFocus(varID)
{
	document.getElementById(varID).focus();
}
````
By applying this technique to all components which trigger the display of new UI content means the screen focus is always in synch with the content

---
In need of accessibility support? [reach out to us](https://www.canaxess.com.au/contact):wave:
**CANAXESS** :heart: A11y
