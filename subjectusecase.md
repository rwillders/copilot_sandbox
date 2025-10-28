Initiative Name: Capability to manage inputs to utilize Data Resources Default Values

Epic Name: Ability to Manage Simple Input Fields to Utilize Data Resource Default Values

TEMPLATES_008150 Ability to Manage Simple Input Fields to Utilize Data Resource Default Values 

Description: Templates can have multiple Input Fields associated with them that allow a user to provide values to populate a Letter Instance. These Input Fields come in many different types, each with their own different configuration settings. In the Template Manager, the Changeset Editor requires the ability to assign and manage default values from an associated Data Resource to populate Simple Input Fields. This use case covers the management of the default values from selected Data Resources for Simple Input Fields: Text, Number, Date, Time, and Boolean values.

Line(s) of Business: All Lines of Business 

Primary Actor(s): Changeset Editor

Goal: Users need to be able to manage Simple Input Fields within a Template Version to utilize default values from a Data Resource, so that Inputs are automatically populated for Letter Editors reducing risks of typing errors when Letters are generated.
Secondary Actor: N/A

List of Abilities:

1. The user is able to view a list of available Data Resources within their LoB that can be used to populate Simple Input Feilds default values on the Template Version.
2. The user is able to assign the default value of a Simple Input Field to use the value provided by a Data Resource Field.
3. The user is able to edit an assigned Data Resource default value assigned to a Simple Input Fields on a Template Version.
4. The user is able to remove an assigned Data Resource default value assigned to a Simple Input Field on a Template Version.

Preconditions:
1. A Simple Input Field is configured on the selected Template the Changeset Manager is assigning a default value to.
2. A Data Resource Field that matches the data type contained in a Simple Input Field has been made available to the Line of Business (LoB).

Post Conditions:
1. None

Main Flow/Assignment of Data Resource Default Values for a Simple Input Field:  
1. Template Simple Input Field has been configured with the selected Data Resource default value that is associated with a Template in the ‘Draft’ Status.
2. When the Letter Instance is generated, the default value data is pulled from the Data Resource and populates in the letter.

Alternative Flow/ Editing Data Resource Default Values for a Simple Input Field:  
1. Data Resource default value on the Simple Input Field has been updated on the Template.

Alternative Flow2/ Removing Data Resource Default Values for a Simple Input Field:
1. Data Resource default value has been removed from selected Simple Input Fields on the Template.


Main Flow - Assignment of Data Resource Default Values for a Simple Input Field:  
1. The user is able to select a Template Version in the ‘Draft’ Status that contains Simple Input Fields.
2. The user is able to assign a default value when selecting a Simple Input Field associated within a given Template Version.
   a. The user is required to select the following for each Simple Input Field from a list of available Data Resources:
      1). Data Resource
      2). Data Resource Field of the same input type

Alternate Flow - Editing of Data Resource Default Values for a Simple Input Field:  
1. The user is able to select a Template Version in the ‘Draft’ Status that contains Simple Input Fields with configured default values.
2. The user is able to select an existing Simple Input Field with an assigned default value within a given Template Version.
   a. The user is able to change the default value by selecting the following for the given Simple Input Field of available Data Resources:
      1). Data Resource
      2). Data Resource Field of the same input type

Alternative Flow - Removing Data Resource Default Values for a Simple Input Field:    
1. The user is able to select a Template Version in the ‘Draft’ Status that contains Simple Input Fields with configured default values.
2. The user is able to select an existing Simple Input Field with an assigned Default Value within a given Template Version.
   a. The user is able to remove existing association with a Data Resource Field default value.
      1). Input Field returns to blank without default value for manual entering of data.

Notes:
1. The user is required to select a Default Value Type that matches the same type of the chosen Simple Input Field.
