FeatureIDE is, as you might already have seen, hosted at github. So the main tool we are using is git.
As FeatureIDE has a wide range of developers we need to set up a common git workflow. 

### Commit messages
Always be as precise as possible what you have done and try to avoid messages like:'Did some stuff', 'Removed some stuff' e.g.

### Commit related changes
**ALWAYS** commit changes that are related to each other. Git has the possibility to stage lines and hunks and not only complete file. You can make use of this feature which helps to commit changes from one file which might have unrelated changes. E.g. please do not mix formatting or documentation commits with commits that have changes in programm logic

### Commit often
Not just put one commit for your complete work. Make more commits helps to share work with others and to keep on track what other developers meant with there work.

### Agree on a Workflow

#### Branching Workflow
Solving Issues and creating enhancements should always result in a corresponding branch. For issues we decided to name them after the issus e.g. *issue_110*
