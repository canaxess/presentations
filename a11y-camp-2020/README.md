# Not another checklist! – A testing methodology which explains the what and how of manual accessibility testing
Accessibility testing is hard. How do you upskill team members to understand WCAG 2.1? How do you explain testing with screen readers? This is a challenge I faced with new team members and requests to standardise the testing. 

I created a checklist which made accessibility testing consistent and removed different interpretations and inaccurate assumptions. When a team's accessibility maturity is low creating a checklist with this methodology results in a testing process anyone can understand.

**The testing methodology is comprised of three separate checklists:**
1. A WCAG 2.1 level AA testing checklist
2. A compatibility testing checklist
3. A workflow testing checklist

---

## 1. Creating a WCAG 2.1 AA testing checklist
**Scope**: Individual Pages

### Instructions
For all 50 WCAG 2.1 AA success criterion look at the sufficient techniques and decide if one or more tests can be identified?

**For example:**

[Success Criterion 1.3.1](https://www.w3.org/WAI/WCAG21/quickref/#info-and-relationships) describes making sure any information and relationship conveyed through presentation is programmatically determinable. Look through the list of sufficient techniques and create a test around the technique.

| Sufficient technique | Possible test to apply |
|:----------------------|:---------------|
| H97: Grouping related links using the nav element | related links are grouped in `<nav>` element |
| H48: Using ol, ul and dl for lists or groups of links | groups of related links use `<ol>`, `<ul>`, `<dl>` |

### Outcome
Applying this technique For [Success Criterion 1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG21/quickref/#info-and-relationships) means at least 13 individual tests can be identified. Your results may be different and may include fewer or greater tests.

Working out your own tests helps you begin to understand what types of elements can be tested in a consistent way.
| Category  | Success Criterion              | Individal Test                                                                               | Page1 URL | 
|:-----------|:--------------------------------|:------------------------------------------------------------------------------------|:------------------:|
| Structure | 1.3.1 Info and Relationships | headings are used to structure content                                           | YES | 
| Structure | 1.3.1 Info and Relationships   | headings are correctly applied                                                     | NO |
| Structure | 1.3.1 Info and Relationships   | tables are used for tabular data                                                 | YES |
| Structure | 1.3.1 Info and Relationships   | tables have the `summary` attribute                                                | YES |
| Structure | 1.3.1 Info and Relationships   | tables use `<th>` elements                                                           | YES |
| Links     | 1.3.1 Info and Relationships   | related links are grouped in `<nav>` element                                       | YES |
| Forms     | 1.3.1 Info and Relationships   | labels programmatically associated to input control                              | YES |
| Forms     | 1.3.1 Info and Relationships   | visually related control are grouped together in a fieldset element              | YES  |
| Forms     | 1.3.1 Info and Relationships   | all fieldset elements have legend element                                        | YES  |
| Forms     | 1.3.1 Info and Relationships   | all radio button and checkbox controls are fully grouped inside fieldset element | YES  |
| Structure | 1.3.1 Info and Relationships   | some HTML5 landmarks are used                                                      | YES  |
| Structure | 1.3.1 Info and Relationships   | all HTML5 landmarks have a programmatic name                                     | YES  |
| Links     | 1.3.1 Info and Relationships   | groups of related links use `<ol>`, `<ul>`, `<dl>`                                     | YES  |

### Example
If a page has the following heading structure:
```html
<h2>Heading 2</h2>
<h4>Heading 4</h4>
<h1>Heading 1</h1>
<h5>Heading 5</h5>
```
* It will **pass** the test 'headings are used to structure content'
* It will **fail** the test 'headings are correctly applied'
* Be recorded as a **fail** against Success Criterion 1.3.1 Info and Relationships 

Whilst headings are applied, they haven't been applied _correctly_. As the two tests reside under the one success criterion it's recorded as a failure overall.

### How to test
Looking through the HTML source code is slow. Applying Javascript/JQuery bookmarklets make it quicker to identify only the sections you need to test.

## 2. Creating a compatibility testing checklist
**Scope**: All representative pages

These are fixed tests covering all representative pages in the site sample which determine how well the content is rendered in browser and screen reader combinations, any irregularities are recorded in each cell. Browser and screen reader combinations need to be tailored for your circumstances.

| Test                             | JAWS IE11 | JAWS Chrome | JAWS Edge | JAWS Firefox | NVDA IE11 | NVDA Chrome | NVDA Edge | NVDA Firefox |
|:----------------------------------|:-------------|:---------------|:-------------|:----------------|:-------------|:---------------|:-------------|:----------------|
| headings make sense              |             |               |             |                |             |               |             |                |
| headings properly structured     |             |               |             |                |             |               |             |                |
| links are understandable         |             |               |             |                |             |               |             |                |
| form labels are understandable   |             |               |             |                |             |               |             |                |
| required form controls announced |             |               |             |                |             |               |             |                |
| lists are understandable         |             |               |             |                |             |               |             |                |
| landmarks are understandable     |             |               |             |                |             |               |             |                |
| button labels are understandable |             |               |             |                |             |               |             |                |
| errors are announced             |             |               |             |                |             |               |             |                |

Each cell records the result of the test **YES**, **NO**, **N/A**. If using Excel the New Comment option on each cell allows a descriptive explanation of the nature of the problem.

## 3. Creating a workflow test
**Scope**: One workflow which may include several pages

This test uses one browser and one screen reader and tests the default path or workflow a user may take through the digital service. Results are recorded via bullet points along with any unusual behaviour, and is based **solely on the audible cues from the screen reader**.

### Instructions
1. Identify a common workflow or path a user may take through the service
2. Use a browser and screen reader combination which are compatible
3. Avoid looking at the screen
4. Record each step and document behaviour

**For example:**

**Test:** Sort all records ascendingly by surname and identify the first record

**Steps**
1. Navigate to table
2. Navigate to 'surname' column
3. Activate sort control and sort ascendingly
4. Identify the first record in the table

**Result**
* Have identified 'surname' column
* Can activate sort control 
* Sort direction applied isn't announced
* Insufficient guidance with how to re-sort column

## Resources
### Twitter conversations
These were conversations I posted to Twitter which resulted in great feedback (click through to read) which helped formulate my approach towards compatibility testing.

[**I asked on August 27th 2020**](https://twitter.com/MrRossMullen/status/1298901256337895424?s=20)
> It’s become almost subconscious how I accessibility test web sites. But it’s surprisingly difficult to write down or explain, #a11y friends how do you write test cases for screen reader testing for someone new to accessibility?

[**I asked on August 18th 2020**](https://twitter.com/MrRossMullen/status/1295548417024733185?s=20)
> I've read too many articles that describe how to test with a screen reader but not *what* to test. The advice of many articles of "have a play around" is not consistent and can't be documented. This is really good from @WeAreSigma describing the what

## Articles
[Testing Accessibility on a Mobile Device – Part 2: Screen reader testing](https://www.designedbysigma.com/news-and-thoughts/testing-accessibility-on-a-mobile-device-part-2-screen-reader-testing/)
