Epic: Ability to Manage Simple Input Fields to Utilize Data Resource Default Values (Templates_008150)
Matches proposed Epic Name: Ability to Manage Simple Input Fields to Utilize Data Resource Default Values

*Value Statement*
As a Changeset Editor, I need to manage Simple Input Fields within a Template Version by assigning, editing, and removing default values from Data Resources, so that Inputs are automatically populated and manual entry for Letter Editors is reduced.

*Assumptions*
1.	A Simple Input Field is configured on the selected Template the Changeset Editor is assigning a default value to.
2.	A Data Resource Field that matches the data type contained in a Simple Input Field has been made available to the Line of Business.
3.	Scope applies to all Lines of Business.

*Acceptance Criteria*
1.	The user is able to view a list of available Data Resources within their Line of Business that can be used to populate default values for Simple Input Fields on a Template Version.
2.	The user is able to assign the default value of a Simple Input Field to use the value provided by a Data Resource Field of the same input type.
3.	The user is able to edit an assigned Data Resource default value for a Simple Input Field on a Template Version.
4.	The user is able to remove an assigned Data Resource default value from a Simple Input Field on a Template Version.
5.	When a Simple Input Field is configured with a Data Resource default value, and the Template Version is in ‘Draft’ status, the value is available to be pulled into the Letter Instance upon generation.
6.	If a Data Resource default value is updated for a Simple Input Field on a Template Version in ‘Draft’ status, the updated value is available for future Letter Instances.
7.	If a Data Resource default value is removed from a Simple Input Field on a Template Version in ‘Draft’ status, the Input Field is returned to blank for manual data entry.
8.	The user is required to select a Data Resource Field whose type matches the type of the chosen Simple Input Field.

*Notes*
1.	The purpose is to enable automation and efficiency for Letter Editors by reducing manual entry and potential for error.
2.	The default value type for Data Resource must match the type of the Simple Input Field.
3.	Assignment, editing, and removal of default values only apply to Template Versions in ‘Draft’ status.
