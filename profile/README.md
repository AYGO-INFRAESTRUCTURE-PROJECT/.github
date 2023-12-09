# Infrastructure Automation and Continuous Deployment Solution

## Executive Summary

In response to the growing complexity and dynamism of modern IT infrastructures, we have successfully implemented an Infrastructure Automation and Continuous Deployment Prototype Solution using utilizing Amazon Web Services (AWS) Cloud Development Kit (CDK), sam-cli, GitHub Actions, a customized API and a user-friendly front-end client. This cutting-edge solution enables us to efficiently manage infrastructure changes, enhance development workflows, and ensure a seamless and reliable deployment process. 

### Architecture

![PROJECT-ARCHITECTURE](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45974699/579d394f-85b5-4166-8694-ca9c7caf36ad)


## Concepts: 

### AWS 
AWS or Amazon Web Services is a cloud service provider, offering storage services, computing resources, applications, databases, etc. 

### SAM CLI  

The AWS [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html) is a command line tool that you can use with AWS SAM templates and supported third-party integrations to build and run your serverless applications.

Use the AWS SAM CLI to: 

- Quickly initialize a new application project. 

- Build your application for deployment. 

- Perform local debugging and testing. 

- Deploy applications. 

- Configure CI/CD deployment pipelines. 

- Monitor and troubleshoot your application in the cloud. 

- Sync local changes to the cloud as you develop. 

- And more!



### CDK  

The [AWS Cloud Development Kit (AWS CDK)](https://docs.aws.amazon.com/cdk/v2/guide/home.html) is an open-source software development framework to define cloud infrastructure in code and provision it through AWS CloudFormation. 

It offers a high-level object-oriented abstraction to define AWS resources imperatively using the power of modern programming languages. 

### Github Actions  

[GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) is an automated workflow and continuous integration/continuous deployment (CI/CD) platform provided by GitHub. Allows to define and execute custom workflows directly in a GitHub repository. These workflows can automate various tasks, such as building, testing, and deploying code, in response to events like pushes, pull requests, or other GitHub activities. 

## Overview:  

The primary goal of this solution is to streamline the management of AWS infrastructure by leveraging powerful automation tools and cloud-native services. By integrating sam-cli into our deployment pipeline, we have achieved a high degree of automation in provisioning, updating, and scaling cloud resources. Additionally, GitHub Actions serve as the orchestrator for this automation, enabling a seamless integration of infrastructure changes with our codebase.


## Key Components: 

### SAM for Deployment:

AWS SAM is at the core of our deployment strategy, facilitating the deployment of AWS resources.  

### Custom API for Template Guidance: 

Our custom API acts as a knowledge hub for creating templates, providing the tools for structuring and configuring stacks. 

### AWS CDK for Template Generation: 

The AWS CDK takes the lead in generating infrastructure templates. With the help of the API, it uses the received data to define or update a stack using a programming language. 

### GitHub Actions for Continuous Deployment: 

GitHub Actions has been seamlessly integrated into our workflow, automating the continuous deployment process. This includes validating changes, running tests, and deploying updates to the stacks using SAM. The integration with GitHub Actions ensures a robust and efficient CI/CD pipeline. 

### Front-End Client for User Interaction: 

The front-end client serves as an intuitive interface, simplifying the interaction with new or updated stacks. Users can effortlessly manage and monitor the deployment process, providing both technical and non-technical stakeholders with a user-friendly experience.


## Project components

- [Graphic tool for template visualization](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/FRONT-TEMPLATE-GENERATOR)
- [API and Template Generator](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/API-TEMPLATE-GENERATOR)
- [Automatic template deployment](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/GITHUB-ACTIONS-LOAD)


## Benefits: 

### Streamlined Deployment Process: 

The combined power of SAM, CDK, and GitHub Actions streamlines the deployment process, reducing manual intervention and speeding up the delivery of changes to the infrastructure. 

### Collaborative Infrastructure Development: 

Infrastructure as code with CDK fosters collaboration and version control, while the custom API provides real-time guidance. This collaborative approach ensures that infrastructure changes align with best practices and project requirements. 

### Efficient Continuous Deployment: 

GitHub Actions automates the continuous deployment pipeline, providing a reliable mechanism for validating, testing, and deploying changes. This results in increased efficiency and a faster feedback loop for developers. 

### User-Centric Front-End Interface: 

The front-end client enhances user experience, making it convenient for both technical and non-technical users to manage and monitor the deployment of new stacks or updates. This focus on user-centric design promotes usability and accessibility.


## Use Cases
1. Serverless Application Deployment.
2. Infrastructure as Code (IaC) Updates
3. Multi-Region Deployments
4. Custom Resource Management
5. Infrastructure Updates Based on Pull Requests
6. Artifact Management
7. Continuous Learning and Documentation


## Conclusion:  

Our integrated solution represents a leap forward in infrastructure management, combining the strengths of SAM, CDK, GitHub Actions, and a user-friendly front-end. By leveraging these tools synergistically, we have created an ecosystem that not only accelerates deployment but also enhances collaboration, reliability, and the overall user experience in managing AWS stacks. 

## Autores
[Andres Ricardo Martinez Diaz](https://github.com/Ricar8o)
[David Alejandro Vasquez Carreño](https://github.com/alejovasquero)
[Richard Santiago Urrea Garcia](https://github.com/RichardUG)

## Licencia & Derechos de Autor
**©** Andres Ricardo Martinez Diaz, Ingeniero de Sistemas

**©** David Alejandro Vasquez Carreño, Ingeniero de Sistemas

**©** Richard Santiago Urrea Garcia, Ingeniero de Sistemas

Licencia bajo la [GNU General Public License](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/blob/main/profile/LICENSE).
