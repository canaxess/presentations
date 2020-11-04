# Not another checklist! – A testing methodology which explains the what and how of manual accessibility testing
Accessibility testing is hard. How do you upskill team members to understand WCAG 2.1? How do you explain testing with screen readers? This is a challenge I faced with new team members and requests to standardise the testing. 

I created a checklist which made accessibility testing consistent and removed different interpretations and inaccurate assumptions. When a team's accessibility maturity is low creating a checklist with this methodology results in a testing process anyone can understand.

## WCAG 2.1 AA Checklist fragment
| Category  | Success Criterion              | Test                                                                               | 
|-----------|--------------------------------|------------------------------------------------------------------------------------|
| Structure | 1.3.1 Info and   Relationships | headings are used to structure content                                           |
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
