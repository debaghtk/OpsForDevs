# Exercise 4: Packaging, Versioning, and Artifact Management

## Objective
Building on the CI pipeline from Exercise 3, package your code and dependencies into a single artifact, implement versioning, and push the artifact to a repository for both Docker and Vagrant ecosystems.

## Instructions

1. **Choose an Artifactory**
   Select an artifact repository to store your packages. Some options include:
   - JFrog Artifactory
   - Nexus Repository Manager
   - GitHub Packages
   - Docker Hub (for Docker images)
   - Vagrant Cloud (for Vagrant boxes)

2. **Packaging for Docker**
   a. Create a Dockerfile that includes your application code and all dependencies.
   b. Build a Docker image with a version tag. Use semantic versioning (e.g., v1.0.0).
   c. Push the Docker image to your chosen artifactory.

3. **Packaging for Vagrant**
   a. Create a Vagrantfile that sets up your application environment.
   b. Package your application code and Vagrantfile into a Vagrant box.
   c. Version your Vagrant box using semantic versioning.
   d. Push the Vagrant box to your chosen artifactory or Vagrant Cloud.

4. **Implement Versioning**
   a. Use semantic versioning (MAJOR.MINOR.PATCH) for your artifacts.
   b. Automate the versioning process in your CI pipeline.
   c. Ensure that each build creates a uniquely versioned artifact.

5. **Update CI Pipeline**
   Extend your CI pipeline from Exercise 3 to include:
   a. Building the Docker image and Vagrant box.
   b. Versioning the artifacts.
   c. Pushing the artifacts to the chosen artifactory.

6. **Test the Process**
   a. Make a change to your codebase.
   b. Commit and push the change.
   c. Verify that the CI pipeline builds new versions of both Docker and Vagrant artifacts.
   d. Confirm that the new artifacts are pushed to the artifactory with the correct version.

7. **Document the Process**
   Update your project documentation to include:
   a. How to retrieve and use the Docker image.
   b. How to retrieve and use the Vagrant box.
   c. The versioning scheme and how to interpret version numbers.

## Bonus Tasks
1. Implement a process for promoting artifacts from a development to a production repository.
2. Set up a staging area where artifacts can be tested before being promoted to production.
3. Implement a rollback strategy for reverting to previous versions if issues are found.

## Deliverables
1. Updated CI configuration file that includes packaging and pushing to artifactory.
2. Dockerfile and Vagrantfile used for packaging.
3. Screenshots or logs showing successful pushing of versioned artifacts to the artifactory.
4. Updated project documentation explaining how to use the packaged artifacts.

Remember, the goal is to create reproducible, versioned artifacts that can be easily shared and deployed. This process should make it easier to manage different versions of your software and simplify deployment to different environments.

