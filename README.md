# Sportradar DevOps Challenge - Darrell Shack

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

Hello All,

Welcome to my DevOps Challenge, below are the steps for the CI/CD  process:

1. Our CI/CI uses git actions to trigger workflow depending on pushes/merges to different branches within our repo. I have two branchs, one is our main branch and the other is feature.

2. When you add any commits or branches to our repo, it kicks off a linter and test. For our use case, we use the following yml files to check for dependencys and linting/testing:
    - code_quality_super-linter
    - dependency_security_scan
    - npm-commit

3. Once we check for the quality of code and dependencies, we can merge this into our main branch whiches kicks off our deployment/mutant testing with the following yml files:
    - mutant_testing_tool
    - npm-publish-deploy


*Bonus*

1. I attempted to add the function User as a lambda and the lambda based on the documentation will inherit some of the properties of the provider. (EX runtime)

2. Next, within the resource, I deployed a RDS instance based on Cloudformation syntax which would provide us the connection string.

3. Once the resource is deployed, I added an output section within the the template to capture the connection string of the RDS resource. I use this to reference an output that can be called from within the template.
