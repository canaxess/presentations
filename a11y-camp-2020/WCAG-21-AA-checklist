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
