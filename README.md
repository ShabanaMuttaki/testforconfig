  # Validate Configuration Yaml Files using  Github Actio

A Github project using GitHub Action for checking if YAML Configuration files comply with specified schema. 
  
Usage
To use the action simply create an country.yml file in the /Configfiles directory.

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

## Next Step:

  Save the file. It will automatically trigger the workflow process and validation of yaml files will happen

Results can be viewed under the workflow action



