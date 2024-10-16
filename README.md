# GitHub-Action
GitHub Actions is a CI/CD (Continuous Integration and Continuous Delivery) tool that allows you to automate, customize, and execute your software development workflows directly in your GitHub repository. 

## Concept ##

- Workflows: Defined in .yml files in the .github/workflows/ directory of your repository. They define a series of jobs that will be run based on events like push or pull_request.
- Jobs: A job contains a sequence of steps to be executed. Jobs can run in parallel or sequentially.
- Steps: Individual tasks performed in a job (e.g., running shell commands, executing scripts).
- Actions: Reusable commands that can be combined in steps to build, test, or deploy your code.

 ## GitHub actions are of two types ##

 *GitHub-Hosted GitHub Actions*

GitHub-hosted runners are the default option provided by GitHub for running workflows in GitHub Actions. 

- Managed Environment: GitHub automatically provides and manages the environment, including hardware, operating systems, and the necessary software, tools, and dependencies.

- Pre-Installed Tools: GitHub-hosted runners come with many pre-installed development tools (e.g., compilers, interpreters, Git, Docker, etc.). This reduces setup time, especially for common programming languages and CI/CD tasks.

- Automatic Scaling: You don't need to manage the hardware or worry about scaling your build environment. GitHub scales the resources depending on your workflow needs.

*Self-Hosted GitHub Actions*

- Self-hosted runners are machines that you manage yourself. They can be any machine, including physical servers, virtual machines, or even cloud-based virtual instances.

- Custom Hardware and Configuration: You have complete control over the machine running your workflows. You can choose the hardware specifications, install custom software, and configure the environment exactly as you need.

- Performance: Self-hosted runners can be configured with more powerful hardware if needed, allowing for greater control over performance.

- Unlimited Execution Time: There's no strict time limit for how long jobs can run on self-hosted runners, making them ideal for lengthy processes or resource-intensive workloads.

- Customization: You can install any software, services, or custom tools you need on self-hosted runners, allowing for full customization of your environment.

### When to use what ###

*GitHub-Hosted Runners* are great if you want an easy-to-use, scalable, and managed CI/CD environment without worrying about infrastructure or maintenance.

*Self-Hosted Runners* are useful when you need more control over the environment, want to avoid GitHub’s job execution limits, or have specific security and customization requirements.

### How to execute Self-Hosted Github ###

- Launch your EC2 instance with port 443 and port 80 active on both inbound and outbound rule
- Go to the youe Git repo and to go it's setting
- Under Action create a new self-hosted runner and select the configuration according to your EC2 instance
- Download and Configure the runner on your EC2 instance too
- and make changes in the .github/workflows/ file from Github hosted to Self Hosted
