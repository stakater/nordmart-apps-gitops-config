#  ManagedGitOpsAPI

Stakater Managed GitOps API to manage gitops repositories
  
##  Local Development

### **To run locally:**

API requires the following Environment variables to operate

- GIT_ACCESS_TOKEN
	- E.g. https://github.com/settings/tokens
	- *Required*
- GIT_REPOSITORY
	- E.g. https://github.com/stakater/gitops-config-template 
	- *Required*
- GIT_BRANCH
	- *Parent branch name on which API will merge branches and retrieve resources*
	- *Default value: main*
	- *Optional*
- GIT_COMMIT_BRANCH
	- *Child branch name prefix on which API will commit changes and merge with GIT_BRANCH*
	-  *Default value: GIT_BRANCH*
	- *Optional*
- GIT_USERNAME
	- *Username to use for commiting changes*
	- *Default value: stakater-gitops-bot*
	- *optional*
  

```terminal

make run-api GIT_ACCESS_TOKEN=ghp_o2amP9VB5DDJFP2u GIT_REPOSITORY=https://github.com/stakater/gitops-config GIT_BRANCH=testing-api GIT_COMMIT_BRANCH=api-test

```

##  Known Limitations

- Due to lack of  *branch merging* functionality of go-git library, currently the API is only compatible with github. 
