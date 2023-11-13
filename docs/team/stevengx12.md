## Guan Xiao - Project Portfolio Page
### Project: QuizHub
QuizHub is a local desktop app designed to help NUS students easily record examinable questions and generate quizzes
from their very own question bank to test their understanding via a Command Line Interface (CLI). Easily launch-able
on the go, QuizHub is a versatile tool that aims to streamline and optimize the revision experience for NUS students
from all fields of study.

### Summary of Contributions
- **Code Contributions:** [Link to reposense contribution](https://nus-cs2113-ay2324s1.github.io/tp-dashboard/?search=&sort=groupTitle&sortWithin=title&timeframe=commit&mergegroup=&groupSelect=groupByRepos&breakdown=true&checkedFileTypes=docs~functional-code~test-code&since=2023-09-22&tabOpen=true&tabType=authorship&tabAuthor=StevenGX12&tabRepo=AY2324S1-CS2113-W12-1%2Ftp%5Bmaster%5D&authorshipIsMergeGroup=false&authorshipFileTypes=docs~functional-code~test-code&authorshipIsBinaryFileTypeChecked=false&authorshipIsIgnoredFilesChecked=false).
- The project structure of QuizHub is adapted from Juncheng's [ip](https://github.com/spinoandraptos/ip). Juncheng is
  responsible for migrating the skeleton code structure into the team repository and aligning the team for initial
  the integration cycle. [#6](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/6)

### New Feature 1: `Help Command`
  [#13](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/13)
  - **What:** Enables users to see a complete list of commands and their respectivve formats
  - **Justification:** Users, especially new ones, are likely going to need to refer to this list of command as a reference

### New Feature 2: `Module Attribute for Questions`
  [#50](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/50),
  [#48](https://github.com/AY2324S1-CS2113-W12-1/tp/issues/48)
  - **What:** Adds a `module` attribute to each question in the form a `String`
  - **Justification:** Allows users to categorize questions by modules so they can focus on a specific module to learn 

### Enhancement 2: `Search By Module Function`
  [#50](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/50)
  - **What:** Modified `find` command so that it allows user to search questions by module
  - **Justification:** Allow users to single out questions from a specific module to aid their learning on that module

### New Feature 3: `MCQ Class and Command`
  [#185](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/185)
  [#146](https://github.com/AY2324S1-CS2113-W12-1/tp/issues/146)
  - **What:** Added a new type of question (`MULTIPLECHOICE`)
  - **Justification:** Provides users with the flexibility to include multiple choice questions as opposed to only having short answer questions. This is a major feature which is more difficult to implement as it involves adding the new MCQ class, the appropriate command to add an MCQ to the list, as well as modifying several other associated methods in various classes such as the `Parser`, `Storage` and `QuestionList` class to accommodate the new question type.

### Enhancement 3: `Update Edit Command for MCQ`
  [#185](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/185),
  [#193](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/193),
  [#146](https://github.com/AY2324S1-CS2113-W12-1/tp/issues/146)
  - **What:** Modify `edit` command to be able to edit each individual field of a multiple choice question
  - **Justification:** Multiple choice questions have more fields that allow editting, so the command must be modified to accomodate this.Additinally, it also needs to make sure that the type of question being editted matches the field that is being editted

<div style="page-break-after: always;"></div>

### Code Testing and Improvement:
  [#39](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/39),
  [#49](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/49),
  [#97](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/97),
  [#133](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/133)
  * Refactored parsing logic from `find`and `edit` command into the main `Parser` class
  * Performed JUnit testing for commands to identify error-prone user input combinations
  - Ensured JUnit tests cover user input formats that are prone to bugs for the following commands:
    * CommandEdit
    * CommandFind
    * CommandDelete
    * CommandHelp

### User Guide Contributions:
  [#112](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/112)
  * Added `delete` and `find` command:
    - [Delete Question Command](https://github.com/AY2324S1-CS2113-W12-1/tp/blob/master/docs/UserGuide.md#delete-questions-delete)
    - [Find Question Command](https://github.com/AY2324S1-CS2113-W12-1/tp/blob/master/docs/UserGuide.md#find-questionanswermodule-find)

### Developer Guide Contributions:
  [#71](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/71),
  [#236](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/236),
  [#244](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/244)
  * Added and modified `Storage` and `UI` component:
    - [Storage](https://github.com/AY2324S1-CS2113-W12-1/tp/blob/master/docs/DeveloperGuide.md#storage-component)
    - [UI](https://github.com/AY2324S1-CS2113-W12-1/tp/blob/master/docs/DeveloperGuide.md#ui-component)

  [#229](https://github.com/AY2324S1-CS2113-W12-1/tp/pull/229)
  * Modified `CommandEdit` component: [CommandEdit](https://github.com/AY2324S1-CS2113-W12-1/tp/blob/master/docs/DeveloperGuide.md#edit-command---edit-question--answer)

### Team-Based Task Contributions:
  - Refactored code to general code enhancements
    * Performed code abstraction in `Parser` class to avoid deep nesting and excessively long methods
    * Performed code abstraction for string literals in commands so relevant methods will not need to hard code 
    the appropriate ui output
    * Refactored code to meet checkstyle requirements
  - Assisted in issue tracker maintenance to ensure team members are assigned to the right issues and avoid 
  potential work conflict
  - Assisted in formating DG diagrams and paragraphs to ensure consistency and accuracy

### Community Contributions
  - **Reviewing other team's UG and software program**: [Reported a total of 7 bugs for T17-4](https://github.com/StevenGX12/ped/issues)