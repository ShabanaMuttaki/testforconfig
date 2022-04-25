  # Validate Configuration Yaml Files using  Github Action

## About:

A Github project using  Actions for checking if YAML Configuration files comply with specified schema. Whenever Configuragtion files are edited or added , workflow action is automatically triggered and the validation of Yaml files takes place.

  
## Usage:

#### Step 1:
To use the action simply create an country_config.yml file in the [/Config files](https://github.com/ShabanaMuttaki/testforconfig/tree/main/configfiles) directory.


For example:
name: India_Config.yml

```

  testConfig:
 - key: BOSCH_B2B
   name: BOSCH B2B
   plp_bazaarvoice: true
   plp_noresults: false
   pdp_tabsvisible:
    - Tech_Specs
    - Reviews
```
#### Step 2:
 Add the new file path inside the [.github/workflows/validate.yml](https://github.com/ShabanaMuttaki/testforconfig/tree/main/.github/workflows/validate.yml) on **files-to-validate:**
 
 ```
        files-to-validate: '[{ "path": "configfiles/Portugal_Config.yml", "schema": "schemas/schema.yml"},{ "path": "configfiles/Germany_Config.yml", "schema": "schemas/schema.yml"},{ "path": "configfiles/India_Config.yml", "schema": "schemas/schema.yml"}]'

```
#### Step 3:

  Save the file. It will automatically trigger the workflow process and validation of yaml files will happen

Results can be viewed under the workflow [Actions](https://github.com/ShabanaMuttaki/testforconfig/actions) like below.

<img width="1671" alt="Screen Shot 2022-04-25 at 13 41 36" src="https://user-images.githubusercontent.com/104023149/165082121-2f4328d9-93e7-432d-9edb-65257ff017aa.png">

## Further Enhancements:
The workflow can be further enhanced to push the config files to different repositories or to create a pull request with an approver to merge or decline.



