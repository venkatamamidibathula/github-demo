# Github-Actions


### GitHub Actions Overview

**Workflow**: A workflow is an automated process that you define in your GitHub repository. It is made up of one or more jobs and can be triggered by events such as push, pull request, or on a schedule.

**Jobs**: A job is a set of steps that execute on the same runner. Jobs run in parallel by default, but you can configure dependencies between jobs to control the order of execution.

**Actions**: Actions are individual tasks that are combined as steps to create a job. GitHub provides a marketplace of reusable actions, or you can create your own.

### How They Are Connected

1. **Workflow**: The top-level definition that contains one or more jobs.
2. **Jobs**: Defined within a workflow, each job contains a sequence of steps.
3. **Actions**: Individual tasks that are executed as steps within a job.

### Diagram

```plaintext
+---------------------+
|     Workflow        |
|  (workflow.yml)     |
+---------------------+
           |
           v
+---------------------+
|        Job 1        |
|  (runs on runner)   |
+---------------------+
           |
           v
+---------------------+
|       Step 1        |
|      (Action)       |
+---------------------+
           |
           v
+---------------------+
|       Step 2        |
|      (Action)       |
+---------------------+
           |
           v
+---------------------+
|        Job 2        |
|  (runs on runner)   |
+---------------------+
           |
           v
+---------------------+
|       Step 1        |
|      (Action)       |
+---------------------+
           |
           v
+---------------------+
|       Step 2        |
|      (Action)       |
+---------------------+
```

### Example Workflow File (`.github/workflows/workflow.yml`)

- **Workflow**: Defines the automated process and contains jobs.
- **Jobs**: Sets of steps that run on the same runner, defined within workflows.
- **Actions**: Individual tasks executed as steps within jobs.

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


