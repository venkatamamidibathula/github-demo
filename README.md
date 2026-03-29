# Github-Actions


### GitHub Actions Overview

**Workflow**: A workflow is an automated process that you define in your GitHub repository. It is made up of one or more jobs and can be triggered by events such as push, pull request, or on a schedule.

**Jobs**: A job is a set of steps that execute on the same runner. Jobs run in parallel by default, but you can configure dependencies between jobs to control the order of execution.

**Actions**: Actions are individual tasks that are combined as steps to create a job. GitHub provides a marketplace of reusable actions, or you can create your own.

### How They Are Connected


- **Workflow**: Defines the automated process and contains jobs.
- **Jobs**: Sets of steps that run on the same runner, defined within workflows.
- **Actions**: Individual tasks executed as steps within jobs.

![Alt text](githubactions.png)


By understanding these components and how they are connected, you can effectively create and manage CI/CD pipelines using GitHub Actions.

```yaml
name: first-workflow
on: workflow_dispatch
jobs:
  first-job:
    runs-on: ubuntu-latest
    steps:
      - name: Print Greeting
        run: echo "Hello World"
      - name: Print Goodbye
        run: echo "Bye-Goodbye"
```


**workflow_dispatch**: This will let the workflow run manually.


![Alt text](triggers.png)


---

# GitHub Administration


![Alt text](ssogithub.png)



