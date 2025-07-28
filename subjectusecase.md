Initiative Name: Capability to Style and Set Fonts within the Content of a Template Version 

Epic Names:
1. Ability to Style and Set Fonts within the Content of a Template Version

TEMPLATES_003450 User Manages the Style of Content within a template
Description: For content of a template, users are able to specify the style of content to be applied to the rendered PDF of a Letter Instance. Styling the content of a letter can be done multiple ways and is useful for ensuring clarity, readability, and consistency when creating letters.
Line(s) of Business: All Lines of Businesses
Primary Actor(s):
Changeset Editor
1.	Goal: The user needs the ability to specify the style of content in the rendered PDF of a Letter Instance. 
List of Abilities:
Changeset editors are able to:
1.	Define the style of the following content in a ‘Draft’ template:
a.	Static Text
b.	Input Placeholders
c.	Data Resource Field Placeholders
d.	Calculation Result Placeholders
2.	Define the paragraph heading style of the content.
3.	Define the font size of the content.
4.	Define the font type of the content from a list of pre-defined fonts.
5.	Define the style of text of the content (Bold, Italicize, Underline). 
Preconditions:
1.	There is a Template to be edited in ‘Draft’ Status. 
Postconditions: 
1.	The style in a Template will be reflected in the rendered Letter Instance. 
Main Flow: Set the Settings, Present Content
1.	The user provides the settings for the style of the content to be added to the template.
2.	The user provides content that uses the provided style settings. 
Alternate Flow: Present Content, Set the Settings 
1.	The user selects existing content and updates the style setting for that content. 
Notes:
1.	The main flow captures the user specifying the style they are going to use before the content is populated vs the alternate flow captures the user’s ability to style existing content to something other than what it’s currently styled as.
