Azure Pipeline Status :

[![Build Status](https://dev.azure.com/DevOpsOrgERP/DevOpsProject/_apis/build/status%2Fshalini0910.ProjectDevOps?branchName=main)](https://dev.azure.com/DevOpsOrgERP/DevOpsProject/_build/latest?definitionId=2&branchName=main)




## **Cloud-DevOps Assignment Overview**

### **Objective**
As a DevOps engineer, the task is to architect and deploy an application, comprising a Java backend, React frontend, and an in-memory database (which can be migrated to a real cloud database). The goal is to build CI/CD pipelines, cloud infrastructure, and document the architecture, as well as provide automation for cleanup and scaling.

---


---

## **Solution Architecture**

### **Application Architecture**
- **Frontend**: React-based web UI hosted on a container.
- **Backend**: Java Spring-based service, containerized, and interfacing with a database.
- **Database**: Initially in-memory, with a planned migration to a managed cloud database.

### **Infrastructure Design**
- **Cloud Provider**: Azure
- **Components**:
  - Azure Kubernetes Service (AKS) or Azure App Service for container hosting.
  - Azure SQL/Cosmos DB for database storage.
  - Azure Storage for any persistent file storage requirements.
  - Azure Virtual Networks for networking.

### **High-level Design Diagram**

![pipeline.png](/.attachments/pipeline-7cdf4b92-89ac-475a-b240-a1323adc50ed.png)
---

## **CI/CD Pipelines**

### **Backend Pipeline**
- **Tasks**:
  - Build Java Spring code.
  - Unit testing and code quality checks.
  - Docker image creation.
  - Push image to Azure Container Registry.
  - Deploy to the appropriate environment (e.g., AKS or Azure App Service).

### **Frontend Pipeline**
- **Tasks**:
  - Build and test React code.
  - Dockerize the frontend.
  - Push to Azure Container Registry.
  - Deploy to the target environment.

---

## **Infrastructure as Code (IaC) Pipeline**

### **Infrastructure Components**:
- **Terraform/ARM Templates**:
  - Define infrastructure components such as virtual networks, load balancers, databases, and application hosting environments.
  
### **Cleanup and Destroy Functionality**:
- Implement functionality to tear down the infrastructure using Terraform destroy or ARM template cleanup scripts.

---

## **Monitoring and Auditing**

- **Azure Monitor**: Set up monitoring for the application and infrastructure.
- **Application Insights**: Monitor the performance and health of the deployed application.
- **Azure Policy**: Implement auditing policies to track the usage of resources and ensure compliance.

---

## **Scaling and Cloud Database**

- **Auto-scaling**: Set up auto-scaling using AKS or VM Scale Sets to handle increasing traffic and load.
- **Cloud Database**: Modify the application code to interface with a real database like Azure SQL or Cosmos DB.

---

## **Instructions for Deployment**

1. **Fork the Repository**:
   - Detailed instructions on how to fork the repository, configure cloud settings, and deploy the solution on a separate Azure account.
   
2. **Configuration**:
   - Set up service connections, environment variables, and secrets for deploying to Azure.

3. **Pipeline Execution**:
   - Step-by-step guide on how to run the pipelines and verify the deployment.

---

This structure organizes the requirements into sections, making it easier for teams to follow through and understand the deliverables.
