## Gitlab Configuration File

GitLab follows DevOps best practices such as Pipeline as code. The **.gitlab-ci.yml** file is the code behind the CI pipeline of your project. Located in the root repository of the project, the **.gitlab-ci.yml** file, meaning the CI pipeline, is version controlled with the source code itself (making builds almost immutables).   

In this file, you can define the scripts you want to run, define include and cache dependencies, choose commands you want to run in sequence and those you want to run in parallel, define where you want to deploy your app, and specify whether you will want to run the scripts automatically or trigger any of them manually. Once you’re familiar with GitLab CI/CD you can add more advanced steps into the configuration file.
