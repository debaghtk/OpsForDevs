# Exercise 3: Setting Up a Continuous Integration Pipeline

## Objective
Set up a Continuous Integration (CI) pipeline that runs on every commit and pull request. The pipeline should validate the codebase by running tests, checking code style, and performing linting and formatting checks.

## Instructions

1. **Choose a CI Tool**
   Select one of the following CI tools:
   - GitHub Actions
   - Jenkins
   - CircleCI
   - GitLab CI
   - Travis CI
   - Azure DevOps

2. **Set Up Your CI Configuration**
   Create a configuration file for your chosen CI tool. The exact filename and location will depend on your chosen tool.

3. **Define the CI Pipeline**
   Your CI pipeline should include the following steps:
   
   a. **Code Validation**
      - Run all unit tests
      - Check code style (e.g., PEP 8 for Python)
      - Perform linting (e.g., pylint for Python)
      - Verify code formatting (e.g., Black for Python)

   b. **Trigger Conditions**
      - Configure the pipeline to run on every commit to the main branch
      - Configure the pipeline to run on every pull request

4. **Implement the Pipeline**
   - Write the necessary configuration to implement each step of the pipeline
   - Ensure that the pipeline fails if any step fails

5. **Test the Pipeline**
   - Make a commit that should pass all checks
   - Make a commit that should fail one or more checks
   - Create a pull request and verify that the CI pipeline runs

6. **Review and Iterate**
   - Review the output of your CI pipeline
   - Make any necessary adjustments to improve its effectiveness or efficiency

## Bonus Tasks
1. Add code coverage reporting to your CI pipeline
2. Implement automatic deployment to a staging environment on successful CI runs
3. Set up notifications (e.g., Slack, email) for pipeline results

## Deliverables
1. CI configuration file
2. Brief explanation of your CI setup and any challenges faced
3. Screenshots or logs showing successful and failed pipeline runs

Remember, the goal is to catch issues early and often. Your CI pipeline should provide quick feedback to developers about the quality and correctness of their code.

