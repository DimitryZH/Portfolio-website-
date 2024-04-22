### Overview:

The "Crafting and Hosting Portfolio Website with GitLab CI/CD" project serves as a platform to showcase a collection of my other projects, featuring links, diagrams, overviews, and more. The portfolio website is developed using HTML, CSS, and JavaScript, and it's containerized using Docker with an Nginx image for seamless deployment. The CI/CD pipeline is orchestrated using GitLab CI/CD, encompassing Dockerization, CI/CD workflows, and infrastructure management on AWS EC2.

- I used my own dmitry-web.com domain name for the deployment. 
- To explore the deployed portfolio website, visit this link: [https://projects.dmitry-web.com](https://projects.dmitry-web.com)

## Technologies:

  [![Terraform Badge](https://img.shields.io/badge/Terraform-623CE4?style=for-the-badge&logo=terraform&logoColor=white)](#)
  [![GitLab Badge](https://img.shields.io/badge/GitLab-FCA121?style=for-the-badge&logo=gitlab&logoColor=white)](#)
  [![Git Badge](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)](#)
  [![Docker Badge](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](#)
  [![Nginx Badge](https://img.shields.io/badge/Nginx-269539?style=for-the-badge&logo=nginx&logoColor=white)](#)
  [![AWS Badge](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](#)
  [![Linux Badge](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](#)
  [![HTML Badge](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
  [![CSS Badge](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)
  [![JavaScript Badge](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)
  [![VSCode Badge](https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](#)

## Project Diagram:
![crafting-portfolio-website](https://github.com/DimitryZH/portfolio-website-GitLab-CICD/assets/146372946/f3ce4ae4-e731-4050-8bec-4183bcecf17a)

### Implementation: 

1. **Project Setup on GitLab:**
   - Establish a GitLab repository to house project files and related resources.
   - Integrate the repository with Visual Studio Code for efficient development workflows.

2. **Local Development:**
   - Construct the portfolio website locally using HTML, CSS, and JavaScript, incorporating links, diagrams, and project overviews.

3. **Dockerization:**
   - Define a Dockerfile to encapsulate the portfolio website within a Docker image, leveraging the Nginx base image for optimal serving capabilities. Check out the  [`Dockerfile`](https://github.com/DimitryZH/portfolio-website-GitLab-CICD/blob/main/Dockerfile) here. 
   - Conduct local testing to validate the Dockerized application's functionality and compatibility.

4. **CI/CD Setup with GitLab:**
   - Configure a comprehensive CI/CD pipeline on GitLab [`.gitlab-ci.yml`](https://github.com/DimitryZH/portfolio-website-GitLab-CICD/blob/main/.gitlab-ci.yml)  to automate build and deployment processes.
   - Specify distinct stages for building and pushing Docker images, as well as deploying to AWS EC2.

5. **AWS EC2 and Docker Setup with Terraform:**
    - Create AWS resources and install Docker on an EC2 instance using Terraform to serve as the production server for hosting the Dockerized portfolio website.
   - Utilize Terraform to automate the deployment process, ensuring consistency and repeatability.
   - Check out the Terraform configuration file [`ec2_docker_nginx.tf`](https://github.com/DimitryZH/portfolio-website-GitLab-CICD/blob/main/ec2_docker_nginx.tf) for detailed implementation.


6. **CI/CD Workflow:**
   - Triggered by commits to the main branch on GitLab, GitLab CI/CD orchestrates the pipeline's execution.
   - During the build stage, the Docker image for the portfolio website is constructed and subsequently pushed to the GitLab Container Registry.
   - The deploy stage involves SSH access to the AWS EC2 instance, where the latest Docker image is pulled from the registry and deployed within a Docker container.

### Future Improvements

- **Monitoring and Logging:**
   - Implement monitoring tools to track the performance and health of the EC2 instance and Docker containers.
   - Introduce logging mechanisms for comprehensive visibility into application behavior and system events.




