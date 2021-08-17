

### Branching, Merging and Tagging

**Stratagy-0**: Zero branching strategy

*master* >>> managing development code - day to day builds on this branch - developers will directly commit the code to this branch.


------


**Strategy-1: Master and develpment(or feature) braching strategy**

*master* >>> managing development code - day to day builds on this branch

*feature* >>> for day to day development

*hotfix* >>> Create a new branch "hostfix-####" from master or tag (from the production code) to fix if there are any PROD issues.

Workflow: 

   Create pull request from *feature-####* branch to *master* >>> code review

   Approve the pull request to merge "feature" branch code to "master" whenever build is required.

   Build will create a git tag with release version.


![image](https://user-images.githubusercontent.com/24622526/129722803-1baf3176-66c2-4fac-b987-432fbe96398d.png)


------

**Strategy-2: Master, develop and feature braching strategy**

*master* >>> managing prod code

*development/develop* >>> managing development code and day to day builds on this branch

*hotfix* >>> Create a new branch *hostfix-####* from master or tag (from the production code) to fix if there are any PROD issues.

Workflow: 

  Create "feature" branch from *development/develop* when there is a requirement to add/update the code

  Merge the code from "feature" branch to "develop" >> Build the code from "develop" branch 

Merge the code to "master" branch when code successfully deployed to PROD. 


![image](https://user-images.githubusercontent.com/24622526/129722695-5b8e7cbc-84c8-46b0-b43a-2b1e10e4a5b9.png)


------

**Strategy-3: Master, develop, release and feature braching strategy**

![image](https://user-images.githubusercontent.com/24622526/129723009-0d68956c-7d92-4e90-ab24-7c50d7dd642a.png)



Case-2: Branching stratagy for each TEST environment.

DEV >>> QA >>> SYST >>> UAT >>> PROD

Case-3: Forking from main repo >> development >> merging

Fork the main repository >> Update the code >> Create the pull request to main repo (merge the code)



Reference docs:

https://clubhouse.io/blog/why-you-need-a-branching-strategy/

https://www.sitepoint.com/use-git-branches-buddy/

