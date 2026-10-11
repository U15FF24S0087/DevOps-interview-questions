# DevOps Interview Questions - Answers

## Part 1: Azure Boards, Jira, and Trello

### What is Azure Boards?
Azure Boards is a work-tracking feature within Azure DevOps that helps teams plan, manage, and track work throughout the software development lifecycle. It supports Agile, Scrum, and Kanban processes and allows teams to create and manage work items such as epics, features, user stories, tasks, bugs, and issues.

Key features of Azure Boards include:
- Backlogs and sprint planning
- Kanban boards and dashboards
- Work-item tracking and custom fields
- Integration with Azure Repos and Azure Pipelines
- Reporting and analytics for team progress

### What is Jira?
Jira is an issue and project tracking tool from Atlassian, widely used by software teams for agile planning and delivery. It is used to manage tasks, bugs, stories, epics, sprint boards, and project workflows.

Common Jira capabilities:
- Scrum boards and Kanban boards
- Backlogs and sprint planning
- Reporting such as burndown and velocity charts
- Workflow automation and issue linking
- Integration with Git, CI/CD tools, and third-party apps

### What is Trello?
Trello is a simple visual collaboration tool based on Kanban-style boards. It allows users to create cards, move them across columns, and track progress in a lightweight way. Trello is best suited for small teams, task tracking, and quick project management.

Key characteristics:
- Easy-to-use boards, lists, and cards
- Flexible workflow management
- Labels, due dates, checklists, and comments
- Great for lightweight project tracking and team collaboration

### What is the difference between Azure Boards, Jira, and Trello?
The main difference is the level of complexity and the target use case:

- Azure Boards: part of Azure DevOps, designed for enterprise-level agile project management with deep integration into Azure tooling and DevOps workflows.
- Jira: a more powerful and configurable issue tracker for software teams, suitable for medium to large teams and complex workflows.
- Trello: simpler and more lightweight, ideal for less complex tasks, personal productivity, and basic project tracking.

In short:
- Azure Boards = enterprise DevOps work tracking in Microsoft ecosystem
- Jira = versatile agile project management and issue tracking
- Trello = lightweight Kanban collaboration board

### What are Epics, Features, User Stories, Tasks, Bugs, Spikes, and Issues?
These are types of work items used in agile project management.

- Epic: a large body of work that is too big to complete in one sprint; it is broken into smaller items.
- Feature: a distinct capability or functionality that delivers business value; usually part of an epic.
- User Story: a requirement written from the user perspective, such as: "As a user, I want to log in so that I can access my account."
- Task: a unit of work needed to complete a story or feature; often technical or operational.
- Bug: an issue that describes a defect or problem in the product.
- Spike: a time-boxed investigation or research task used to gather information before implementing a feature or fixing a bug.
- Issue: a general term for any problem, task, or concern that needs attention; in Jira and Azure Boards, it can mean a work item or problem record.

### What statuses are used on Jira or Azure DevOps boards?
Statuses represent the current stage of a work item in its workflow. Common statuses include:

- To Do / New
- In Progress / Active
- In Review / Code Review
- Done / Closed / Resolved
- Blocked
- Reopened
- Deferred / Cancelled

The exact statuses depend on the board setup and workflow configuration. For example:
- Jira boards usually use custom workflows defined by the project admin.
- Azure DevOps boards also allow custom states based on the process template (Agile, Scrum, or CMMI).

### Is a status the same as a work-item type?
No. A status and a work-item type are different concepts.

- Work-item type (WIT): defines what the item is, such as Epic, Story, Task, or Bug.
- Status: defines where the item is in its workflow, such as To Do, In Progress, or Done.

Example:
- Work item type = User Story
- Status = In Progress

A single work-item type can have multiple statuses, and a workflow can be customized per type.

---

## Part 2: Azure DevOps Fundamentals

### What is Azure DevOps?
Azure DevOps is a Microsoft platform that provides a set of tools for planning, developing, delivering, and monitoring software projects. It includes services such as:

- Azure Repos for source control
- Azure Pipelines for CI/CD automation
- Azure Boards for project tracking
- Azure Test Plans for testing
- Azure Artifacts for package management

Azure DevOps helps teams collaborate and automate the entire software development lifecycle.

### What is a pipeline?
A pipeline is an automated workflow used to build, test, validate, and deploy code from source to target environments. Pipelines are a core part of CI/CD.

Typical pipeline steps include:
- Get source code from a repository
- Install dependencies
- Build the application
- Run unit and integration tests
- Package artifacts
- Deploy to staging or production

### How do you create a pipeline in Azure DevOps?
To create a pipeline in Azure DevOps:

1. Go to your Azure DevOps project.
2. Click Pipelines in the left menu.
3. Select New Pipeline.
4. Choose the source repository (for example, Azure Repos Git, GitHub, or another supported repo).
5. Select the repository and branch to use.
6. Choose a pipeline template or create a YAML pipeline.
7. Define the pipeline steps (build, test, deploy) in YAML or using a classic UI pipeline.
8. Save the pipeline.
9. Run it manually or trigger it automatically based on code changes.

A common example is a YAML file such as azure-pipelines.yml that defines the stages and jobs.

### How do you connect Azure Repos to Azure Pipelines?
You connect Azure Repos to Azure Pipelines by creating a pipeline and selecting the repository as the source.

Typical steps:
1. Open Azure DevOps.
2. Navigate to Pipelines > New Pipeline.
3. Select Azure Repos Git.
4. Choose the repository and branch.
5. Select a template or configure YAML.
6. Save and run the pipeline.

If the pipeline needs access to external services, you may also configure service connections, authentication, or environment variables.

### What is the difference between Azure DevOps and GitOps?
Azure DevOps and GitOps are related but not the same.

- Azure DevOps is a platform for end-to-end software delivery and lifecycle management.
- GitOps is a deployment and infrastructure management approach where Git is the single source of truth for infrastructure and application configuration.

In GitOps:
- Desired state is stored in Git repositories.
- Automated systems compare the cluster or environment state with Git.
- Any drift is corrected automatically.

Azure DevOps can be used to implement GitOps by running pipelines that apply Kubernetes manifests or infrastructure-as-code changes from Git repositories.

### What are the advantages of DevOps?
DevOps brings several benefits to an organization:

- Faster software delivery
- Continuous integration and continuous deployment
- Better collaboration between development and operations teams
- Improved product quality through automation and testing
- Faster feedback and issue detection
- Reduced deployment risk and downtime
- Better traceability and auditability
- More efficient use of resources

### What is version control, and why is it important in DevOps?
Version control is a system that tracks changes made to files and code over time. It allows multiple developers to work on the same project without overwriting each other’s work.

Popular version control systems include Git and Azure Repos.

Why version control is important in DevOps:
- Tracks code history and changes
- Enables branching and merging for feature development
- Supports collaboration across teams
- Helps roll back to previous versions if needed
- Supports CI/CD pipelines by triggering builds on code changes
- Improves traceability and debugging
- Makes change reviews and audits easier

In DevOps, version control is foundational because it enables automation, team collaboration, and reliable software delivery.

---

## Summary
Azure Boards, Jira, and Trello are all work-management tools, but they differ in complexity and ecosystem. Azure DevOps is a broad DevOps platform that includes code management, project tracking, CI/CD, testing, and artifact management. Pipelines automate the delivery process, and version control is essential for collaboration, traceability, and reliable deployments. DevOps itself brings automation, faster delivery, and better team alignment, all of which help organizations build and ship software more efficiently.

---

## Part 7: Company and Placement Preparation

### Who owns Jira? Is Atlassian a product-based company?
Jira is owned by Atlassian, a global software company headquartered in Australia. Yes, Atlassian is primarily a product-based company because it develops and sells software products such as Jira, Confluence, Bitbucket, and Trello.

### What is the difference between a product-based and a service-based company?
A product-based company creates and sells its own software products or platforms. It usually focuses on building scalable products for customers, often with a strong engineering and innovation culture.

A service-based company provides IT, consulting, or software development services to other organizations. It usually works on client projects, delivers solutions based on client requirements, and may not own a product in the market.

Examples:
- Product-based: Microsoft, Atlassian, Google, Amazon
- Service-based: TCS, Infosys, Wipro, Accenture

### What DevOps questions should a fresher prepare for placements?
Freshers should prepare both basic and practical DevOps questions, such as:

- What is DevOps?
- What is Git and why is it used?
- What is CI/CD?
- What is a pipeline?
- Difference between Git and GitHub
- Difference between Docker and Kubernetes
- What is a container?
- What is a Kubernetes pod?
- What is Azure DevOps?
- How does Jenkins work?
- What is infrastructure as code?
- What is version control?
- What is the difference between DevOps and Azure DevOps?
- Explain the DevOps lifecycle
- What is an artifact?
- What are common cloud services such as EC2, S3, Azure VM, Azure App Service, etc.?
- How do you deploy an application?

For fresher interviews, basic concepts and practical explanations matter more than advanced architecture.

### Will BCA freshers get DevOps questions during placements?
Yes, BCA freshers can absolutely get DevOps questions during placements, especially if they are applying for IT, cloud, or software roles. Even if their degree is not directly technical, they may still be asked basic DevOps and Linux/Git questions. The difficulty depends on the company and the role.

### Should you mention DevOps and Azure DevOps on your resume?
Yes, if you have relevant knowledge, projects, or certifications. Mentioning DevOps and Azure DevOps can be valuable if you can explain the concepts clearly and relate them to practical projects. However, it is important to be honest and only include tools and skills you truly understand.

Good resume examples:
- DevOps Fundamentals: Git, CI/CD, Azure DevOps, pipelines, YAML
- Azure DevOps: Azure Repos, Pipelines, Boards, Artifacts
- Tools: Git, Linux, Docker, Bash, Jenkins, Terraform

Avoid listing tools you cannot explain in an interview.

### What is the DevOps lifecycle, and what happens at each stage?
The DevOps lifecycle is a continuous process that connects software development and operations. The standard stages are:

1. Plan
   - Define requirements, goals, and timelines.
   - Use tools like Jira, Azure Boards, or Trello.

2. Code
   - Developers write code and store it in version control systems like Git.

3. Build
   - Source code is compiled and packaged into build artifacts.

4. Test
   - Automated tests check for bugs, security issues, and quality problems.

5. Release
   - Approved changes are prepared for deployment.

6. Deploy
   - The application is deployed to development, testing, staging, or production environments.

7. Operate
   - The application runs in production and is monitored for performance and issues.

8. Monitor
   - Logs, metrics, and alerts are used to detect errors, downtime, or performance problems.

Then the loop repeats, improving performance and reliability continuously.

### How does Azure DevOps support the DevOps lifecycle?
Azure DevOps supports the lifecycle through its integrated services:

- Azure Boards: planning and tracking work items
- Azure Repos: source code management and version control
- Azure Pipelines: build, test, and deployment automation
- Azure Artifacts: package and dependency management
- Azure Test Plans: testing and quality validation
- Azure Monitor and integrations: operational monitoring and reporting

This creates a connected DevOps workflow from planning to production monitoring.

### What is the difference between DevOps and Azure DevOps?
DevOps is a broad engineering culture and practice that combines development and operations to shorten delivery cycles and improve software quality.

Azure DevOps is a Microsoft product that provides tools to implement DevOps practices. It is not the same as DevOps itself; it is a platform that supports it.

In simple terms:
- DevOps = concept, philosophy, and practice
- Azure DevOps = toolset/platform used to enable DevOps

### Why is DevOps important?
DevOps is important because it helps organizations deliver software faster, with better quality and lower risk. It improves collaboration across teams, enables automation, reduces manual work, and helps detect and fix issues quickly.

Key benefits include:
- Faster releases
- More reliable deployments
- Better teamwork
- Reduced downtime
- Improved productivity and customer satisfaction

---

## Part 8: Practice Questions

### A developer pushes code, and automated tests run immediately. Which practice is this?
This is Continuous Integration (CI).

CI is the practice where developers frequently merge code changes and automated builds/tests run automatically after each commit or push.

### What is the difference between a Bug and a User Story?
A Bug is a defect or issue in the software that is not working as expected. It describes a problem in the current product.

A User Story is a feature or requirement from the end user’s perspective. It describes what a user wants to achieve, usually in a format such as: "As a user, I want to log in so that I can access my account."

### In Jira, is “In Progress” a work-item type?
No. "In Progress" is a workflow status, not a work-item type.

Examples:
- Work-item type: Story, Task, Bug
- Status: To Do, In Progress, Done

### What does a Spike primarily help a team do?
A Spike is primarily used to investigate or research an uncertain or complex problem before committing to implementation. It helps the team gather information, estimate effort, and reduce risk before starting development.

---

## Part 3: Docker, Containers, and Virtualization

### What is the difference between Docker and a container?
Docker is a platform and toolset used to build, package, ship, and run containers. A container is the actual runtime unit that holds an application and its dependencies.

In simple terms:
- Docker = technology/tool used to create and manage containers
- Container = the isolated execution environment

### What is a container, and how does it help in DevOps?
A container is a lightweight, portable, and isolated environment that packages an application along with its dependencies, libraries, and runtime. It allows the application to run consistently across different environments.

How it helps in DevOps:
- Consistent builds and deployments across environments
- Faster startup compared to virtual machines
- Easier automation in CI/CD pipelines
- Improved scalability and portability
- Simplifies microservices-based deployments

### What is the difference between a virtual machine and a container?
A virtual machine (VM) includes a full guest operating system, virtual hardware, and application stack. It is heavier and slower to start.

A container shares the host operating system kernel and only packages the application and required dependencies. It is much lighter and faster.

Comparison:
- VM: more isolated, heavier, slower
- Container: lighter, faster, more portable, shares OS kernel

Containers are preferred for application packaging and deployment in modern DevOps workflows, while VMs are still used for full OS isolation and legacy workloads.

---

## Part 4: DevOps Process and Architecture

### What is the DevOps process, and how does it work?
The DevOps process is a set of practices that connect software development and operations into a continuous flow. It typically works like this:

1. Developers write code and commit it to a version control system.
2. A CI pipeline automatically triggers builds and tests.
3. Quality checks ensure the code is valid and secure.
4. The application is packaged as an artifact.
5. Deployment pipelines push the code to testing, staging, or production.
6. Monitoring tools collect logs, metrics, and alerts.
7. Feedback from monitoring is used to improve future releases.

This creates a continuous loop of improvement and delivery.

### What is the architecture of Azure DevOps?
Azure DevOps architecture typically includes the following major services:

- Azure Boards: planning and work tracking
- Azure Repos: source control and code hosting
- Azure Pipelines: CI/CD automation
- Azure Artifacts: package management
- Azure Test Plans: testing and quality assurance
- Integration with GitHub, Azure resources, and external tools

The architecture is centered around a single project where teams plan work, manage code, automate builds/tests, and deploy applications.

### How can Azure DevOps and GitOps work together in a deployment architecture?
Azure DevOps can be used to automate the GitOps workflow by:

- Pulling infrastructure or Kubernetes manifests from Git repositories
- Running validation and security checks through pipelines
- Applying infrastructure changes using tools like Terraform or kubectl
- Triggering deployments when Git changes are pushed
- Enforcing policy checks before production deployment

In this model, Git stays as the source of truth, while Azure DevOps pipelines act as the automation engine that manages environment state and deployment workflows.

### What are the disadvantages or challenges of DevOps?
Some common challenges include:

- Requires cultural change and team collaboration
- Initial setup and automation can be time-consuming
- Toolchain complexity can increase with multiple systems
- Security and compliance must be built into pipelines
- Monitoring and incident response need continuous attention
- Poorly designed pipelines can create deployment failures and instability

DevOps is powerful, but it requires discipline, process maturity, and automation to be effective.

---

## Part 5: Security Fundamentals

### What is a CVE?
A CVE (Common Vulnerabilities and Exposures) is a publicly known security vulnerability or exposure in software or hardware. Each CVE has a unique identifier and is used to track and communicate a vulnerability across the industry.

### What is a vulnerability, and how does DevOps help manage it?
A vulnerability is a weakness in software, infrastructure, or configuration that could be exploited by an attacker.

DevOps helps manage vulnerabilities by:
- Automating security testing in CI/CD
- Scanning code and dependencies for known issues
- Using secure configuration management
- Applying patches and updates quickly
- Monitoring environments for suspicious activity

### What is DevSecOps?
DevSecOps is the practice of integrating security into the DevOps process from the beginning, rather than treating it as a last step. It ensures security checks, vulnerability scanning, and compliance controls become part of the software delivery pipeline.

Examples of DevSecOps practices:
- SAST and DAST scanning
- Dependency vulnerability scanning
- Secret management
- Policy enforcement in pipelines
- Container image scanning

---

## Part 6: CI/CD and Common Interview Questions

### What is the difference between Continuous Integration, Continuous Delivery, and Continuous Deployment?
These are related but different practices.

- Continuous Integration (CI): developers merge code changes frequently, and automated builds/tests run on each integration.
- Continuous Delivery (CD): code is always in a deployable state, and the team can release it to production when approved.
- Continuous Deployment (CD): every valid change is automatically deployed to production without manual approval.

Summary:
- CI = build and test automatically
- CD = release-ready pipeline
- Continuous Deployment = automatic production release

### What is Infrastructure as Code (IaC)?
Infrastructure as Code is the practice of managing and provisioning infrastructure using machine-readable configuration files instead of manual setup. It allows teams to automate infrastructure creation, updates, and versioning.

Examples of IaC tools:
- Terraform
- Azure Resource Manager (ARM)
- Bicep
- CloudFormation

Benefits:
- Consistency across environments
- Repeatability and faster provisioning
- Version control for infrastructure changes
- Easier rollback and auditing

### What is the difference between Docker and Kubernetes?
Docker is a platform for building and running containers.

Kubernetes is an orchestration platform used to manage, scale, and automate container workloads across multiple hosts or nodes.

In short:
- Docker runs individual containers
- Kubernetes manages containerized applications at scale

### What is a build agent in Azure Pipelines?
A build agent is a machine or runtime environment that executes pipeline jobs such as build, test, and deployment tasks. Azure Pipelines can use Microsoft-hosted agents or self-hosted agents.

Build agents run the commands defined in the pipeline and report results back to Azure DevOps.

### What happens when an Azure DevOps pipeline fails?
When a pipeline fails:

- The job stops at the failed step
- The failed task or stage is marked with an error
- Build/test/deployment status is reported in Azure DevOps
- Developers can inspect logs to diagnose the issue
- The pipeline may block deployment to the next environment

This helps the team identify and fix problems before release.

---

## Final Interview Tip
To prepare well for DevOps interviews and placement exams, practice answering questions in a simple, clear, and confident way. Focus on understanding the concepts, not memorizing long paragraphs. For every topic, be ready to explain:

- What it is
- Why it is used
- When it is used
- How it fits into the DevOps lifecycle

This will help you answer both technical and HR-style interview questions effectively.
