
# Usecase to Req Workflow SOP

## Steps to Run Prompt Chain

### 1. Create a Local Respoitory
- Go to Github.com
- On the left hand side of the screen, select the green button labeled **New** in the **Top Respoitories** column.
- **Choose Owner** (choose yourself or a member of your team)
- Enter **Repository Name** (e.g 'Local-Sandbox')
- Description is optional
- Create a README is optional, you can do this later
- Select the green button labeled **Create Repository**

### 2. Create a file with the name 'subjectusecase.md' in local repository
- Select your local repository.
- Select **Add File** and then, **Create New File**.
- Name the file 'subjectusecase.md', confirm correct spelling, must be exact for prompt to work because the file name is used in prompt chain.
- Enter a name for the Initiative and Epic(s) at the top of the file, see example file in this folder. Decide how many Epics you will create with the use case and create a title for each and include it at the top of the file.
- Copy & Paste a Use Case into this file.
- Select the green button labeled **Commit Changes** and confirm.
- You should see a file in your local repository titled 'subjectusecase.md'
- Tip: In your personal repository, or a repository you share with your team (Calypso, Metis, Ganymede, Cosmos, Carpo), create a new file. Do not edit the Prompt Chain in Cheryl's repository.

### 3. Copy the content of 'ocrh-usecase-to-req.md'
- Copy the content of 'orch-usecase-to-req.md' from Cheryl's Repository 'cheryl-blocker/BID_Requirements_Team_Repo/SOP'.
  
### 4. Start new Copilot Chat Session
- Paste the content of 'orch-usecase-to-req.md' into the chat.
  
### 5. Attach the following files
- Select **'Attach'**, then **'Files, Folders, Symbols'**
- Select Cheryl's Repository **'cheryl-blocker/BID_Requirements_Team_Repo'**
- Attach **'usecase-to-req'** folder
- Select **'Attach'**, then **'Files, Folders, Symbols'**
- Select Your Repository
- Attach **'subjectusecase.md'**
  
### 6. Submit

## How It Works

The Input outlined here should produce two markdown (.md) files.
- The first contains the requirements, one initiative and an epic for each title included in the orch-usecase-to-req.md file.
- The second contains revisions that shows how copilot modified its work for each step. This can help identify errors in processing.

### 1. Input

- The workflow begins with a **Use Case input** provided in chat or as source text.

### 2. Automated Step Processing

The chain executes the following steps in order, using the prompt files in `usecase-to-req/`:

1. `step1_transpose.md`
2. `step2_writeAC.md`
3. `step3_formatAC.md`
4. `step4_etcAC.md`
5. `step5_testVS.md`
6. `step6_testSB.md`
7. `step7_formatSG.md`

For each step:
- The relevant prompt file is read.
- Instructions are combined with the latest output (or initial input for step 1).
- The step is processed **immediately and automatically**.
- No pausing, review, or user feedback is allowed between steps.
