Initiative Name: Capability to Utilize Calculations in the Template Manager

Epic Name: Ability to use Calculator Functions while Configuring Rules for Conditional Logic

TEMPLATES_003000 User manages Conditional Logic in the Content of a Template

Description: Letters will often need to vary their content based on values either provided by the letter creator or related to the work object with which the Letter Instance is associated. To allow this dynamic letter content, the user who creates Templates needs the ability to define the conditions under which the letter content will change and to provide the content that will display under those various conditions. This use case is meant to inform what the user’s abilities are regarding this conditional content.

Line(s) of Business: All Lines of Businesses

Table/List of Actors/Stakeholders:
    Changeset Editor – Will be able to provide content to display under certain conditions and define the conditions for that content’s use.
    
List of Abilities for each Actor/Actor Actions:

While editing a template:
- The user is able to insert a placeholder into the content of the Template that holds a number of comparative equations or statements to be evaluated (called rules) and content to be populated into documents created from the Template when the combination of rules evaluates as “True”.
- The user is able to add a conditional placeholder as either an ‘inline’ conditional, which can exist within a string of text, or a ‘block’ conditional, which exists as its own paragraph block.
- When there is more than one rule associated with a conditional placeholder, the user is required to create groupings for all rules that can include rules and/or other groupings of rules and apply one of the following categories to each grouping:
   An AND operation, where if all grouped items evaluate as “True”, the overall grouping evaluates as “True”, else the grouping evaluates as “False”.
   An OR operation, where if at least one grouped item evaluates as “True”, the overall grouping evaluates as “True”, else the grouping evaluates as “False”.
- The user is able to select from all fields (both Input Field and Data Resource Fields) of the following types to be compared in a rule:
Text
Number
Date
Boolean
Option Select
- The user is able to select a calculated value to be compared in a rule.
    When selected, the user will be able to provide any equation available using existing calculator functionality, including using any number fields assigned to the template.
- The comparative functions available to a rule will vary by type of value compared as listed:
Text fields:
  Equals
  Does Not Equal
  Contains
  Does Not Contain
  Starts With
  Ends With
  Is Empty
  Is Not Empty
Number Fields and Date Fields:
  Equals
  Does Not Equal
  Less Than
  Less Than or Equal To
  Greater Than
  Greater Than or Equal To
  Is Null
  Is Not Null
Boolean Fields:
  Is True
  Is False
Option Select:
  Equals
  Does Not Equal
  Contains
  Does Not Contain
  Is Null
  Is Not Null
Calculation:
  Equals
  Does Not Equal
  Less Than
  Less Than or Equal To
  Greater Than
  Greater Than or Equal To

- When the rule requires a value to be compared against, the user is provided a method to enter a value of the same type as the field associated with the rule.

- The user is provided a method to enter content (including further conditional fields) that will populate a letter created from the current Template if the overall conditional evaluates as “True”.

- The user is provided a method to indicate if there is conditional content to be displayed if the overall conditional evaluates as “False”.
    If indicated, the user is provided a method to enter content (including further conditional fields) that will populate a letter created from the current Template if the overall conditional evaluates as “False”.

- If a conditional placeholder is placed within the content portion of a List Builder, Input Group, or (Data Resource Group/Field Group) placeholder, the conditional rules will be able to select the fields contained in that List Builder, Input Group, or (Data Resource Group/Field Group) to have those values be compared for each occurrence of that Group.

- If a conditional placeholder is placed not within the content portion of a List Builder, Input Group, or (Data Resource Group/Field Group) placeholder, The user is able to select the instanced fields held within a List Builder, Input Group, or (Data Resource Group/Field Group) as fields to be compared in a rule. If a conditional ruleset contains an instanced field, that ruleset will be evaluated for each occurrence within that group, and if the ruleset evaluates as true for any occurrence, then the conditional content will be displayed.
    A conditional ruleset may only evaluate instanced fields from a single Group Field at a time. If an instanced field is selected to be evaluated, instanced fields from other Group Fields will no longer be available to that ruleset.

Preconditions:
User is editing a template.

Post Conditions:
The Template is designed to display certain content only when given conditions are met.


TEMPLATES_003450 User Manages the Style of Content within a template

Description: For content of a template, users are able to specify the style of content to be applied to the rendered PDF of a Letter Instance. Styling the content of a letter can be done multiple ways and is useful for ensuring clarity, readability, and consistency when creating letters.

Line(s) of Business: All Lines of Businesses

Primary Actor(s):
  Changeset Editor

Goal: The user needs the ability to specify the style of content in the rendered PDF of a Letter Instance. 

List of Abilities:

Changeset editors are able to:

Define the style of the following content in a ‘Draft’ template:

Static Text

Input Placeholders

Data Resource Field Placeholders

Calculation Result Placeholders

Define the paragraph heading style of the content.

Define the font size of the content.

Define the font type of the content from a list of pre-defined fonts.

Define the style of text of the content (Bold, Italicize, Underline). 

Preconditions:

There is a Template to be edited in ‘Draft’ Status. 
Postconditions: 

The style in a Template will be reflected in the rendered Letter Instance. 
