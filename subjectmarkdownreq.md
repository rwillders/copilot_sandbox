*Value Statement*
As a user that manages Templates in Template Manager, I need the ability to define conditional logic and calculator functions within a Template Version, so that resulting letter content varies appropriately based on associated letter data.
*Assumptions*
1.	Conditional Placeholders within the content of a Template Version can hold a number of comparative equations or statements to be evaluated, referred to as Rules or a Ruleset.
2.	The scope of this epic does not cover conditional content for dynamic tables (i.e. - tables created from Group Fields).       
*Acceptance Criteria*
1. The user is able to insert a Conditional Placeholder in a Template Version in ‘draft’ Status.
    a. The user is able to add a Conditional Placeholder as an ‘inline’ conditional within a string of text.
    b.  The user is able to add a Conditional Placeholder as a ‘block’ conditional which exists as its own paragraph.
    c.  The user is able to specify the style and font for content produced by a Conditional Placeholder.
 2. When multiple Rules are associated with a Conditional Placeholder, the user is required to create Rule Groupings:
     a.  Rule Groupings can include Rules and/or other Rule Groupings.
 3. When there is more than one Rule associated with a conditional placeholder the user is required to apply one of the following operations:
      a.  AND operation, where all grouped items must evaluate as “True” for the grouping to be “True”.
      b.  OR operation, where at least one grouped item must evaluate as “True” for the grouping to be “True”.
 4. The user is able to select from all fields (both Input Fields and Data Resource Fields) of the following field types for comparison in a Rule.
       a.  Text
       b.  Number
       c.  Date
       d.  Boolean
       e.  Option Select
5. The user is able to select a calculated value to be compared in a Rule, using any available equation and number fields assigned to the Template Version.
6. The comparative functions available to a Rule vary by field type, as follows:
        a. Text fields:
            1. Equals
            2. Does Not Equal
            3. Contains
            4. Does Not Contain
            5. Starts With
            6. Ends With
            7. Is Empty
            8. Is Not Empty
        b. Number Fields and Date Fields:
            1. Equals
            2. Does Not Equal
            3. Less Than
            4. Less Than or Equal To
            5. Greater Than
            6. Greater Than or Equal To
            7. Is Null
            8. Is Not Null
        c. Boolean Fields:
            1. Is True
            2. Is False
        d. Option Select:
            1. Equals
            2. Does Not Equal
            3. Contains
            4. Does Not Contain
            5. Is Null
            6. Is Not Null
        e. Calculation:
            1. Equals
            2. Does Not Equal
            3. Less Than
            4. Less Than or Equal To
            5. Greater Than
            6. Greater Than or Equal To
7. When a Rule requires a value to be compared against, the user is provided a method to enter a value of the same field type to be used in the comparison.
8. When evaluating a Rule involving text, comparative operations will ignore differences in capitalization.
9. The user is provided a method to enter content that will populate the letter if the conditional Ruleset evaluates as “True”.
       a. The user is able to add additional Conditional Placeholders within this content held by a Conditional Placeholder.
10. The user is provided a method to indicate if there is conditional content to display if the conditional Ruleset evaluates as “False”.
        a. If indicated, the user can enter content (including additional conditional fields) when the conditional evaluates as “False”.
11. If a Conditional Placeholder is placed in the content of any of the following, the conditional Rules can select individual fields within that group.
         a. List Builder
         b. Input Group
         c. Data Resource Group
         d. Input Field Group
12. If a Conditional Placeholder is placed outside the content portion of these groups, the user is able to select individual fields from a single Group Field at a time; selecting individual fields from other Group Fields disables selection from the first.
        a. Selecting individual fields from other Group Fields disables selection from the first group.
             1). If a conditional Ruleset contains an individual field, that Ruleset will be evaluated for each occurrence within that group, and if the ruleset evaluates as true for any occurrence, then the conditional content is displayed.
             2). A conditional Ruleset may only evaluate individual fields from a single Group Field at a time. 
             3). If an individual field is selected to be evaluated, individual fields from other Group Fields will no longer be available to the Ruleset.

*Notes*
1.	Related to functionality in VBMSR-33314.
2.	Implementation suggestion:  For an Option Select field, the provided method of entry of values to be compared against can default to a string field if limiting to configured options is cumbersome to implement.
