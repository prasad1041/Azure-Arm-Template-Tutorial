# Azure-Arm-Template-Tutorial
 The template is a JavaScript Object Notation (JSON) file that defines the infrastructure and configuration for your project
# Features Of Arm Template
 1. **Declarative syntax**
    Desired State Configuration: ARM templates use a declarative syntax, meaning you describe what you want rather than how to achieve it. You specify the resources and their configurations, and Azure Resource          Manager ensures that your Azure environment matches this desired state.
 2.**Repeatable results**
    deployments are consistent and repeatable. You can use the same template to deploy identical environments across different regions or subscriptions, minimizing the risk of configuration drift.
 3. **Orchestration**
    When deploying resources in Microsoft Azure using ARM (Azure Resource Manager) templates, Resource Manager handles the entire deployment process efficiently and intelligently.
 4. **Dependency Management**:
    Resource Manager evaluates the dependencies between resources defined in the template. If a resource depends on another resource (e.g., a virtual machine depends on a virtual network),Resource Manager ensures that the dependent resource is created first.
 5. **Correct Order:**
    By understanding these dependencies, Resource Manager orchestrates the deployment in the correct order. This ensures that all necessary prerequisites are met before a resource is created.
 6. **Modular files**: Deployment of multiple resources can be divided in multiple template.
 7. **Preview changes**
     You can use the what-if operation to get a preview of changes before deploying the template.
 8. **Built-in validation**
    Your template is deployed only after passing validation. Resource Manager checks the template before starting the deployment to make sure the deployment will succeed. Your deployment is less likely to stop in a half-finished state.
 9. **CI/CD integration**
     You can integrate templates into your continuous integration and continuous deployment (CI/CD) tools, which can automate your release pipelines for fast and reliable application and infrastructure updates

# The template has the following sections:

- **Parameters** - Provide values during deployment.
- **Variables** - Define values that are reused in templates. They can be constructed from parameter values.
- **User-defined functions** - Create customized functions that simplify template.
- **Resources** - Specify the resources to deploy.
- **Outputs** - Return values from the deployed resources.

# Modes of Deployment
Azure Resource Manager supports two deployment modes: incremental and complete.

- **Incremental mode**
The default deployment mode is incremental. In this mode, Resource Manager doesn't delete anything. If resources exist in the resource group but aren't specified in the template, Resource Manager leaves them alone. Resources in the template are added to the resource group if they don't already exist, and if they do exist, Resource Manager updates them to the configuration in the template.

- **Complete mode**
You have to explicitly ask for your deployment to run in complete mode. When you use this mode, resources that exist in Azure but that aren't specified in the template are deleted. Complete mode doesn't delete all resources in your resource group. Some resource types are exempt.

# Template deployment process
To deploy a template, use any of the following options:
- Azure portal
- Azure CLI
- PowerShell
- REST API
- Button in GitHub repository
- Azure Cloud Shell
  
# Why to use apiVersion in Template?
the apiVersion you set in the template for the resource is used as the API version for the REST operation. You can repeatedly deploy the template and have confidence it will continue to work. By using the same API version, you don't have to worry about breaking changes that might be introduced in later versions.

# Template design
- deploy your three tier application through a single template to a single resource group.

   ![image](https://github.com/prasad1041/Azure-Arm-Template-Tutorial/assets/96993480/19c07f0d-125a-4630-917e-1f1edd8e9f9c)
  
- deploy a three tier solution through a parent template that includes three nested templates.

   ![image](https://github.com/prasad1041/Azure-Arm-Template-Tutorial/assets/96993480/5fb38a8c-ac64-4773-8673-560a811343f0)
  
- deploy your three tiers to separate resource groups.

  ![image](https://github.com/prasad1041/Azure-Arm-Template-Tutorial/assets/96993480/abd5d081-3af8-402c-9abd-1fe0c6e2747c)

**Template specs** service provided by azure enable you to store a template as a resource type. You use role-based access control to manage access to the template spec.

  
