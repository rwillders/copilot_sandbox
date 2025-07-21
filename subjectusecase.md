Initiative Name: Capability to Update Name and other Attributes on a Template

Epic Names:
1. Ability to Update Name and other Attributes on a Template

TEMPLATES_002100 User Updates Name on a Template
Use Case ID: TEMPLATES_002100

Description: This use case describes the ability of a user to modify the name associated with a Template that is in a Changeset within the ECM-L system. This functionality allows users to maintain clarity and organization among various templates, ensuring they are easily distinguishable. Updating the name might be necessary for various reasons, such as correcting typos, improving clarity, or reflecting changes in the Template's purpose.

Line(s) of Business: All Lines of Business

Primary Actor(s): Changeset Editor

Goal: The user needs to be able to update the name of an existing Template that is in a Changeset in the ‘Draft’ status, so that the Template names are easily identifiable, clear, and reflect the Template's purpose. 
Secondary Actor: N/A

List of Abilities:

Users who edit the Template are able to:

Provide a value that will update the Name property when the Template is published
Preconditions:

The user is logged into the system and has the necessary permissions to access and modify the Template that is in a ‘Draft’ status.
Post Conditions:

The specified Template's name is updated on that Template to the new value provided by the user.
The updated name is reflected in all relevant areas of the draft copy.
Main Flow/Use Case:

The user navigates to the Template manager and selects a Template that is in a 'Draft’ status.

The system displays the editable properties of the template, including the current name.

The user modifies the content of the Name field with the new desired name for the template.

The system then updates and saves the name of the Template with the new name within the draft copy of the Changeset.

Notes:

The Name property is saved immediately when modified, even while the Changeset is in ‘Draft’ status. The updated name is reflected in the draft copy of the Template within the Changeset.
Is there a list of validations for creating and editing the name of a template? Yes, all of the items below will be addressed during requirements documentation.
Such as:
Exceeds character limits
Contains invalid characters
Is a duplicate of an existing name
Should an error message be displayed if these validations are in place?

TEMPLATES_002150 User Manages Template Attributes
Use Case ID: TEMPLATES_002150

Description: For creating Templates in the Template Manager, there are two kinds of Templates to choose from: Fragment Templates and Full Templates. Fragment Templates are Templates that represent a piece of content that can be included inside of another Template. A Full Template is a Template that represents the full content of a piece of correspondence, possibly including Fragment Templates. Unlike Full Templates, Fragment Templates cannot become a Letter Instance on their own. Attributes are a set of configuration details and content needed to manage a particular type of correspondence. The purpose of this Use Case is for the user to have the ability to manage the attributes aligned to each Template.

Line(s) of Business: All Lines of Business

Primary Actor(s): Changeset Editor

The goal of the Changeset Editor is to assign and manage the respective attributes when creating Templates in the Template Manager so that the Template information is clear, accurate, and identifiable.
Secondary Actor: N/A

List of Abilities:

The Changeset Editor is able to:

Assign the Template Attribute Template Type at the creation of the Template.
View the Template Attributes Name, Template Type, Description, and Labels for any Template in ‘Draft’ status aligned to the Line of Business they are working under.
Update the Template Attribute Types Name, Description, and Labels for any Template in a Changeset aligned to the Line of Business they are working under.
Preconditions:

The Application(s) for which the user intends to manage Template Attributes must exist.
Post Conditions:

The Template Attributes are accurate, and the Template is no longer in ‘Draft’ status.
Main Flow/Use Case:

When the Template is in a Changeset:
The user can view the following Template Attributes:
Name
Template Type
Description
Labels
The user can update the following Template Attributes:
Name
Description
Labels
When the Template is outside a Changeset:
The user can view the following Template Attributes:
Name
Template Type
Description
Labels
The user can update the following Template Attributes:
Labels
Notes:

The Template Type attribute has two possible values: Full or Fragment. This is something that is identified at the creation of the Template and cannot be changed after creation.
This use case is set at the Template level, not at the Template Version level.
