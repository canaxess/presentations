# Not another checklist! – A testing methodology which explains the what and how of manual accessibility testing
Accessibility testing is hard. How do you upskill team members to understand WCAG 2.1? How do you explain testing with screen readers? This is a challenge I faced with new team members and requests to standardise the testing. 

I created a checklist which made accessibility testing consistent and removed different interpretations and inaccurate assumptions. When a team's accessibility maturity is low creating a checklist with this methodology results in a testing process anyone can understand.

## 1. Creating a WCAG 2.1 AA testing checklist
### Instructions
For each WCAG 2.1 AA success criterion look at the sufficient techniques. Are one or more test identified?

**For example:**

Success criterion 1.3.1 describes making sure any information and relationship conveyed through presentation is programmatically determinable. Look through the list of sufficient techniques and create a test around the technique.

| Sufficient technique | Test to apply |
|:----------------------|:---------------|
| H97: Grouping related links using the nav element | related links are grouped in &lt;nav&gt; element |
| H48: Using ol, ul and dl for lists or groups of links | groups of related links use &lt;ol&gt;, &lt;ul&gt;, &lt;dl&gt; |

### Test outcome
Applying this technique For success criterion 1.3.1 Info and Relationships means 13 individual tests can be identified. Your results may be different and may include fewer or greater tests.

Working out your own tests helps you begin to understand what can be tested in a consistent way.
| Category  | Success Criterion              | Individal Test                                                                               | 
|:-----------|:--------------------------------|:------------------------------------------------------------------------------------|
| Structure | 1.3.1 Info and Relationships | headings are used to structure content                                           |
| Structure | 1.3.1 Info and Relationships   | headings are correctly applied                                                     |
| Structure | 1.3.1 Info and Relationships   | tables are used for tabular data                                                 |
| Structure | 1.3.1 Info and Relationships   | tables have the summary attribute                                                |
| Structure | 1.3.1 Info and Relationships   | tables use &lt;th&gt; elements                                                           |
| Links     | 1.3.1 Info and Relationships   | related links are grouped in &lt;nav&gt; element                                       |
| Forms     | 1.3.1 Info and Relationships   | labels programmatically associated to input control                              |
| Forms     | 1.3.1 Info and Relationships   | visually related control are grouped together in a fieldset element              |
| Forms     | 1.3.1 Info and Relationships   | all fieldset elements have legend element                                        |
| Forms     | 1.3.1 Info and Relationships   | all radio button and checkbox controls are fully grouped inside fieldset element |
| Structure | 1.3.1 Info and Relationships   | some HTML5 landmarks are used                                                      |
| Structure | 1.3.1 Info and Relationships   | all HTML5 landmarks have a programmatic name                                     |
| Links     | 1.3.1 Info and Relationships   | groups of related links use &lt;ol&gt;, &lt;ul&gt;, &lt;dl&gt;                                     |

## 2. Creating a screen reader testing checklist
### Twitter conversations
These were conversations I posted to Twitter which resulted in great feedback (click through to read) which helped formulate my approach towards screen reader testing.

[**I asked on August 27th 2020**](https://twitter.com/MrRossMullen/status/1298901256337895424?s=20)
> It’s become almost subconscious how I accessibility test web sites. But it’s surprisingly difficult to write down or explain, #a11y friends how do you write test cases for screen reader testing for someone new to accessibility?

[**I asked on August 18th 2020**](https://twitter.com/MrRossMullen/status/1295548417024733185?s=20)
> I've read too many articles that describe how to test with a screen reader but not *what* to test. The advice of many articles of "have a play around" is not consistent and can't be documented. This is really good from @WeAreSigma describing the what
