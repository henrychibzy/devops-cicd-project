Automated Web Application Deployment Using CI/CD

Project Overview

This project demonstrates how DevOps practices can automate the build and deployment of a simple web application. The application is built with HTML and CSS, containerized using Docker, and deployed online using Render. GitHub Actions automates the Docker build verification process whenever code changes are pushed to the repository.

Objectives

* Create and host a simple web application.
* Store source code and configuration files in GitHub.
* Containerize the application using Docker.
* Automate build verification using GitHub Actions.
* Deploy the application using Render.
* Test automatic deployment by committing a code change.
* Document the implementation and lessons learned.

Tools and Technologies

* HTML and CSS: Web application interface.
* GitHub: Source code management and version control.
* Docker: Application containerization.
* GitHub Actions: Automated CI workflow.
* Nginx: Web server used inside the Docker container.
* Render: Cloud hosting and automatic deployment.
* Markdown: Project documentation.

Project Structure

devops-cicd-project/
├── index.html
├── Dockerfile
├── README.md
└── .github/
    └── workflows/
        └── docker-build.yml

Implementation

1. Application Development

Created a responsive deployment dashboard using HTML and CSS.

2. Docker Configuration

Created a Dockerfile based on the lightweight Nginx Alpine image. The application file is copied into the Nginx web directory, where it can be served over HTTP.

3. Continuous Integration

Configured GitHub Actions to run when changes are pushed to the main branch or when a pull request targets the main branch. The workflow checks that the required files exist and builds the Docker image without publishing it to a container registry.

4. Cloud Deployment

Connected the GitHub repository to Render and deployed the application using its Dockerfile. Render handles the hosting and automatic deployment of repository changes.

5. Deployment Testing

Committed a change to the application footer to display “Deployment test: Version 2”. The GitHub Actions workflow completed successfully, Render completed the subsequent deployment, and the updated text appeared on the live application.

Challenges and Solutions

* Working without a computer: Used GitHub’s web interface on an iPhone to create and edit project files.
* Troubleshooting the CI workflow: Investigated a failed required-file check, verified the project files in the repository, and confirmed a subsequent workflow run succeeded.
* Verifying deployment: Made a visible code change and checked the live website to confirm the update was deployed.

What I Learned

* How GitHub supports source control and collaborative development.
* How Docker packages a web application for consistent execution.
* How GitHub Actions automates CI tasks.
* How a cloud hosting platform can deploy updates from a GitHub repository.
* Why testing, troubleshooting, and documenting deployment results are important DevOps practices.

Architecture

Developer commits code → GitHub repository → GitHub Actions builds and verifies the Docker image.

Separately, Render monitors the connected repository, builds the application using the Dockerfile, and deploys updates to the live website.

Project Links

* GitHub Repository: [https://github.com/henrychibzy/devops-cicd-project]
* Live Application: [Insert your Render URL]

Conclusion

This project demonstrates a practical introduction to Docker, continuous integration, and automated cloud deployment. It also provided hands-on experience troubleshooting a workflow, validating a live deployment, and documenting a software delivery process.
