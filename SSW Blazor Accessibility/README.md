# Accessify Your Blazor Apps

Blazor is no different than any other framework for accessibility. It doesn’t make any web application any more or less accessible, but you still need to actively put in accessibility support.

## Reusable Components
Creating reusable components makes the design consistently repeatable. A component can be created which has a range of parameters that can be set when developing, developers aren’t having to directly code the attributes they're simply setting what type of message to display.

Taking the responsibility away from the developer to have to worry and think about these sorts of things means a stronger likelihood accessibility is being maintained and is being implemented consistently.

## Managing Focus
Managing focus is crucial to making it easier for keyboard users to navigate around the screen. When modals, or new screens are loaded and the focus isn't programmatically managed and moved to the new content, a keyboard user will have to repeatedly advance the Tab position on to this new content. 

Programmatically managing the focus means when new content is loaded and we want the user to interact with it, the focus is manually moved. The user does not have to worry about tabbing to the new content as its already there, and it has reduced a potential keyboard accessibility navigation problem.

Javascript is called from within a Razor component from the `OnAfterRenderAsync` lifecycle method to focus any named element on the page using `getElementById()`.
