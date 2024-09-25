# Catalyst Center Ops using GenAI
The repo includes the files for GenAI configuration management using function calling and Catalyst Center REST APIs.

The goal of the solution is to re-use existing Infrastructure as Code workflows, developed in Python, Ansible or Terraform, while providing an AI interface for the users to trigger the execution of CI/CD pipelines. 

# Cisco DNA Center Network Compliance

This repo hosts files for triggering Jenkins Pipelines, based on user input provided natural language.

**Cisco Products & Services:**

 - Cisco DNA Center, devices managed by Cisco DNA Center
 - Cisco DNA Center Python SDK

**Tools & Frameworks:**

- Python environment to run the application
- Optional: CI/CD platform if desired to automate the process
- OpenAI, or any other LLM model

**Usage**

Sample output of running the "catalyst_center_genai_config_tools.py" application:

```shell
I am a network assistant running network automation workflows. What network configuration task are you interested in? Start the software upgrade process for the device with the hostname NYX-RO

 Workflow name: software_distribution
 Params identified: 
      {"hostname": "NYX-RO"}

 Do you want to continue or not (y/n)? n

 I am a network assistant running network automation workflows. What network configuration task are you interested in? Provision this swithc PDX-ACCESS at this location Global/OR/PDX/Floor-2

 Workflow name: provision_network_device_jenkins
 Params identified: 
      {"hostname": "PDX-ACCESS", "siteHierarchy": "Global/OR/PDX/Floor-2"}

 Do you want to continue or not (y/n)? y

 Network Assistant: Device provisioning started, see status here: https://10.93.141.47:8443/job/Provision%20Device/

 I am a network assistant running network automation workflows. What network configuration task are you interested in? q
Exiting chatbot...
 End of Application "catalyst_center_genai_config_tools.py" Run: 2024-09-25 14:53:33

```


**License**

This project is licensed to you under the terms of the [Cisco Sample Code License](./LICENSE).


