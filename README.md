# Overview
This is the configuration management repository for the **UH Login** user interface. It is currently implemented using the CAS Overlay methodology.
# Branch Management
In the event that two configurations are activiely changing at the same time, past configurations are kept in branches so that they can be updated separately.

Branches:
- main -- the current configuration is in the main branch
- v7.0 -- example previously deployed configuration
# Deployment
Update the CAS version in gradle.properties and rebuild/redeploy.

To overlay an existing CAS overlay folder:
  git clone git@rep11.pvt.hawaii.edu:iam-developers/uh-login-overlay-cas-6.x.git cas-overlay-template
# Non-Prod Warning Message
The text message for non-prod environments is dynamically set in src/main/resources/static/css/cas/css, entry **.uh-not-prod-warning:before**.
```
    /* target substitution string must match "content:" target string in deployment script ~cas/bin/deploy-cas-uh-login.sh */
    content: "UH_NON_PROD_WARNING_CONTENT_ENVIRONMENT_ID";
```
