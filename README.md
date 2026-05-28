# Java Web App Deployment with AWS CI/CD

Welcome to this project combining Java web app development and AWS CI/CD tools!

<br>

## Table of Contents
- [Introduction](#introduction)
- [Technologies](#technologies)
- [Setup](#setup)
- [Contact](#contact)
- [Conclusion](#conclusion)

<br>

## Introduction
This project is used for an introduction to creating and deploying a Java-based web app using AWS, especially their CI/CD tools.

The deployment pipeline I'm building around the Java web app in this repository is invisible to the end-user, but makes a big impact by automating the software release processes.

### Why I'm Building This
* **Career Growth:** I am tackling this project to bridge the gap between application development and modern cloud infrastructure, directly aligned with my goals of advancing into advanced cloud engineering and DevOps domains.
* **Practical Learning:** This project allows me to master the end-to-end deployment pipeline—moving code seamlessly from a local terminal and version control system directly to live cloud infrastructure.

<br>

## Technologies
Here’s what I’m using for this project:

- **Amazon EC2**: I'm developing my web app on Amazon EC2 virtual servers, so that software development and deployment happens entirely on the cloud.
- **VS Code**: For my IDE, I chose Visual Studio Code. It connects directly to my development EC2 instance, making it easy to edit code and manage files in the cloud.
- **GitHub**: All my web app code is stored and versioned in this GitHub repository.
- **[COMING SOON] AWS CodeArtifact**: Once it's rolled out, CodeArtifact will store my artifacts and dependencies, which is great for high availability and speeding up my project's build process.
- **[COMING SOON] AWS CodeBuild**: Once it's rolled out, CodeBuild will take over my build process. It'll compile the source code, run tests, and produce ready-to-deploy software packages automatically.
- **[COMING SOON] AWS CodeDeploy**: Once it's rolled out, CodeDeploy will automate my deployment process across EC2 instances.
- **[COMING SOON] AWS CodePipeline**: Once it's rolled out, CodePipeline will automate the entire process from GitHub to CodeDeploy, integrating build, test, and deployment steps into one efficient workflow.

### 🛠️ Challenges Faced & Solutions Found
* **Terminal Authentication Block:** Running into terminal authentication failures when pushing code using standard account passwords.
  * *Solution:* Shifted to secure token-based authentication by generating a GitHub Personal Access Token (PAT) with custom scopes (`repo`) and an expiration limit.

<br>

## Setup
To get this project up and running on your local machine, follow these steps:

1. Clone the repository:
```bash
    git clone [https://github.com/yourusername/nextwork-web-project.git](https://github.com/yourusername/nextwork-web-project.git)
    ```
2. Navigate to the project directory:
```bash
    cd nextwork-web-project
    ```
3. Install dependencies:
```bash
    mvn install
    ```

### 💡 Troubleshooting Tips
* **Terminal Stuck on Status/Log:** If your terminal feels "frozen" after running a tracking command like `git log`, it is just using a system pager to display long text. Press `q` on your keyboard to instantly quit the view and return to your prompt.
* **Frequent Password Prompts:** Since HTTPS connections are stateless, configure Git to securely cache your active credentials by executing:
```bash
  git config --global credential.helper store

