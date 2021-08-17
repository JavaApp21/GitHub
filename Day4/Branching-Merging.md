

### Branching, Merging and Tagging

**Stratagy-0**: Zero branching strategy

*master* >>> managing development code - day to day builds on this branch - developers will directly commit the code to this branch.

**Strategy-1: Master and develpment(or feature) braching strategy**

*master* >>> managing development code - day to day builds on this branch

*feature* >>> for day to day development

*hotfix* >>> Create a new branch "hostfix-####" from master or tag (from the production code) to fix if there are any PROD issues.

Workflow: 

   Create pull request from *feature-####* branch to *master* >>> code review

   Approve the pull request to merge "feature" branch code to "master" whenever build is required.

   Build will create a git tag with release version.

**Strategy-2: Master, develpment and feature braching strategy**

*master* >>> managing prod code

*development/develop* >>> managing development code and day to day builds on this branch

*hotfix* >>> Create a new branch *hostfix-####* from master or tag (from the production code) to fix if there are any PROD issues.

Workflow: 

  Create "feature" branch from *development/develop* when there is a requirement to add/update the code

  Merge the code from "feature" branch to "develop" >> Build the code from "develop" branch 

Merge the code to "master" branch when code successfully deployed to PROD. 

Case-2: Branching stratagy for each TEST environment.

DEV >>> QA >>> SYST >>> UAT >>> PROD

Case-3: Forking from main repo >> development >> merging

Fork the main repository >> Update the code >> Create the pull request to main repo (merge the code)

