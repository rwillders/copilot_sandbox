Initiative Name: Capability to Manage Option Selection Group Inputs and Placeholders within Templates

Epic Names:
1. Ability to Manage Option Selection Group Inputs and Their Placeholders Within a Template

TEMPLATES_003110: User Manages Option Selection Group Inputs and their Placeholders, using Manually Provided Options, within a Template
Use Case ID: TEMPLATES_003110

Description: While building out a Template in the Template Manager, the Changeset Editor has the ability to create, modify, and retire Templates. One of the input values that can be available for the Changeset Editor to create and utilize in a Template is the Option Selection Group. This input group allows the Changeset Editor to create groups of manually provided option values for the Letter Editor to select from, that may include additional subfields. These groups can be made optional, multiselect, or both. This input group allows the Letter Editor the ability to select from multiple predefined values, designed by the Changeset Editor, while building out a Letter Instance.

Line(s) of Business: All Lines of Business 

Primary Actor(s): Changeset Editor

Goal: The goal of the Changeset Editor is to configure Option Selection Groups so that the Letter Editor has the ability to select from a group of predefined options in order to accurately reflect the information needed specifically for the Letter Instance they are working in.
Secondary Actor: N/A

List of Abilities:

The Changeset Editor is able to:

Create an Option Selection Group:
Configure the Option Selection Group:
Provide Option Selection Group with a Name.
Identify if the Option Selection Group is Optional.
Identify if the Option Selection Group is Multiselect.
Manually provide Option Group Values as choice(s) under the Option Selection Group; can be zero-to-many.
Provide each Option Group Value with a Name; the Name will be the title of the Option Group Value and will be what the Letter Editor see’s when selecting options in the Option Selection.
Add additional Subfield(s) to each Option Group Value as nested inputs that will only be exposed if the Option Group Value the subfields are tied to is selected.
Provide each Subfield with a Name, Data Type, and any additional configuration settings determined by that Data Type.
This subfield can be of any Data Type that ECM-L supports.
Add Option Selection Group Placeholder(s) as Conditional Block(s) or Inline Conditional(s) into a specified location in the Content of the Template.
Configure the Inline or Block Conditional Placeholder to evaluate each Option Group Value:
Each Option Group Value within the Option Selection Group is available as a Boolean value that is able to be evaluated in any Conditional Content rules. 
Configure the content portion of an Option Selection Group Placeholder.
The user will populate the content of an Option Selection Group Placeholder.
This content can be of any type of content that ECM-L supports.
Update the configuration of an Option Selection Group Placeholder in the Content of a Template.
Remove an Option Selection Group Placeholder from the Content of a Template.
Preconditions

The user is working in a Template that is in ‘Draft’ status.
Post Conditions

The Option Selection Group Input Placeholder(s) have been configured and updated in the Template.
Main Flow:

The user selects an Option Selection Group as a new Input field on the Template.
The user configures the Option Selection Group:
User provides the Option Selection Group with a Name.
User identifies if the Option Selection Group is Optional.
User identifies if the Option Selection Group is Multiselect.
User manually provides one or more Option Group Value(s) as option(s) for the user to select from.
User provides each Option Group Value with a Name.
User adds additional Subfield(s) to an Option Group Value:
User provides each Subfield with a Name, Data Type, and any additional configuration settings determined by that Data Type.
The user configures an Option Selection Group Placeholder via Conditional Block or Inline Conditional for each Option Group Value in the Option Selection Group.
The user inserts each Placeholder into a specified location in the Content of the Template.
The user populates the content of each Option Selection Group Placeholder.
The user can update the configuration of the Option Selection Group Placeholder in the Content of the Template.
If needed, the user can remove an Option Selection Group Placeholder from the Content of a Template.
The user can continue making updates and adding/removing Option Selection Group Placeholders into the Content of a Template while it is in ‘Draft’ status.

Notes:

Option Selection Group Scenario:
The user is able to select one or more options of information needed from a Veteran. Within each option selected, the user is required to enter the corresponding subfields, if there are any.
