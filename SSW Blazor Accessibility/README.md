# Accessify Your Blazor Apps

Blazor is no different than any other framework for accessibility. It doesn’t make any web application any more or less accessible, but you still need to actively put in accessibility support.

## Frankenstein's Monster, The `DIV` Button
We can go ahead and make custom controls but the effort to make them accessible and practically usable is significantly greater and much more effort. 

By sticking with regular HTML controls and components  apps are already more accessible than if building a custom control. That isn't to say custom controls should be avoided, but its understanding that to make those controls accessible is much more challenging.

**Things to consider when creating custom controls:**
* Make the control keyboard focusable, use `tabindex="-1"
* Make it function like a button, use `role="button"`
* Provide a text label (if one doesn’t exist), use `aria-label="<button text>`
* Add mouse **AND** keyboard event handlers
* Add CSS focus effects

## The difficulty with 3rd party control suites
The accessibility statements vendors provide are often so narrowly defined and superficial that the accessibility support provided is extremely limited and, in some instances, non-existent.

**You cant rely on the vendor accessibility confromance claim. If you do use custom controls:**
* [Independently verify its has accessibility support](https://www.canaxess.com.au/services/audit/)
* Request information if the controls have been tested with a screen reader
* Request information if the controls have been tested with a user wtih disabilities

## Reusable Components
Creating reusable components makes the design consistently repeatable. A component can be created which has a range of parameters that can be set when developing, developers aren’t having to directly code the attributes they're simply setting what type of message to display.

Taking the responsibility away from the developer to have to worry and think about these sorts of things means a stronger likelihood accessibility is being maintained and is being implemented consistently.

## Managing Focus
Managing focus is crucial to making it easier for keyboard users to navigate around the screen. When modals, or new screens are loaded and the focus isn't programmatically managed and moved to the new content, a keyboard user will have to repeatedly advance the Tab position on to this new content. 

Programmatically managing the focus means when new content is loaded and we want the user to interact with it, the focus is manually moved. The user does not have to worry about tabbing to the new content as its already there, and it has reduced a potential keyboard accessibility navigation problem.

Javascript is called from within a Razor component from the `OnAfterRenderAsync` lifecycle method to focus any named element on the page using `getElementById()`.
