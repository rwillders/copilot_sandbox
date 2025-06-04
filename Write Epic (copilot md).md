# Write Epic Prompt

Follow the steps to execute this prompt:
- Read this entire markdown file.
- Create a plan to Write Epic using the Epic Planning Table format.
- Complete and present the Epic Planning Table.
- Ask for acceptance or rejection of the plan.
- If reject, ask for feedback on why the plan was rejected. When feedback is received, suggest updates to this prompt to implement the feedback.
- If accept, continue the following steps.
- Apply the plan to Write Epic for the Use Case provided.
- Respond with the Epic and provide an option to accept or reject.
- If reject, ask for feedback on why the Epic was rejected. When feedback is received, suggest updates to this prompt to implement the feedback.
- If accept, conclude prompt.

<!-- BEGIN EPIC PLANNING TABLE INSTRUCTIONS -->
 # Epic Planning Table Instructions

## Purpose
The Epic Planning Table provides a concise, structured approach to mapping Use Case elements to Epic components before writing the full Epic. This helps ensure all necessary information is properly transformed and nothing is missed.

## Table Structure
Create a table with three columns:
1. **Use Case Element** - The source information from the Use Case
2. **Epic Component** - The corresponding Epic section where this information will be used
3. **Transformation Notes** - Brief explanation of how the information will be transformed

## How to Create the Table in Markdown
```markdown
| Use Case Element | Epic Component | Transformation Notes |
|------------------|----------------|----------------------|
| Use Case Name | Epic Title | Direct use with "Ability to" format and proper capitalization |
| Description + Primary Actor | Value Statement | "As a [actor], I need [need from description], so that [benefit]" |
| Primary Actor | User in Value Statement | The primary user who benefits from the functionality |
| List of Abilities | Primary Acceptance Criteria | Each key ability becomes a primary AC with "As a [actor], I need to..." |
| Configuration Requirements | Secondary/Tertiary AC | Technical details become nested criteria |
| Preconditions | Assumptions | System states required before functionality can be used |
| Main/Alternate Flows | Detailed AC structure | User interaction steps inform the hierarchical AC structure |
| Postconditions | Validation criteria in AC | Expected outcomes used to validate completion criteria |
```

## Example Completed Table
| Use Case Element | Epic Component | Transformation Notes |
|------------------|----------------|----------------------|
| Use Case Name | Epic Title | "Ability to Create and Modify Text Input Field Placeholders in the Content of a Template" |
| Description + Primary Actor | Value Statement | "As a Changeset Editor, I need to control how values are displayed in letters, so that I can configure Templates effectively." |
| Primary Actor | User in Value Statement | "Changeset Editor" |
| List of Abilities | Primary Acceptance Criteria | Each ability becomes an AC starting with "As a Changeset Editor, I need to..." |
| Configuration Requirements | Secondary/Tertiary AC | Details on Trim (Boolean) and Capitalization options |
| Preconditions | Assumptions | Template in "Draft" status, has Text Input Fields |
| Main/Alternate Flows | Detailed AC structure | Steps in flows will inform the hierarchical AC structure |
| Postconditions | Validation criteria in AC | Ensures placeholders are properly created/modified |

## Integration Instructions
Add this table creation step to the "Create a plan to Write Epic" section of your Write Epic prompt. The table should be created before writing the full Epic and shared with the user for approval.
<!-- END EPIC PLANNING TABLE INSTRUCTIONS -->

<!-- BEGIN EPIC FORMAT -->
# Epic Format
Your Epic should follow this exact structure and formatting:

# Format and Indentation Guidelines:
- Primary Level acceptance criteria should begin with "As a [Primary Actor], I need to..."
- Use blank lines between each item at all levels for better readability
- Apply consistent indentation to show hierarchy:
- - Primary level (1, 2, 3): No indentation
  - Secondary level (a, b, c): Three space indentation
  - Tertiary level (i, ii, iii): Nine space indentation
- Maintain consistent spacing throughout the document
- Use bold formatting for field names and signle quotes for field values

## Value Statement:
Insert Value Statement

## Assumptions:
1. Insert Assumption 1
2. Insert Assumption 2
3. Etc.

## Acceptance Criteria:
1. Insert AC1 primary functional need
   a. Insert AC1 secondary functional need
      i. Insert AC1 tertiary functional need
      ii. Etc.
   b. Insert additional secondary functional need
2. Insert AC2 primary functional need
   a. Etc.

## Notes:
1. Insert Note 1
2. Insert Note 2
3. Etc.

<!-- END EPIC FORMAT -->

## Epic Title sectiion guidelines:
- Epic Titles are to be one sentence, starting with the words "Ability to".
- Epic Titles will capitalize the first letter of the first word, and all words except for articles, connectives, and prepositions.
- Epic Titles should match content of a "Use Case Name:" found in the Use Case.

## Requirements Epic Sections:
Use the following phrases as a section headers for each section within an Epic.
- Value Statement
- Assumptions
- Acceptance Criteria
- Notes
  
## Value Statement section guidelines:
- Value Statements follow the pattern of:  "As a [insert primary actor from Use Case], I need [insert Need derived from Use Case Description], so that [insert Benefit derived from Use Case Description]."
- The user represents the end user of the functionality.
- The Need represents the ability that the user will be provided.
- The Benefit represents the value that the user will experience by the need being provided.

## Assumptions section guidelines:
- Information that is pertinent to the requirements that impact the understanding of the business need and acceptance criteria
  
## Acceptance Criteria section guidelines:
- Acceptance criteria should state the functional need of the business.
- Acceptance criteria should represent a single requirement.
- Acceptance criteria can be structured with a primary functional need stated, and then decomposed into more granular detailed acceptance critiria that state business rules and alternative use cases that the primary acceptance criteria must support.
- Acceptance criteria must use complete sentences that are in active voice.
- Acceptance criteria should utilize definitive verbs and avoid non-definitive verbs such as 'should', 'may', 'could'.
- Acceptance criteria must be testable.
- Acceptance criteria should be agnostic to the user interface design.
- If the Primary Actor stated in the use case is a user, begin each Accepatance Criteria primary functional need with "As a [insert Primary Actor from Use Case], I need to...". Secondary, tertiary, and subsequent Acceptance Criteria listed underneath the first Accepatance Criteria do not need to begin with this phrase.

## Notes section guidelines:
- Information that provides context that explans the reason these requirements are needed
- Suggestions for how the user interface might implement an acceptance criteria

## Requirements Style Guidance
- When referencing field names, the names should be in Bold.
- When referencing specific values for contents of a field, the values should be in ‘single quotes’.
- When referencing Terms of Art, words or phrases that have a connotation or meaning specific to the process or program being worked on, the first letter of each word should be capitalized. Terms of Art are specified in the Use Case and formatted with the first letter of each word capitalized.
- The word "Veteran" should always be capitalized.