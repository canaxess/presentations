# Transcript
Accessibility testing is hard. It involves an understanding of the web content accessibility guidelines, frontend development techniques, sometimes backend development, browser quirks and how screen readers and other assistive technology render the content and display it.

Trying to systemise and make testing a consistent process is challenging. A new colleague joined the team and management were keen to provide accessibility testing as a service offering and ultimately increase the capacity of the testing services the team offered. 

Other teams would approach us to request an accessibility audit and this would then guide their development as they'd know what to address, what's important and what's a nice to have feature.
But even though I knew what we wanted to offer, trying to allocate blocks of time against this as a resource proved challenging. 

All of my knowledge was acquired over many years, but when asked about how long it would take, I would reply about 3-4 weeks, hardly a definitive figure.

I also appreciated accessibility knowledge can't be just retained by one person. To increase testing capacity of the team more people need to be brought in. 

But as accessibility testing is a very niche skillset, a way had to be found that allowed all people with all levels of technical ability to perform an accessibility review in a consistent way. 
The difficulty is, it's such a diverse skillset that the knowledge resides in pockets in organisations, and often individual people. 

Which mean whilst there are accessibility professionals, that knowledge isn't spread around and accessibility maturity within a large organisation remains low.
And the challenge with WCAG is that its often subjective and can be left up to the whims of the individual accessibility specialist performing the test on that day, one person may identify a pass whilst another identifies a failure. 

The whole testing process didn’t feel consistent and I wanted to reduce that level of variance. 

At a minimum we had to measure against WCAG 2.1 guidelines, and I identified all the relevant double A success criteria and these are mandatory tests which we must perform. 
But knowing what to test and how to test are two different things. 

For example, success criteria 1.4.5 Images of Text If the technologies being used can achieve the visual presentation, text is used to convey information rather than images of text except for the following: 

* Customizable: The image of text can be visually customized to the user's requirements;
* Essential: A particular presentation of text is essential to the information being conveyed.

Note 1: Logotypes (text that is part of a logo or brand name) are considered essential.

The understanding success criteria does a great job of trying to unpick and includes test to apply but it's tricky to understand and its very dense. 

Ultimately the success criterion means don’t use images to convey textual information use text unless the image is required or the image can be customisable.
 
Rather than grappling with that description this was distilled down into one test no images of text exist unless necessary. Its deliberately made this success criteria easier to test as it removed a lot of redundant information. 

The information ignored is not irrelevant but as our accessibility maturity was very low, and time constraints existed, a quick way had to be found of establishing a baseline of testing.

I began applying this technique to other success criteria. For 1.3.1 Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text. 

This again can be open to interpretation, what is information, what is structure what is a visually conveyed relationship?

The sufficient techniques gave hints as to what sort of things to test. For example, Technique H42: Using h1-h6 to identify headings is pretty self-explanatory but then headings on a page can be applied out of sequence, or heading levels are skipped. 

So, whilst a single test of headings are logical and sequential could exist, I wanted to make it as easy as possible to test against – logical and sequential is still very subjective and ideally have one test answering one question. 

So that one sufficient technique became two separate tests, headings are used to structure content and headings are correctly applied. 

If a page had added headings to a document in an irregular way, it may pass the first test - headings are used to structure content as yes headings are used albeit incorrectly, but then fail on the second test headings are correctly applied. 

As these two tests are both within success criterion 1.3.1, then that content has failed. 

This approach was applied to all 50 WCAG 2.1 AA success criteria which became 96 individual tests which are applied to every page, grouped under broad categories. 

Some success criteria had multiple tests whilst others had single tests catering for every type of content on the webpage. 

These tests are individual actions with a definitive outcome, yes it passes, no it fails or not applicable. Because it’s a single outcome, it becomes much clearer to test manually and faster to execute.

This meant the whole process of accessibility testing could be sped up. 

It’s a repeatable consistent process, ultimately a site tested today and one tested in a years' time have exactly the same tests applied in exactly the same way. 

Its systemised, and its consistent. 

I also found it was a really good way to begin identifying how long an accessibility review would actually take. I assumed each test would conservatively take 2 minutes to run. 

The WCAG 2.1 success criteria is broken down in 96 individual tests, so it becomes 96 tests multiplied by 2minutes which is 192 minutes or 3.2 hours per page. 

And then multiply that figure by the total number of pages, 10 pages multiplied by 3.2 gives 32 hours of testing for 10 pages. A reasonably accurate figure for planning activities.

But there was still a niggling doubt. WCAG 2.1 AA criteria had been tested in its entirety but WCAG by itself is not necessarily an effective measure of a site's accessibility. 

After all a site can be technically conformant and practically unusable. I then looked at adding screen reader compatibility tests between versions of browsers. 

Some pages may render well in browsers, and some pages may have gaps with their support for accessibility and HTML techniques. But which items to actually test? 

in an ideal world it would be every HTML element in every browser against every screen reader. But that could balloon out easily, and with limited resources it's difficult to make a case for more time to test because ultimately the testing could never end. 

There could always be a further test to perform, a line had to be drawn somewhere.

The more I searched for approaches the more I found I didn’t like the often quoted advice on blogs and articles about screen reader testing. 

These articles go into detail telling how to test and which commands to use but not what to test, or worse still encouraging the user to "get a feel" for navigating with a screen reader, when time is limited and the approach is needing to be consistent and systemised that advice isn't that helpful. 

It was good advice, but it was difficult to encourage new colleagues to get a feel for screen reader testing when it wasn’t really clear what to identify.

After a lot of time searching, and a few questions posted to Twitter with some great suggestions I found a really good article by Harley Callaghan a test analyst at UK design consultancy Sigma which when combined with the Twitter responses helped me formulate the what of screen reader testing.

His article describes ensuring headings are coded as headings, does the screen reader read out form labels and required form fields, is an alert read out if the form is in error. 

Whilst its primarily mobile focused this for me was the "what" for screen reader testing, it may appear obvious but it was only until I was requested to systemise the test that I realised I didn’t really know how to convey testing with a screen reader in a consistent way to new testers.

I added an additional 9 tests. These could be thought of as zooming out of the WCAG 2.1 tests and were now testing the compatibility between browsers and screen readers. 

Our standard software combinations used Firefox, Chrome and Edge Legacy and included optional support for IE11. 

These were teamed with the screen readers NVDA and JAWS with a matrix detailing support, if it passes or if there were gaps in the support. 

For example, do headings make sense, that is are the headings clear when navigated with a screen reader. A heading with several div and span elements can often result in clipped text in some browser and screen reader combinations. 

I'm now not testing WCAG criteria but how well portions of the page content are rendered in browser and screen reader combinations. 

These comprised 9 tests across 6 different browsers and screen reader combinations so all up a total of 54 tests. 

These tests are reduced in scope and now focus on compatibility of key sections of content, so I called them compatibility tests.

I was feeling pretty good about what had been covered. All of WCAG was covered combined with compatibility tests for popular browsers. 

But a discussion of real world testing was introduced, for all WCAG testing and compatibility testing if a user isn't able to navigate our sites It matters little if I say but we've tested against WCAG, I needed to test an average path through the application a user could take. 

Could a user navigate a workflow solely listening to the audible prompts from the screen reader? I wasn't testing all workflows, just the default path and the default actions. 

And this test is on one browser with one screen reader. 

It’s a way to determine if a theoretical user can navigate through the application and complete the workflow, the workflow may be filter and sort records or login basically anything other than simple navigation. 

When I had assembled all of the testing, it began looking like a pyramid showing how I allocate testing activities and what to place emphasis on. 

WCAG represents the baseline of testing, followed by compatibility testing and lastly workflow testing. 

We now have a methodology which has been applied to several web applications and the results are promising.
 
We're able to quickly and efficiently test all WCAG 2.1 AA success criteria using simple statements which have a yes, no, n/a as a possible answer. 

But its not perfect, more complicated WCAG 2.1 success are very challenging to test against. 

This testing methodology doesn’t factor in the nuances of accessibility testing, accessibility testing is never clear cut with definitive answers. 

But for us where our corporate accessibility maturity was low this represented a significant improvement where we could test with fairly good certainty. 

Its not perfect, but its good enough and we didn’t want to let perfection be the enemy of good.

It was tempting to try and find a nice solution for accessibility testing, but where testing maturity is low the biggest challenge for us was understanding how to increase that testing capacity and capability because we didn’t want to rely on external vendors. 

Building that capability internally means there are more accessibility testers able to perform testing at a defined level.

Accessibility testing isn't exciting, its hard work and very repetitive and unless the process is documented can become inconsistent. 

Applying this methodology can reduce the level of variance in your testing as it did with ours. 

Where there is a requirement to ensure a consistent process is applied this can help towards that goal.

I've created a readme which leads you through creating your own checklist and a downloadable Excel starter spreadsheet along with all of the feedback from Twitter which helped me formulate this methodology. 

Check out [github.com/canaxess/presentations](https://github.com/canaxess/presentations) and navigate to **a11y-hyphen-camp-hyphen-2020**. 

Reach out to me on Twitter [@MrRossMullen](https://twitter.com/MrRossMullen), email [hello@canaxess.com.au](mailto:hello@canaxess.com.au) or visit [www.canaxess.com.au](https://www.canaxess.com.au/) for any digital accessibility support for your projects.
