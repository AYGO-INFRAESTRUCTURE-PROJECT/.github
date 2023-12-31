# Infrastructure Automation and Continuous Deployment Solution

# Table of Contents

1. [Introduction](#introduction)
   - [Problem Statement](#problem)
   - [Executive Summary](#executive-summary)

2. [Concepts](#concepts)

3. [Overview](#overview)
   - [Prototype Architecture](#prototype-architecture)

4. [Key Components](#key-components)
   - [SAM for Deployment](#sam-for-deployment)
   - [Custom API for Template Guidance](#custom-api-for-template-guidance)
   - [AWS CDK for Template Generation](#aws-cdk-for-template-generation)
   - [GitHub Actions for Continuous Deployment](#github-actions-for-continuous-deployment)
   - [Front-End Client for User Interaction](#front-end-client-for-user-interaction)

5. [Application View](#application-view)

6. [Business View](#business-view)
   - [Executive Leadership](#executive-leadership)
   - [IT Operations Teams](#it-operations-teams)
   - [Development Teams](#development-teams)
   - [Security Teams](#security-teams)
   - [Financial Stakeholders](#financial-stakeholders)
   - [Customers](#customers)

7. [Project Component Repositories](#project-component-repositories)

8. [Setting Credentials on Stacks Deployment](#setting-credentials-on-stacks-deployment)

9. [Steps](#steps)

10. [Use Cases](#use-cases)

11. [Benefits](#benefits)

12. [Conclusion](#conclusion)

13. [Authors](#authors)


## Introduction

### Problem
We noticed a problem that happens very commonly in small companies or in companies that are making an adoption to the cloud and do not know how to manage their resources correctly.
This problem consists in the lack of control and standards to manage infrastructure.

This results in:

- Deploying resources manually and prone to errors.
- Complexity to effectively manage the infrastructure of cloud projects.
- Lack of standards in infrastructure management
- Problems when configuring resources in the cloud
- Lack of traceability of infrastructure changes within the companies.

### Executive Summary

In response to the growing complexity and dynamism of modern IT infrastructures, we have successfully implemented an Infrastructure Automation and Continuous Deployment Prototype Solution using utilizing Amazon Web Services (AWS) Cloud Development Kit (CDK), sam-cli, GitHub Actions, a customized API and a user-friendly front-end client. This cutting-edge solution enables us to efficiently manage infrastructure changes, enhance development workflows, and ensure a seamless and reliable deployment process. 

## Concepts: 

### AWS 
AWS or Amazon Web Services is a cloud service provider, offering storage services, computing resources, applications, databases, etc. 

### SAM CLI  

The AWS [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html) is a command line tool that you can use with AWS SAM templates and supported third-party integrations to build and run your serverless applications.

### CDK  

The [AWS Cloud Development Kit (AWS CDK)](https://docs.aws.amazon.com/cdk/v2/guide/home.html) is an open-source software development framework to define cloud infrastructure in code and provision it through AWS CloudFormation. 

It offers a high-level object-oriented abstraction to define AWS resources imperatively using the power of modern programming languages. 

### Github Actions  

[GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) is an automated workflow and continuous integration/continuous deployment (CI/CD) platform provided by GitHub. Allows to define and execute custom workflows directly in a GitHub repository. These workflows can automate various tasks, such as building, testing, and deploying code, in response to events like pushes, pull requests, or other GitHub activities. 

## Overview:  

The primary goal of this solution is to streamline the management of AWS infrastructure by leveraging powerful automation tools and cloud-native services. By integrating sam-cli into our deployment pipeline, we have achieved a high degree of automation in provisioning, updating, and scaling cloud resources. Additionally, GitHub Actions serve as the orchestrator for this automation, enabling a seamless integration of infrastructure changes with our codebase.

## Prototype Architecture

![PROJECT-ARCHITECTURE](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45974699/579d394f-85b5-4166-8694-ca9c7caf36ad)


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

## Application View
![image](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45279329/d48aecbb-a412-4eec-9648-34ac0d5f96cb)


## Business View

The project's business view emphasizes a strategic shift towards modern, automated infrastructure deployment. This positions the organization for future growth by fostering agility, reliability, and cost-effectiveness in its technology operations. The value proposition for stakeholders highlights tangible benefits across various facets of the business, making it a strategic investment for sustained success.

### Executive Leadership:
**Value Proposition: Accelerated Time-to-Market**

By automating infrastructure deployment, the project significantly reduces the time required to bring new features or products to market. This aligns with business goals of staying ahead in a fast-paced industry.

### IT Operations Teams:

**Value Proposition: Improved Operational Efficiency**

The automated deployment process reduces the burden on IT operations, minimizing manual interventions, and mitigating the risk of errors. This results in smoother operations, reduced downtime, and improved resource utilization.

### Development Teams:

**Value Proposition: Enhanced Developer Productivity**

Developers benefit from faster feedback cycles, enabling them to iterate quickly. Automation frees up developers from manual deployment tasks, allowing them to focus on writing code and delivering business value.

### Security Teams:

**Value Proposition: Consistent Security Measures**

The use of SAM, AWS CDK, and GitHub Actions ensures that security measures are consistently applied across environments. Security teams can rely on standardized deployment processes, reducing the risk of misconfigurations.

### Financial Stakeholders:

**Value Proposition: Cost Optimization**

Automation not only accelerates deployment but also contributes to cost optimization. Efficient resource scaling and the ability to handle varying workloads reduce unnecessary resource consumption, aligning with financial goals.

### Customers:

**Value Proposition: Enhanced Service Reliability**

Faster deployments and reduced downtime contribute to a more reliable service for customers. Continuous improvements, facilitated by automated deployments, lead to a better overall customer experience.

## Project Component Repositories

- [Graphic tool for template visualization](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/FRONT-TEMPLATE-GENERATOR)
- [API and Template Generator](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/API-TEMPLATE-GENERATOR)
- [Automatic template deployment](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/GITHUB-ACTIONS-LOAD)

## Setting credentials on stacks deployment
In order for github actions to successfully perform deployments, repository secrets need to be configured with the credentials of an AWS account in the repository where the stacks are stored.

![image](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45279329/094b2254-e52c-4de0-b218-e58f523ab947)

## Steps:

### Deployment:
1. Configure Automatic template deployment repository:
   - Fork the repository, (you don´t need the stacks saved in stacks folder)
   - Push the repository on github
   - Set credentials of an AWS account
2. Configure API and Template Generator:
   - Fork the API and Template Generator repository
   - Set the Automatic template deployment repository on the `src/main/resources/application.properties`
   - Deploy this java backend and configure github credentials on the host.
3. Configure  the graphic tool with react:
   - Fork the Graphic tool for template visualization repository
   - Change the API url with the Template Generator API
   - Deploy this react web server

### Use:
Once you have deployed the tools and have the the Automatic template deployment repo on github.
1. Go to graphic interface
2. Specify the template resources
3. Review the template preview
4. Send the template
5. Review the workflow on github (You can also view for each stack the CloudFormation event logs on AWS)
6. Validate the resources have been deployed sucessfully 


## Automatic deploy on stacks upload showcase
When a template change is uploaded or a new template is uploaded, github actions takes care of review the template, check the changes and make the deployments.

![image](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45279329/2a19f3d0-9c46-42e5-8ae2-f316cf6e6477)

![image](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45279329/b6ddef6f-54a9-41e9-a22e-bdd386a467b5)

And if a stack has no changes it also shows that on the github actions workflow.

![image](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/assets/45279329/0ee08542-1e1f-4fd2-aad0-f0efc28fe7d2)


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

## Authors
[Andres Ricardo Martinez Diaz](https://github.com/Ricar8o)

[David Alejandro Vasquez Carreño](https://github.com/alejovasquero)

[Richard Santiago Urrea Garcia](https://github.com/RichardUG)

## Licencia & Derechos de Autor
**©** Andres Ricardo Martinez Diaz, Ingeniero de Sistemas

**©** David Alejandro Vasquez Carreño, Ingeniero de Sistemas

**©** Richard Santiago Urrea Garcia, Ingeniero de Sistemas

Licencia bajo la [GNU General Public License](https://github.com/AYGO-INFRAESTRUCTURE-PROJECT/.github/blob/main/profile/LICENSE).
