# Validate Configuration Yaml Files
- Validates the yml configuration files with respect to schema
- Input Configuration files: /Configfiles/<Country>_Config.yml 
- Schema files: /schema/schema.yml 
- Workflow definition: for yaml validation inside actions under name Validate Yml
- When new countries are added go to /.github/workflows/validate.yml and add the config file name in line number 26.
  
  
 Validate Configuration Yaml Files using   Github Actio
A Github action for checking if YAML files comply with specified schema.

Usage
To use the action simply create an country.yml file in the /Configfiles directory.

For example:

name: India_Config.yml
  testConfig:
 - key: BOSCH_B2B
   name: BOSCH B2B
   plp_bazaarvoice: true
   plp_noresults: false
   pdp_tabsvisible:
    - Tech_Specs
    - Reviews


Next Step:
  Save the file. It will automatically trigger the workflow process and validation of yaml files will happen

