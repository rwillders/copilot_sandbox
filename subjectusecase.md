Initiative Name: Capability to Manage Letter Restrictions for Full Templates

Epic Name: Ability to Manage Letter Restrictions for Full Templates

TEMPLATES_003600 User Manages Letter Restrictions for Full Templates

Use Case Name: User Manages Letter Restrictions

Use Case ID: TEMPLATES_003600

Description:
Letter Editors select, organize, and optionally create custom Field Group occurrences from Data Resources to curate the content displayed on a Letter Instance. This is accomplished through a configured Field Group Option Selection Input, which allows users to choose from system-generated Field Group entries, arrange them in sequence, and add custom entries when permitted.

To support this functionality, users who manage Templates within a Changeset must be able to define the conditional data requirements for Letter Restrictions. This use case describes the capabilities required for users to create and manage these conditional rules. 

Line(s) of Business: All Lines of Business (LoB)

Primary Actor(s): Changeset Editor
1.	Goal: Users who manage Template Versions for their Line of Business need the ability to create and manage Letter Restrictions, so that letters are inhibited from being created, duplicated or finalized under specific conditions.

Secondary Actor(s): N/A

List of Abilities:
1.	The user is able to create Letter Restrictions for a ‘Full’ Template Version that is in ‘Draft’ Status.
   a.	The user is able to create one of the following restrictions for a Template Version:
      i.	The restriction makes the letter visible to the Letter Editor, but unavailable for them to create.
         1).	The user is required to enter a message to be displayed to the Letter Editor explaining why the Letter is not available to be created.
      ii.	The restriction prevents the letter from being visible to the Letter user for creation entirely.
   b.	The user is able to specify conditional logic under which a Letter Restriction will apply to a Template Version (see note below for VBMSR-34336 guidance on building conditional equations).
   c.	The user is able to specify that a Letter Restriction for a Template Version is based upon the existence of ‘Draft’ Letter Instances associated with the Workflow Instance the Letter Editor is currently working.
      i.	The user is required to select the Template(s) that will block the creation of a new Letter Instance.
      ii.	The user is required to enter a message to be displayed to the Letter Editor explaining why the Letter is not available to be created.
   d.	The user is able to specify the following Letter Restrictions for letters that can only be created or finalized by a request from an external System Actor:
      i.	The Letter Restriction inhibits activities for manually creating the Letter Instance.
      ii.	The Letter Restriction inhibits activities for finalizing the Letter Instance.
   e.	The user is able to modify any existing Letter Restrictions for a Template Version in ‘Draft’ Status.
   f.	The user is able to remove any existing Letter Restrictions for a Template Version in ‘Draft’ Status.

Preconditions:
1.	A ‘Full’ Template Version in ‘Draft’ Status exists within the user’s Line of Business.

Postconditions:
1.	New Letter Restriction(s) have been configured for the Template Version.
2.	Existing Letter Restriction(s) for the Template Version have been modified or removed.
3.	Within Letter Manager, dependent on the result of letter restriction conditions, letters will either be available or not available to the Letter Editor.

Main Flow/Use Case:
Users can specify Letter Restrictions for a Template Version in ‘Draft’ Status, in a Changeset assigned to them, based upon conditional equations constructed by the user.  This flow is specific to determining if a Template Version should be either disabled from creation by the Letter Editor or totally hidden from the Letter Editor.
1.	The user selects an existing ‘Full’ Template Version in Template Manager to apply restrictions.
2.	The user creates or modifies relevant Letter Restrictions.
   a.	The user defines all necessary conditional rules for the Letter Restrictions (see Note below for VBMSR-34336 guidance on building conditional equations).
3.	The user indicates the specific outcome for the Template Version when the Letter Restriction conditions have been met.
   a.	When a Letter Restriction specifies that a letter should be visible, but disabled from the Letter Editor’s use, the letter will be visible to the Letter Editor but cannot be selected.
      i.	The user defines a message indicating to the Letter Editor why the letter is not selectable.
   b.	When a Letter Restriction specifies that a letter should be hidden from the Letter Editor selection list, the letter is hidden from the Letter Editor.

Alternative Path/Exceptions:
Users can specify Letter Restrictions for a Template Version in ‘Draft’ Status, in a Changeset assigned to them, based upon the existence of pending (see Note definition) Letter Instances.
1.	The user selects an existing ‘Full’ Template Version in Template Manager to apply restrictions.
2.	The user indicates that the Template Version is restricted from being used to create a new Letter Instance if the following is true:
   a.	A pending Letter Instance already exists in the Workflow Instance (see Note definition) for the defined Template Version(s).
      i.	The user is required to define the Template Version(s) that will block the creation of a new Letter Instanc

Alternative Path/Exceptions:
Users can specify Letter Restrictions for a Template Version in ‘Draft’ Status within their Line of Business based upon an external System Actor request.
 
1.	The user indicates that a Full Template Version prohibits manual letter creation or finalization activities by the Letter Editor and only allows those activities when requested by an external System Actor.
   a.	When the restriction affects letter creations activities, the user is required to enter an informative message to be displayed to the Letter Editor when they try to create a Letter Instance with this restriction applied.
   b.	When the restriction affects letter finalization activities, the user is required to enter an informative message to be displayed to the Letter Editor when they try to finalize a Letter Instance with this restriction applied.
   c.	If a System Actor requests creation or finalization of a letter with this restriction, all activities are allowed to proceed.

Notes:
1.	See VBMSR-34336 for requirements that outline the definition of conditional fields and how to construct conditional tests within a Template Version.
2.	Examples of Letter Restriction types:
   a.	String conditional – where Claim Contention name = “PTSD”
   b.	Boolean conditional – where Veteran claim contention indicates unemployability is set to true
   c.	Numeric conditional – where Veteran number of dependents > 0
3.	Definition of a “pending” Letter Instance: A Letter Instance that is not in a finalized or canceled status.
4.	Definition of a “Workflow Instance”: Letter instances that have the same LoB, Workflow and Workflow Key Parameter Type values.
5.	Letter rules and restrictions affecting “Follow-up” and “Linked” letters will be addressed in future requirements.
6.	The conditional logic in this use case will be implemented using 'expression based conditions' aligned with existing approach in DGMT.
