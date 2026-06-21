# Introduction to Terraform

An introduction to Infrastructure as Code (IaC) and Terraform, covering why IaC is important and how Terraform automates cloud infrastructure management.

## 🎯 What is Infrastructure as Code (IaC)?

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure using code instead of manual configuration.

Rather than creating cloud resources through a web console, infrastructure is defined in configuration files that can be version-controlled and reused.

### Benefits of IaC

* **Consistency** – Deploy identical infrastructure across environments.
* **Time Efficiency** – Automate repetitive provisioning tasks.
* **Cost Management** – Create and destroy resources when needed.
* **Scalability** – Easily replicate infrastructure.
* **Version Control** – Track changes using Git.
* **Reduced Human Error** – Minimize manual configuration mistakes.
* **Collaboration** – Teams can review and manage infrastructure together.

---

## 🌍 What is Terraform?

Terraform is an open-source Infrastructure as Code (IaC) tool developed by HashiCorp.

It allows users to define cloud infrastructure using declarative configuration files and automatically provision resources across multiple cloud providers such as AWS, Azure, and Google Cloud.

Terraform helps manage:

* Virtual Machines
* Storage Services
* Databases
* Networking Components
* Kubernetes Clusters
* Security Resources

---

## ⚙️ How Terraform Works

Terraform follows a simple workflow:

```text
Write Terraform Configuration Files
            ↓
     Run Terraform Commands
            ↓
 Terraform Provider Calls APIs
            ↓
 Cloud Resources are Created
```

For AWS deployments:

```text
Terraform Configuration
          ↓
     AWS Provider
          ↓
       AWS APIs
          ↓
     AWS Resources
```

---

## 🔄 Terraform Workflow Phases

### 1. Initialize the Working Directory

```bash
terraform init
```

Downloads required providers and initializes the Terraform project.

---

### 2. Validate Configuration Files

```bash
terraform validate
```

Checks configuration syntax and verifies that the files are valid.

---

### 3. Create an Execution Plan

```bash
terraform plan
```

Shows what Terraform will create, modify, or destroy before making changes.

---

### 4. Apply Infrastructure Changes

```bash
terraform apply
```

Creates or updates infrastructure to match the desired state defined in the configuration.

---

### 5. Destroy Infrastructure

```bash
terraform destroy
```

Removes all resources managed by Terraform.

---

## 📚 Key Learnings

* Infrastructure as Code enables automated and repeatable infrastructure management.
* Terraform uses declarative configuration files to define infrastructure.
* Terraform communicates with cloud providers through Providers.
* The Terraform workflow consists of:

  * Initialization
  * Validation
  * Planning
  * Applying
  * Destroying
* Terraform improves consistency, scalability, and collaboration while reducing manual effort.

---

## 🛠️ Commands Used

```bash
terraform init
terraform validate
terraform plan
terraform apply
terraform destroy
```
