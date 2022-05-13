# update-gitops-task


## Util Functions

### GitClone

This function clone your git repository. it takes following parameters 

- repo: repo to clone (Required)
- user: username of git user for authentication
- password: password of git user for authentication

**Return:** Repo object

#### Example 
 ```
 repo = GitClone("https://github.com/hanzala1234/py-script-test-temp","/tmp/file-123","my_user","dummy_password")
```
### UpdateChartFile

This function update dependency and chart version of Chart.yaml. it takes following parameters

- path: path of ```Chart.yaml``` file (Required)
- version: Version of updated chart (Required)

**Return:** nil

#### Example
``` 
 UpdateChartFile(repo.working_dir+"/Chart.yaml","2.2.7")
```

### SetGitConfig

This function set global git config username and password. it takes following parameters

- repo: repo object (required)
- user: username of git user (required)
- email: email of git user (required)

**Return:** nil

#### Example
``` 
 SetGitConfig(repo,"user1","user1@gmail.com")
```

###  WriteYaml

This function writes dict object into yaml file. It takes following parameters

- path: path of yaml file to write data
- data: data to write to yaml file

#### Example
``` 
 WriteYaml(path,data)
```

**Return:**  nil 

### GetYamlData

This function returns dict object from yaml file. it takes following parameters

- path: path of yaml file to read data from

#### Example
``` 
 getYamlData(path)
```

**Return:**  data object 
