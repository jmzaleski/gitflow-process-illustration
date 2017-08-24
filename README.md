# gitflow-process-illustration
attempt at illustrating gitflow process with code.

## Proposed recipe

### hotfix branches. 
- create branch name prefixed with hotfix- off master
- make PR with name prefixed with [hotfix]
- eventually merge PR to master

### sync hotfix to development
- using same hotfix branch as above
- make PR from hotfix branch name against development with name prefixed with [sync-hotfix]

### feature branches
- create branch name prefixed with feature- off development
- make PR with name prefixed with [feature] against development
- eventually merge PR with development

### release branches
- create branch name prefixed with release- off development
- bump version number
- make PR with name prefixed with [sync-release] against development
- when satisfied that release branch is working merge PR with development

### release to master
- using same release- branch as above
- make PR with name prefixed with [release] this time against master
- merge [release] PR into master.
- can reasonably expect conflicts with hotfixes previously applied to master and development differently.               
