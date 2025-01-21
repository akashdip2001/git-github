[<img align="right" alt="GitHub Foundations exam logo" width="300" src="https://github.com/akashdip2001/akashdip2001/raw/main/img/Badge/github-actions.png">](https://www.linkedin.com/posts/akashdip2001_macbook-desktop-github-activity-7286721666125119488-G-B4) 

### GitHub Actions

Passing the GitHub Actions certification exam validates subject matter expertise with applying continuous integration/continuous delivery (CI/CD) patterns and practices using GitHub Actions in the enterprise.

---

#### Skills :

`Build Pipeline` ,  `Continuous Delivery` ,  `Continuous Integration`

`DevOps` , `GitHub` , `GitHub Actions` , `Release Management`

</br>
</br>
</br>

![Screenshot (876)](https://github.com/user-attachments/assets/8015d816-9b0b-48ce-b526-e60e31b60184)

<details>	
 <summary><b>Rules 🔐</b></summary>
  
![1](https://github.com/user-attachments/assets/f1d61bfb-918a-41b7-86ef-2823da5a7bfe)
![2](https://github.com/user-attachments/assets/59cb4aca-fa17-490e-baf7-7dff6a636ec5)
![3](https://github.com/user-attachments/assets/c250ff73-23fc-44ba-af55-67adc81c5394)

---

### 🔐 1. How does a proctor communicate with a test taker?
Answer: Through the live chat function.

### 🔐 2. Which of the below is considered a valid photo identification card?
Answer: A current government-issued photo identification card.

### 🔐 3. What is a proctor checking when reviewing a room scan prior to admission? (Select all that apply)
Answer:
 * The workspace is free of prohibited materials.
 * No other individuals are present.
 * Lighting is adequate.
   
### 🔐 4. At what point does the test timer start counting down?
Answer: When the test is released.

### 🔐 5. In order to end the test session properly, the test taker must...
Answer: Click on the end session button.

### 🔐 6. Which are the most common violations leading to the termination of a test? (Select all that apply)
Answer:
 * Someone else in the room.
 * Talking to yourself/reading questions aloud.
   
### 🔐 7. If a test taker grabs their cell phone and takes a picture of the results screen at the end of the test, what will the proctor do?
Answer: Terminate the test taker and file a report.

---

</details>

# ✅ Other User Questions & also collected from Google and modify for preparation using AI

**Page 1 of 75**

**Question:** GitHub-hosted runners support which capabilities? (Choose two)

**Options:**
- support for a variety of Linux variations including CentOS, Fedora, and Debian
- requiring a payment mechanism (e.g., credit card) to use for private repositories
- automatic patching of both the runner and the underlying OS
- automatic file-system caching between workflow runs
- support for Linux, Windows, and macOS

**Correct Answers:**
- **automatic patching of both the runner and the underlying OS**
- **support for Linux, Windows, and macOS**

**Supporting Statement:** GitHub-hosted runners are maintained by GitHub and offer features like automatic patching and support for various operating systems.

---

**Page 2 of 75**

**Question:** Which workflow event is used to manually trigger a workflow run?

**Options:**
- status
- create
- workflow_run
- workflow_dispatch

**Correct Answer:**
- **workflow_dispatch**

**Supporting Statement:** The `workflow_dispatch` event is specifically designed for manually triggering workflows via the GitHub API or the UI.

---

**Page 3 of 75**

**Question:** In which of the following scenarios should you use self-hosted runners? (Choose two)

**Options:**
- when a workflow job needs to install software from the local network
- when you want to use macOS runners
- when GitHub Actions minutes must be used for the workflow runs
- when jobs must run for longer than 6 hours
- when the workflow jobs must be run on Windows 10

**Correct Answers:**
- **when a workflow job needs to install software from the local network**
- **when jobs must run for longer than 6 hours**

**Supporting Statement:** Self-hosted runners provide access to your local network and can run for longer durations than GitHub-hosted runners.

---

**Page 4 of 75**

**Question:** A workflow that had been working now stalls in a waiting state until failing. The workflow file process_yaml-jobs specifying runs-on: [gpu] 1. Which of the following steps would troubleshoot the issue? (Choose two)

**Options:**
- Increase the usage limits for the GitHub-hosted runners.
- Review the contents of the Runner *.log files in the _diag folder.
- Update the org settings to enable GPU-based GitHub-hosted runners.
- Check the "Set up job" step for the logs of the last successful run to determine the runner.
- Rotate the GITHUB_TOKEN secret for the appropriate runners.

**Correct Answers:**
- **Review the contents of the Runner *.log files in the _diag folder.**
- **Check the "Set up job" step for the logs of the last successful run to determine the runner.**

**Supporting Statement:** Examining runner logs and the last successful run's setup can help identify issues like resource limitations or runner availability.

---

**Page 5 of 75**

**Question:** Scheduled workflows run on the:

**Options:**
- latest commit from the branch named main.
- latest commit on the default or base branch.
- latest commit and branch on which the workflow was triggered.
- latest commit from the branch named schedule.
- specified commit and branch from the workflow YAML file.

**Correct Answer:**
- **latest commit on the default or base branch.**

**Supporting Statement:** By default, scheduled workflows trigger on the latest commit of the default or base branch (usually 'main' or 'master').

---

**Page 6 of 75**

**Question:** You are a DevOps engineer working on a custom action. You want to conditionally run a script at the start of the action, before the main entrypoint. Which code block should be used to define the metadata file for your custom action?

**Options:**
- ```yaml
  runs:
    using: 'node16'
    pre: 'start.js'
    pre-if: github.event_name == 'push'
    main: 'index.js'
  ```

- ```yaml
  runs:
    using: 'node16'
    start: 'start.js'
    start-if: github.event_name == 'push'
    main: 'index.js'
  ```

**Correct Answer:**
- ```yaml
  runs:
    using: 'node16'
    pre: 'start.js'
    pre-if: github.event_name == 'push'
    main: 'index.js'
  ```

**Supporting Statement:** The `pre` section in the `runs` block is used to define a script that should run before the main entrypoint of the action, and the `pre-if` condition allows you to control when the script is executed.

---

**Page 7 of 75**

**Question:** How should you print a debug message in your workflow?

**Options:**
- `echo "Set variable MyVariable to true" >> $DEBUG_MESSAGE`
- `echo "::debug::Set variable myVariable to true"`
- `echo "debug_message=Set variable myVariable to true" >> $GITHUB_OUTPUT`
- `echo "::add-mask::Set variable myVariable to true"`

**Correct Answer:**
- `echo "::debug::Set variable myVariable to true"`

**Supporting Statement:** The `::debug::` prefix is the correct syntax for printing debug messages in GitHub Actions workflows.

---

**Page 8 of 75**

**Question:** Which choices represent best practices for publishing actions so that they can be consumed reliably? (Choose two)

**Options:**
- repo name
- organization name
- tag
- default branch
- commit SHA

**Correct Answers:**
- **tag**
- **default branch**

**Supporting Statement:** Tagging a specific commit or using the default branch provides a stable reference for consumers to use when referencing the action.

**Page 9 of 75**

---

**Question:** What is the simplest action type to run a shell script?

**Options:**
- Docker container action
- Composite action
- Bash script action
- JavaScript action

**Correct Answer:**
- **Bash script action**

**Supporting Statement:** A Bash script action is the most straightforward way to execute shell commands within a workflow.

---

**Page 10 of 75**

**Question:** Your organization needs to simplify reusing and maintaining automation in your GitHub Enterprise Cloud across all repositories. (Choose three)

**Options:**
- self-hosted runners
- actions stored in an organizational partition in the GitHub Marketplace
- custom Docker actions stored in GitHub Container Registry
- encrypted secrets
- actions stored in private repositories in the organization
- workflow templates

**Correct Answers:**
- **actions stored in an organizational partition in the GitHub Marketplace**
- **custom Docker actions stored in GitHub Container Registry**
- **actions stored in private repositories in the organization**

**Supporting Statement:** These options promote reusability by allowing you to share and manage actions centrally.

---

**Page 11 of 75**

**Question:** As a developer, which of the following snippets will enable you to run the commands `npm ci` and `npm run build` as part of a workflow?

**Options:**
- `run:`
  `  npm ci`
  `  npm run build`

- `shell:`
  `  npm ci`
  `  npm run build`

**Correct Answer:**
- `shell:`
  `  npm ci`
  `  npm run build`

**Supporting Statement:** The `shell:` keyword indicates that the following commands should be executed in a shell environment.

---

**Page 12 of 75**

**Question:** As a developer, you need to leverage Redis in your workflow. What is the best way to use Redis on a self-hosted runner without affecting future workflow runs?

**Options:**
- Specify `container:` and `services:` in your job definition to leverage a Redis service container.
- Add a run step to your workflow, which dynamically installs and configures Redis as part of your job.
- Set up Redis on a separate machine and reference that instance from your job.
- Install Redis on the hosted runner image and place it in a runner group. Specify `label:` in your job to target the runner group.

**Correct Answer:**
- **Specify `container:` and `services:` in your job definition to leverage a Redis service container.**

**Supporting Statement:** Using a service container ensures that Redis is available to your job without modifying the runner itself or requiring additional setup.

---

**Page 13 of 75**

**Question:** As a DevOps engineer, you need to execute a deployment to different environments like development and testing based on the labels added to a pull request. The deployment should use the `releases` branch and trigger only when there is a change in the files under `apps` folder. Which code block should be used to define the deployment workflow trigger?

**Options:**
- ```yaml
  on:
    pull_request:
      types: [labeled]
      branches:
        - 'releases'
      paths:
        - 'apps/**'
  ```

- ```yaml
  on:
    pull_request:
      types: [labeled]
      branches:
        - 'releases'
  ```

**Correct Answer:**
- ```yaml
  on:
    pull_request:
      types: [labeled]
      branches:
        - 'releases'
      paths:
        - 'apps/**'
  ```

**Supporting Statement:** This YAML block correctly defines the trigger to run the deployment workflow only when:
  * A pull request is labeled (indicated by `types: [labeled]`)
  * The pull request is targeting the `releases` branch
  * The changes in the pull request affect files within the `apps` directory (or any subdirectories within it, indicated by `paths: - 'apps/**'`)

---

**Page 14 of 75**

**Question:** In which locations can actions be referenced by workflows? (Choose three)

**Options:**
- the same repository as the workflow
- an action extension file in the repository
- the `runs-on:` keyword of a workflow file
- the repository's Secrets settings page
- a published Docker container image on Docker Hub
- a public NPM registry
- a separate public repository

**Correct Answers:**
- **the same repository as the workflow**
- **a published Docker container image on Docker Hub**
- **a separate public repository**

**Supporting Statement:** Actions can be referenced from:
  * The same repository where the workflow is defined.
  * A published Docker container image on Docker Hub.
  * A separate public repository containing the action.

---

**Page 15 of 75**

**Question:** What are the two ways to pass data between jobs? (Choose two)

**Options:**
- Use the copy action with restore parameter to restore the data from the cache.
- Use artifact storage.
- Use job outputs.
- Use data storage.
- Use the copy action to save the data that should be passed in the artifacts folder.
- Use the copy action with cache parameter to cache the data.

**Correct Answers:**
- **Use job outputs.**
- **Use artifact storage.**

**Supporting Statement:** 
  * Job outputs allow you to pass values or data generated by one job to subsequent jobs in the same workflow.
  * Artifact storage provides a persistent way to store and share files or data between jobs, even across different workflows.

---

**Page 16 of 75**

**Question:** In which scenarios could the GITHUB_TOKEN be used? (Choose two)

**Options:**
- to leverage a self-hosted runner
- to publish to GitHub Packages
- to create a repository secret
- to add a member to an organization
- to create issues in the repo
- to read from the file system on the runner

**Correct Answers:**
- **to publish to GitHub Packages**
- **to create issues in the repo**

**Supporting Statement:** The GITHUB_TOKEN can be used for actions that interact with GitHub APIs, such as publishing packages to GitHub Packages or creating issues in a repository.

---

**Page 17 of 75**

**Question:** You need to trigger a workflow using the GitHub API for activity that happens outside of GitHub.

**Options:**
- workflow_run
- repository_dispatch
- check_suite
- deployment

**Correct Answer:**
- **repository_dispatch**

**Supporting Statement:** The `repository_dispatch` event is specifically designed to trigger workflows from external sources using the GitHub API.

---

**Page 18 of 75**

**Question:** While writing a custom action, some behavior within the runner must be changed. Which commands can be used to influence the runner's output? (Choose two)

**Options:**
- `echo "::error file=main.py,line=10,col=15::There was an error"`
- `echo "::error=There was an error::"`
- `echo "::error::There was an error"`
- `echo "::error message=There was an error::"`

**Correct Answers:**
- `echo "::error file=main.py,line=10,col=15::There was an error"`
- `echo "::error message=There was an error::"`

**Supporting Statement:** The `::error::` prefix is used to display error messages in the runner's output. The first option provides additional context by specifying the file, line, and column where the error occurred.

---

**Page 19 of 75**

**Question:** You need to make a script to retrieve workflow run logs via the API. Which is the correct API to download a workflow run's logs?

**Options:**
- `GET /repos/:owner/:repo/actions/runs/:run_id/logs`
- `GET /repos/:owner/:repo/actions/artifacts/logs`
- `POST /repos/:owner/:repo/actions/runs/:run_id/logs`
- `POST /repos/:owner/:repo/actions/runs/:run_id`

**Correct Answer:**
- `GET /repos/:owner/:repo/actions/runs/:run_id/logs`

**Supporting Statement:** This endpoint is specifically designed to retrieve the logs for a given workflow run.

---

**Page 20 of 75**

**Question:** What is the most suitable action type for a custom action written in TypeScript?

**Options:**
- Docker container action
- Composite run step
- Bash script action
- JavaScript action

**Correct Answer:**
- **JavaScript action**

**Supporting Statement:** TypeScript is a superset of JavaScript, so a JavaScript action is the most appropriate choice for TypeScript code.

---

**Page 21 of 75**

**Question:** As a DevOps engineer, you need to define a deployment workflow that runs after the build workflow has completed. Without modifying the build workflow, which trigger should you define in the deployment workflow?

**Options:**
- workflow_dispatch
- workflow_run
- workflow_exec
- repository_dispatch

**Correct Answer:**
- **workflow_run**

**Supporting Statement:** The `workflow_run` trigger allows a workflow to be triggered when another workflow in the same repository completes successfully.

---

**Page 22 of 75**

**Question:** Custom environment variables can be defined at multiple levels within a workflow file including: (Choose three)

**Options:**
- runner level.
- step level.
- top level.
- job level.
- stage level.
- default level.

**Correct Answers:**
- **Job level.**
- **Step level.**
- **Top level.**

**Supporting Statement:** Environment variables can be defined at the top level of the workflow file, at the job level, or within individual steps.

---

**Page 23 of 75**

**Question:** As a developer, you are designing a workflow and need to communicate with the runner machine to set environment variables, add debug messages to the output logs, and other tasks. Which of the following options should be used?

**Options:**
- self-hosted runners
- composite run step
- environment variables
- enable debug logging
- workflow commands

**Correct Answer:**
- **workflow commands**

**Supporting Statement:** Workflow commands provide a way to interact with the runner machine and perform actions like setting environment variables and printing debug messages.

---

**Page 24 of 75**

**Question:** Which of the following statements are true regarding the use of GitHub Actions on a GitHub Enterprise Server? (Choose three)

**Options:**
- Actions must be defined in the .github repository.
- Actions created by GitHub are automatically available and cannot be disabled.
- Third-party actions can be used on GitHub Enterprise Server by configuring GitHub Connect.
- Use of GitHub Actions on GitHub Enterprise Server requires a persistent internet connection.
- Third-party actions can be manually synchronized for use on GitHub Enterprise Server.
- Most GitHub-authored actions are automatically bundled for use on GitHub Enterprise Server.

**Correct Answers:**
- **Actions must be defined in the .github repository.**
- **Third-party actions can be manually synchronized for use on GitHub Enterprise Server.**
- **Most GitHub-authored actions are automatically bundled for use on GitHub Enterprise Server.**

**Supporting Statement:** Actions on GitHub Enterprise Server are managed through the .github repository, and third-party actions require manual synchronization.

---

**Page 25 of 75**

**Question:** As a developer, you are optimizing a GitHub workflow that uses and produces many different files. You want to improve performance and reduce workflow run times versus workflow artifacts. Which two statements are true? (Choose two)

**Options:**
- Use artifacts to access the GitHub Package Registry and download a package for a workflow.
- Use artifacts when referencing files produced by a job after a workflow has ended.
- Use caching when reusing files that change rarely between jobs or workflow runs.
- Use caching to store cache entries for up to 30 days between accesses.

**Correct Answers:**
- **Use artifacts when referencing files produced by a job after a workflow has ended.**
- **Use caching when reusing files that change rarely between jobs or workflow runs.**

**Supporting Statement:** 
  * Artifacts are used to store and share files between jobs or even across workflows.
  * Caching helps improve performance by storing frequently used files and avoiding unnecessary downloads.

---

**Page 26 of 75**

**Question:** Which default GitHub environment variable indicates the name of the person or app that initiated a workflow run?

**Options:**
- GITHUB_ACTOR
- GITHUB_USER
- ENV_ACTOR
- GITHUB_WORKFLOW_ACTOR

**Correct Answer:**
- **GITHUB_ACTOR**

**Supporting Statement:** The `GITHUB_ACTOR` environment variable contains the name of the user or app that triggered the workflow run.

---

**Page 27 of 75**

**Question:** As a developer, one of your workflows will require Xcode version 11.2 on a hosted macOS Catalina (i.e., v10.15) runner. You've already created and configured a self-hosted runner to conform to those requirements and registered it with your organization. What else should you do to ensure that the workflow accesses the correct runner instance? (Choose three)

**Options:**
- Assign the custom labels to the self-hosted runner.
- In the workflow, specify:
  ```yaml
  runs-on: [ self-hosted, macos-10.15, xcode-11.2 ]
  ```
- Add your runner to the appropriate runner groups.
- Create custom runner labels for macos-10.15 and xcode-11.2.
- In the workflow, specify:
  ```yaml
  runs-on: [ ${{groups.macos-10.15}}, ${{groups.xcode-11.2}} ]
  ```
- Create runner groups named `macos-10.15` and `xcode-11.2`.

**Correct Answers:**
- **Assign the custom labels to the self-hosted runner.**
- **Add your runner to the appropriate runner groups.**
- **In the workflow, specify:**
  ```yaml
  runs-on: [ self-hosted, macos-10.15, xcode-11.2 ]
  ```

**Supporting Statement:** By assigning labels and adding the runner to groups, you can filter and select the correct runner instance based on its capabilities in the workflow definition.

---

**Page 28 of 75**

**Question:** You are a DevOps engineer working on deployment workflows. You need to execute the `deploy` job only if the current branch name is `feature-branch`. Which code snippet will help you to implement the conditional execution of the job?

**Options:**
- ```yaml
  jobs:
    deploy:
      if: github.ref_name == 'feature-branch'
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
  ```

- ```yaml
  jobs:
    deploy:
      if: github.branch_name == 'feature-branch'
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
  ```

**Correct Answer:**
- ```yaml
  jobs:
    deploy:
      if: github.ref_name == 'refs/heads/feature-branch'
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
  ```

**Supporting Statement:** The `if` condition checks the value of `github.ref_name`, which represents the full Git reference (e.g., `refs/heads/feature-branch`), to determine whether the job should run.

---

**Page 29 of 75**

**Question:** Which of the following is a valid reusable workflow reference?

**Options:**
- `uses: another-repo/.github/workflows/workflow.yml@v1`
- `uses: octo-org/another-repo/workflow.yml@v1`
- `uses: another-repo/workflow.yml@v1`
- `uses: octo-org/another-repo/.github/workflows/workflow.yml`

**Correct Answer:**
- `uses: another-repo/workflow.yml@v1`

**Supporting Statement:** This is the correct syntax for referencing a reusable workflow in another repository.

---

**Page 30 of 75**

**Question:** What are two reasons to keep an action in its own repository instead of bundling it with other application code? (Choose two)

**Options:**
- It widens the scope of the code base for developers fixing issues and extending the action.
- It decouples the action's versioning from the versioning of other application code.
- It allows sharing workflow secrets with other users.
- It makes the `action.yml` file optional.
- It makes it easier for the GitHub community to discover the action.

**Correct Answers:**
- **It decouples the action's versioning from the versioning of other application code.**
- **It makes it easier for the GitHub community to discover the action.**

**Supporting Statement:** Keeping an action in its own repository allows for independent versioning and makes it more discoverable by the GitHub community.

---

**Page 31 of 75**

**Question:** Which command can you include in your workflow file to set the output parameter for an action?

**Options:**
- `echo "::add-mask::ACTION_COLOR"`
- `echo "action_color=purple" >> $GITHUB_OUTPUT`
- `echo "::debug::action_color=purple"`
- `echo "action_color=purple" >> $GITHUB_ENV`

**Correct Answer:**
- `echo "action_color=purple" >> $GITHUB_OUTPUT`

**Supporting Statement:** This command writes the output parameter "action_color" with...

---

**Page 31 of 75**

**Question:** As a DevOps engineer, you have configured an IP allow list on a GitHub organization. Which effects does the IP allow list have on GitHub Actions? (Choose two)

**Options:**
- You must allow GitHub Actions's IP address ranges in order to use marketplace actions.
- You can use standard GitHub-hosted runners since their IP addresses are automatically allowed.
- You can use GitHub-hosted larger runners since they can be configured with static IP addresses.
- You can use self-hosted runners with known IP addresses.

**Correct Answers:**
- **You must allow GitHub Actions's IP address ranges in order to use marketplace actions.**
- **You can use self-hosted runners with known IP addresses.**

**Supporting Statement:** 
* Marketplace actions run on GitHub's infrastructure, so their IP addresses need to be allowed for communication.
* With self-hosted runners, you control the IP addresses, allowing you to add them explicitly to the allow list for security.

---

**Page 32 of 75**

**Question:** You installed specific software on a Linux self-hosted runner. You have users with workflows that need to be able to use this identified custom software. Which steps should you perform to prepare the runner and your users to run these workflows? (Choose two)

**Options:**
- Inform users to identify the runner based on the group.
- Create the group `custom-software-on-linux` and move the runner into the group.
- Inform users to identify the runner with the labels `custom-software` and `linux`.
- Configure the webhook and network to enable GitHub to trigger workflows.
- Add the label `custom-software` to the runner.
- Add the label `linux` to the runner.

**Correct Answers:**
- **Create the group `custom-software-on-linux` and move the runner into the group.**
- **Inform users to identify the runner based on the group.**

**Supporting Statement:** Organizing runners into groups based on their capabilities (like installed software) allows users to easily identify and select the appropriate runner for their workflows.

---

**Page 33 of 75**

**Question:** What is the proper syntax to reference the system-provided run number variable?

**Options:**
- `$GITHUB_RUN_NUMBER`
- `${{ GITHUB_RUN_NUMBER }}`
- `$github.run_number`
- `${{ env.GITHUB_RUN_NUMBER }}`
- `${{ var.GITHUB_RUN_NUMBER }}`

**Correct Answer:**
- `${{ GITHUB_RUN_NUMBER }}`

**Supporting Statement:** This is the correct syntax to access the value of the `GITHUB_RUN_NUMBER` environment variable within a workflow file.

---

**Page 34 of 75**

**Question:** What are the mandatory requirements for publishing GitHub Actions to the GitHub Marketplace? (Choose two)

**Options:**
- Each repository can contain a collection of actions as long as they are under the same Marketplace category.
- The action's name cannot match a user or organization on GitHub unless the user or organization owns the action.
- The action's metadata file must be in the root directory of the repository.
- The action can be either in a public or private repository.
- The name should match with one of the existing GitHub Marketplace categories.

**Correct Answers:**
- **The action's metadata file must be in the root directory of the repository.**
- **The action's name cannot match a user or organization on GitHub unless the user or organization owns the action.**

**Supporting Statement:** These are two of the essential requirements for publishing Actions to the Marketplace.

---

**Page 35 of 75**

**Question:** Which default environment variable specifies the branch or tag that triggered a workflow?

**Options:**
- `ENV_BRANCH`
- `GITHUB_BRANCH`
- `GITHUB_TAG`
- `GITHUB_REF`

**Correct Answer:**
- **GITHUB_REF**

**Supporting Statement:** The `GITHUB_REF` environment variable contains the full Git reference (e.g., `refs/heads/main`, `refs/tags/v1.0`) that triggered the workflow.

---

**Page 36 of 75**

**Question:** As a developer, you need to make sure that only actions from trusted sources are available for use in your GitHub Enterprise Cloud organization. (Choose three)

**Options:**
- Actions can be published to an internal marketplace.
- Actions created by GitHub are automatically enabled and cannot be disabled.
- GitHub-verified actions can be collectively enabled for use in the enterprise.
- Specific actions can individually be enabled for the organization, including version information.
- Individual third-party actions enabled with a specific tag will prevent updated versions of the action from introducing vulnerabilities.
- Actions can be restricted to only those available in the enterprise.

**Correct Answers:**
- **Actions can be published to an internal marketplace.**
- **GitHub-verified actions can be collectively enabled for use in the enterprise.**
- **Specific actions can individually be enabled for the organization, including version information.**

**Supporting Statement:** These options provide ways to control which actions are available within your organization, allowing you to prioritize trusted sources and manage access.

---

**Page 37 of 75**

**Question:** Disabling a workflow allows you to stop a workflow from being triggered without having to delete the file from the repo. In which of the following scenarios is disabling a workflow most useful? (Choose two)

**Options:**
- A workflow needs to be changed from running on a schedule to a manual trigger.
- A workflow error produces too many, or wrong, requests, impacting external services negatively.
- A workflow sends requests to a service that is down.
- A workflow is configured to run on self-hosted runners.
- A runner needs to have diagnostic logging enabled.

**Correct Answers:**
- **A workflow needs to be changed from running on a schedule to a manual trigger.**
- **A workflow error produces too many, or wrong, requests, impacting external services negatively.**

**Supporting Statement:** Disabling a workflow is useful when you need to temporarily stop its execution without making permanent changes to the workflow file. This is helpful for scenarios like switching to manual triggers or mitigating issues caused by errors.

---

**Page 38 of 75**

**Question:** Where should workflow files be stored to be triggered by events in a repository?

**Options:**
- .github/workflows/
- workflows/
- .github/actions/
- anywhere
- Nowhere; they must be attached to an action in the GitHub user interface.

**Correct Answer:**
- **.github/workflows/**

**Supporting Statement:** Workflow files must be placed in the `.github/workflows/` directory within the repository to be recognized and triggered by GitHub Actions.

---

**Page 39 of 75**

**Question:** What are the most significant advantages of adding documentation while distributing custom actions? (Choose two)

**Options:**
- It provides an example of the action.
- It shares the description of the action to the users.
- It generates auto completion when using the action in a workflow.
- It creates a `readme.md` for the consuming workflow.

**Correct Answers:**
- **It shares the description of the action to the users.**
- **It generates auto completion when using the action in a workflow.**

**Supporting Statement:** Documentation is crucial for users to understand how to use an action. It helps them understand its purpose, inputs, outputs, and usage examples, and can often enable IDEs to provide auto-completion suggestions when using the action.

---

**Page 40 of 75**

**Question:** Which files are required for a Docker container action in addition to the source code? (Choose two)

**Options:**
- Actionfile
- metadata.yml
- Dockerfile
- action.yml

**Correct Answers:**
- **Dockerfile**
- **action.yml**

**Supporting Statement:**
- The `Dockerfile` is essential for building the Docker image that will run the action.
- The `action.yml` file provides metadata about the action, such as inputs, outputs, and other configuration details.

---

**Page 41 of 75**

**Question:** Which of the following is the most common way to target a specific major release version?

**Options:**
- ```
  steps:
    - uses: actions/checkout
  ```
- ```
  steps:
    - uses: actions/checkout@v3
  ```
- ```
  steps:
    - uses: actions/checkout@011673995124
  ```
- ```
  steps:
    - uses: actions/checkout@ac939985615ec5ede59e132de21d2eb1cbd6121c
  ```

**Correct Answer:**
- ```
  steps:
    - uses: actions/checkout@v3
  ```

**Supporting Statement:** Using a major version number (like `@v3`) in the action reference targets the latest stable release within that major version. This allows you to receive updates and bug fixes within the major version while maintaining compatibility.

---

**Page 42 of 75**

**Question:** In the following workflow file, line 5 interprets lines 3 and 4 as Python. Which of the following is a valid option to complete line 5?

```yaml
1 steps:
2   - run: |
3     import os
4     print(os.environ['PATH'])
5 
```

**Options:**
- `shell: bash`
- `with: python`
- `working-directory: .github/python`
- `shell: python`

**Correct Answer:**
- `shell: python`

**Supporting Statement:** Since lines 3 and 4 contain Python code, specifying `shell: python` on line 5 tells the runner to interpret those lines as Python commands.

---

**Page 43 of 75**

**Question:** What is a valid scenario regarding environment secrets?

**Options:**
- ensuring only a specific step can access an environment secret
- configuring environment secrets to automatically pull from Azure Key Vault
- configuring environment secrets for connecting to GitHub Enterprise Server
- ensuring a job cannot access environment secrets until approval is obtained from a required reviewer

**Correct Answer:**
- **ensuring only a specific step can access an environment secret**

**Supporting Statement:** This scenario demonstrates a valid use case for controlling access to sensitive information within a workflow.

---

**Page 44 of 75**

**Question:** By default, which workflows can use an action stored in an internal repository? (Choose two)

**Options:**
- public repositories owned by the same organization as the enterprise
- internal repositories owned by the same organization as the enterprise
- private repositories owned by an organization of the enterprise
- selected public repositories outside of the enterprise

**Correct Answers:**
- **internal repositories owned by the same organization as the enterprise**
- **private repositories owned by an organization of the enterprise**

**Supporting Statement:** By default, workflows within an enterprise can access actions stored in internal repositories (private or internal) owned by organizations belonging to the same enterprise.

---

**Page 45 of 75**

**Question:** You are a DevOps engineer in ABC Corp. You need to schedule your deployment workflow twice a week at 7:45 AM on Wednesday and Saturday. What is the appropriate YAML structure?

**Options:**
- ```yaml
  on:
    cron: '45 7 * * 3,6'
  ```
- ```yaml
  on:
    cron:
      - schedule: '45 7 * * 3,6'
  ```
- ```yaml
  schedule: '45 7 * * 3,6'
  ```
- ```yaml
  on:
    schedule:
      - cron: '45 7 * * 3,6'
  ```

**Correct Answer:**
- ```yaml
  on:
    schedule:
      - cron: '45 7 * * 3,6'
  ```

**Supporting Statement:** This YAML structure correctly defines a cron schedule to trigger the workflow at 7:45 AM on Wednesdays and Saturdays.

---

**Page 46 of 75**

**Question:** You are reaching your organization's storage limit for GitHub artifacts and packages. What should you do to prevent the storage limit from being reached? (Choose two)

**Options:**
- Disable branch protections in the repository.
- Use self-hosted runners for all workflow runs.
- Configure the repo to use Git Large File Storage.
- Delete artifacts from the repositories manually.
- Configure the artifact and log retention period.

**Correct Answers:**
- **Configure the repo to use Git Large File Storage.**
- **Configure the artifact and log retention period.**

**Supporting Statement:** 
  * Git Large File Storage (LFS) stores large files outside the main repository, reducing storage usage.
  * Configuring retention periods for artifacts and logs helps automatically delete old data, freeing up space.

---

**Page 47 of 75**

**Question:** As a developer, you have configured an IP allow list on a GitHub organization. Which effects does the IP allow list have on GitHub Actions? (Choose two)

**Options:**
- You must allow GitHub Actions's IP address ranges in order to use marketplace actions.
- You can use standard GitHub-hosted runners since their IP addresses are automatically allowed.
- You can use GitHub-hosted larger runners since they can be configured with static IP addresses.
- You can use self-hosted runners with known IP addresses.

**Correct Answers:**
- **You must allow GitHub Actions's IP address ranges in order to use marketplace actions.**
- **You can use self-hosted runners with known IP addresses.**

**Supporting Statement:** 
* Marketplace actions run on GitHub's infrastructure, so their IP addresses need to be allowed for communication.
* With self-hosted runners, you control the IP addresses, allowing you to add them explicitly to the allow list for security.

---

**Page 48 of 75**

**Question:** What is the proper syntax to reference the system-provided run number variable?

**Options:**
- `$GITHUB_RUN_NUMBER`
- `${{ GITHUB_RUN_NUMBER }}`
- `$github.run_number`
- `${{ env.GITHUB_RUN_NUMBER }}`
- `${{ var.GITHUB_RUN_NUMBER }}`

**Correct Answer:**
- `${{ GITHUB_RUN_NUMBER }}`

**Supporting Statement:** This is the correct syntax to access the value of the `GITHUB_RUN_NUMBER` environment variable within a workflow file.

---

**Page 49 of 75**

**Question:** What are the mandatory requirements for publishing GitHub Actions to the GitHub Marketplace? (Choose two)

**Options:**
- Each repository can contain a collection of actions as long as they are under the same Marketplace category.
- The action's name cannot match a user or organization on GitHub unless the user or organization owns the action.
- The action's metadata file must be in the root directory of the repository.
- The action can be either in a public or private repository.
- The name should match with one of the existing GitHub Marketplace categories.

**Correct Answers:**
- **The action's metadata file must be in the root directory of the repository.**
- **The action's name cannot match a user or organization on GitHub unless the user or organization owns the action.**

**Supporting Statement:** These are two of the essential requirements for publishing Actions to the Marketplace.

---

**Page 50 of 75**

**Question:** Which default environment variable specifies the branch or tag that triggered a workflow?

**Options:**
- `ENV_BRANCH`
- `GITHUB_BRANCH`
- `GITHUB_TAG`
- `GITHUB_REF`

**Correct Answer:**
- **GITHUB_REF**

**Supporting Statement:** The `GITHUB_REF` environment variable contains the full Git reference (e.g., `refs/heads/main`, `refs/tags/v1.0`) that triggered the workflow.

---

**Page 51 of 75**

**Question:** As a developer, you are optimizing a GitHub workflow that uses and produces many different files. You want to improve performance and reduce workflow run times versus workflow artifacts. Which two statements are true? (Choose two)

**Options:**
- Use artifacts to access the GitHub Package Registry and download a package for a workflow.
- Use artifacts when referencing files produced by a job after a workflow has ended.
- Use caching when reusing files that change rarely between jobs or workflow runs.
- Use caching to store cache entries for up to 30 days between accesses.

**Correct Answers:**
- **Use artifacts when referencing files produced by a job after a workflow has ended.**
- **Use caching when reusing files that change rarely between jobs or workflow runs.**

**Supporting Statement:** 
  * Artifacts are used to store and share files between jobs or even across workflows.
  * Caching helps improve performance by storing frequently used files and avoiding unnecessary downloads.

---

**Page 52 of 75**

**Question:** Which default GitHub environment variable indicates the name of the person or app that initiated a workflow run?

**Options:**
- GITHUB_ACTOR
- GITHUB_USER
- ENV_ACTOR
- GITHUB_WORKFLOW_ACTOR

**Correct Answer:**
- **GITHUB_ACTOR**

**Supporting Statement:** The `GITHUB_ACTOR` environment variable contains the name of the user or app that triggered the workflow run.

---

**Page 53 of 75**

**Question:** As a developer, one of your workflows will require Xcode version 11.2 on a hosted macOS Catalina (i.e., v10.15) runner. You've already created and configured a self-hosted runner to conform to those requirements and registered it with your organization. What else should you do to ensure that the workflow accesses the correct runner instance? (Choose three)

**Options:**
- Assign the custom labels to the self-hosted runner.
- In the workflow, specify:
  ```yaml
  runs-on: [ self-hosted, macos-10.15, xcode-11.2 ]
  ```
- Add your runner to the appropriate runner groups.
- Create custom runner labels for macos-10.15 and xcode-11.2.
- In the workflow, specify:
  ```yaml
  runs-on: [ ${{groups.macos-10.15}}, ${{groups.xcode-11.2}} ]
  ```
- Create runner groups named `macos-10.15` and `xcode-11.2`.

**Correct Answers:**
- **Assign the custom labels to the self-hosted runner.**
- **Add your runner to the appropriate runner groups.**
- **In the workflow, specify:**
  ```yaml
  runs-on: [ self-hosted, macos-10.15, xcode-11.2 ]
  ```

**Supporting Statement:** By assigning labels and adding the runner to groups, you can filter and select the correct runner instance based on its capabilities in the workflow definition.

---

**Page 54 of 75**

**Question:** You are a DevOps engineer working on deployment workflows. You need to execute the `deploy` job only if the current branch name is `feature-branch`. Which code snippet will help you to implement the conditional execution of the job?

**Options:**
- ```yaml
  jobs:
    deploy:
      if: github.ref_name == 'feature-branch'
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
  ```
- ```yaml
  jobs:
    deploy:
      if: github.branch_name == 'feature-branch'
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
  ```

**Correct Answer:**
- ```yaml
  jobs:
    deploy:
      if: github.ref_name == 'refs/heads/feature-branch'
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
  ```

**Supporting Statement:** The `if` condition checks the value of `github.ref_name`, which represents the full Git reference (e.g., `refs/heads/feature-branch`), to determine whether the job should run.

---

**Page 55 of 75**

**Question:** Which of the following is a valid reusable workflow reference?

**Options:**
- `uses: another-repo/.github/workflows/workflow.yml@v1`
- `uses: octo-org/another-repo/workflow.yml@v1`
- `uses: another-repo/workflow.yml@v1`
- `uses: octo-org/another-repo/.github/workflows/workflow.yml`

**Correct Answer:**
- `uses: another-repo/workflow.yml@v1`

**Supporting Statement:** This is the correct syntax for referencing a reusable workflow in another repository.

---

**Page 56 of 75**

**Question:** What are two reasons to keep an action in its own repository instead of bundling it with other application code? (Choose two)

**Options:**
- It widens the scope of the code base for developers fixing issues and extending the action.
- It decouples the action's versioning from the versioning of other application code.
- It allows sharing workflow secrets with other users.
- It makes the `action.yml` file optional.
- It makes it easier for the GitHub community to discover the action.

**Correct Answers:**
- **It decouples the action's versioning from the versioning of other application code.**
- **It makes it easier for the GitHub community to discover the action.**

**Supporting Statement:** Keeping an action in its own repository allows for independent versioning and makes it more discoverable by the GitHub community.

---

**Page 57 of 75**

**Question:** Which command can you include in your workflow file to set the output parameter for an action?

**Options:**
- `echo "::add-mask::ACTION_COLOR"`
- `echo "action_color=purple" >> $GITHUB_OUTPUT`
- `echo "::debug::action_color=purple"`
- `echo "action_color=purple" >> $GITHUB_ENV`

**Correct Answer:**
- `echo "action_color=purple" >> $GITHUB_OUTPUT`

**Supporting Statement:** This command writes the output parameter "action_color" with the value "purple" to the `$GITHUB_OUTPUT` file, making it available to subsequent steps or other actions.

---

**Page 58 of 75**

**Question:** As a developer, you are configuring GitHub Actions to deploy VMs to production. A member of the VM Ops team must provide approval before deployment occurs. Which of the following steps should you take? (Choose two)

**Options:**
- Navigate to the repository settings and create a Production environment with the VM Ops team as a required reviewer.
- Navigate to the organization settings and create a Production environment with the VM Ops team as a required reviewer.
- Add the VMs to the environment.
- Specify the VM Ops team as the owner of the environment.
- Specify the environment named Production in the workflow jobs that deploy to the VMs.

**Correct Answers:**
- **Navigate to the organization settings and create a Production environment with the VM Ops team as a required reviewer.**
- **Specify the environment named Production in the workflow jobs that deploy to the VMs.**

**Supporting Statement:** 
* Creating a production environment with required reviewers in the organization settings allows for centralized management of deployment approvals.
* Specifying the environment in the workflow jobs ensures that the deployment process is subject to the approval requirements.

---

**Page 59 of 75**

**Question:** As a developer, you need to use GitHub Actions to deploy a microservice that requires runtime access to a secure token used by a variety of other microservices managed by different teams in different repos. To minimize management overhead and ensure the token is secure, which mechanisms should you use and access the token? (Choose two)

**Options:**
- Store the token as an organizational-level encrypted secret in GitHub. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.
- Store the token in a configuration file in a private repository. Use GitHub Actions to deploy the configuration file to the runtime environment.
- Store the token as a GitHub encrypted secret in the same repo as the code. Create a reusable custom GitHub Action to access the token by the microservice at runtime.
- Use a corporate non-GitHub secret store (e.g., Hash Corp Vault) to store the token. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.
- Store the token as a GitHub encrypted secret in the same repo as the code. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.

**Correct Answers:**
- **Store the token as an organizational-level encrypted secret in GitHub. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.**
- **Use a corporate

---

**Page 60 of 75**

**Question:** As a developer, you need to use GitHub Actions to deploy a microservice that requires runtime access to a secure token used by a variety of other microservices managed by different teams in different repos. To minimize management overhead and ensure the token is secure, which mechanisms should you use and access the token? (Choose two)

**Options:**
- Store the token as an organizational-level encrypted secret in GitHub. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.
- Store the token in a configuration file in a private repository. Use GitHub Actions to deploy the configuration file to the runtime environment.
- Store the token as a GitHub encrypted secret in the same repo as the code. Create a reusable custom GitHub Action to access the token by the microservice at runtime.
- Use a corporate non-GitHub secret store (e.g., Hash Corp Vault) to store the token. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.
- Store the token as a GitHub encrypted secret in the same repo as the code. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.

**Correct Answers:**
- **Store the token as an organizational-level encrypted secret in GitHub. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.**
- **Use a corporate non-GitHub secret store (e.g., Hash Corp Vault) to store the token. During deployment, use GitHub Actions to store the secret in an environment variable that can be accessed at runtime.**

**Supporting Statement:** 
* Storing the token at the organizational level provides central management and control.
* Using a dedicated secret store like Hashicorp Vault offers enhanced security and centralized management for sensitive information.

---

**Page 61 of 75**

**Question:** You installed specific software on a Linux self-hosted runner. You have users with workflows that need to be able to use this identified custom software. Which steps should you perform to prepare the runner and your users to run these workflows? (Choose two)

**Options:**
- Inform users to identify the runner based on the group.
- Create the group `custom-software-on-linux` and move the runner into the group.
- Inform users to identify the runner with the labels `custom-software` and `linux`.
- Configure the webhook and network to enable GitHub to trigger workflows.
- Add the label `custom-software` to the runner.
- Add the label `linux` to the runner.

**Correct Answers:**
- **Create the group `custom-software-on-linux` and move the runner into the group.**
- **Inform users to identify the runner based on the group.**

**Supporting Statement:** Organizing runners into groups based on their capabilities (like installed software) allows users to easily identify and select the appropriate runner for their workflows.

---

**Page 62 of 75**

**Question:** What is the proper syntax to reference the system-provided run number variable?

**Options:**
- `$GITHUB_RUN_NUMBER`
- `${{ GITHUB_RUN_NUMBER }}`
- `$github.run_number`
- `${{ env.GITHUB_RUN_NUMBER }}`
- `${{ var.GITHUB_RUN_NUMBER }}`

**Correct Answer:**
- `${{ GITHUB_RUN_NUMBER }}`

**Supporting Statement:** This is the correct syntax to access the value of the `GITHUB_RUN_NUMBER` environment variable within a workflow file.

---

**Page 63 of 75**

**Question:** What are the mandatory requirements for publishing GitHub Actions to the GitHub Marketplace? (Choose two)

**Options:**
- Each repository can contain a collection of actions as long as they are under the same Marketplace category.
- The action's name cannot match a user or organization on GitHub unless the user or organization owns the action.
- The action's metadata file must be in the root directory of the repository.
- The action can be either in a public or private repository.
- The name should match with one of the existing GitHub Marketplace categories.

**Correct Answers:**
- **The action's metadata file must be in the root directory of the repository.**
- **The action's name cannot match a user or organization on GitHub unless the user or organization owns the action.**

**Supporting Statement:** These are two of the essential requirements for publishing Actions to the Marketplace.

---

**Page 64 of 75**

**Question:** Which default environment variable specifies the branch or tag that triggered a workflow?

**Options:**
- `ENV_BRANCH`
- `GITHUB_BRANCH`
- `GITHUB_TAG`
- `GITHUB_REF`

**Correct Answer:**
- **GITHUB_REF**

**Supporting Statement:** The `GITHUB_REF` environment variable contains the full Git reference (e.g., `refs/heads/main`, `refs/tags/v1.0`) that triggered the workflow.

---

**Page 65 of 75**

**Question:** As a developer, you need to make sure that only actions from trusted sources are available for use in your GitHub Enterprise Cloud organization. (Choose three)

**Options:**
- Actions can be published to an internal marketplace.
- Actions created by GitHub are automatically enabled and cannot be disabled.
- GitHub-verified actions can be collectively enabled for use in the enterprise.
- Specific actions can individually be enabled for the organization, including version information.
- Individual third-party actions enabled with a specific tag will prevent updated versions of the action from introducing vulnerabilities.
- Actions can be restricted to only those available in the enterprise.

**Correct Answers:**
- **Actions can be published to an internal marketplace.**
- **GitHub-verified actions can be collectively enabled for use in the enterprise.**
- **Specific actions can individually be enabled for the organization, including version information.**

**Supporting Statement:** These options provide ways to control which actions are available within your organization, allowing you to prioritize trusted sources and manage access.

---

**Page 66 of 75**

**Question:** Disabling a workflow allows you to stop a workflow from being triggered without having to delete the file from the repo. In which of the following scenarios is disabling a workflow most useful? (Choose two)

**Options:**
- A workflow needs to be changed from running on a schedule to a manual trigger.
- A workflow error produces too many, or wrong, requests, impacting external services negatively.
- A workflow sends requests to a service that is down.
- A workflow is configured to run on self-hosted runners.
- A runner needs to have diagnostic logging enabled.

**Correct Answers:**
- **A workflow needs to be changed from running on a schedule to a manual trigger.**
- **A workflow error produces too many, or wrong, requests, impacting external services negatively.**

**Supporting Statement:** Disabling a workflow is useful when you need to temporarily stop its execution without making permanent changes to the workflow file. This is helpful for scenarios like switching to manual triggers or mitigating issues caused by errors.

---

**Page 67 of 75**

**Question:** Where should workflow files be stored to be triggered by events in a repository?

**Options:**
- .github/workflows/
- workflows/
- .github/actions/
- anywhere
- Nowhere; they must be attached to an action in the GitHub user interface.

**Correct Answer:**
- **.github/workflows/**

**Supporting Statement:** Workflow files must be placed in the `.github/workflows/` directory within the repository to be recognized and triggered by GitHub Actions.

---

**Page 68 of 75**

**Question:** What are the most significant advantages of adding documentation while distributing custom actions? (Choose two)

**Options:**
- It provides an example of the action.
- It shares the description of the action to the users.
- It generates auto completion when using the action in a workflow.
- It creates a `readme.md` for the consuming workflow.

**Correct Answers:**
- **It shares the description of the action to the users.**
- **It generates auto completion when using the action in a workflow.**

**Supporting Statement:** Documentation is crucial for users to understand how to use an action. It helps them understand its purpose, inputs, outputs, and usage examples, and can often enable IDEs to provide auto-completion suggestions when using the action.

---

**Page 69 of 75**

**Question:** Which files are required for a Docker container action in addition to the source code? (Choose two)

**Options:**
- Actionfile
- metadata.yml
- Dockerfile
- action.yml

**Correct Answers:**
- **Dockerfile**
- **action.yml**

**Supporting Statement:**
- The `Dockerfile` is essential for building the Docker image that will run the action.
- The `action.yml` file provides metadata about the action, such as inputs, outputs, and other configuration details.

---

**Page 70 of 75**

**Question:** Which of the following is the most common way to target a specific major release version?

**Options:**
- ```
  steps:
    - uses: actions/checkout
  ```
- ```
  steps:
    - uses: actions/checkout@v3
  ```
-

---

**Page 70 of 75**

**Question:** In the following workflow file, line 5 interprets lines 3 and 4 as Python. Which of the following is a valid option to complete line 5?

```yaml
1 steps:
2   - run: |
3     import os
4     print(os.environ['PATH'])
5 
```

**Options:**
- `shell: bash`
- `with: python`
- `working-directory: .github/python`
- `shell: python`

**Correct Answer:**
- `shell: python`

**Supporting Statement:** Since lines 3 and 4 contain Python code, specifying `shell: python` on line 5 tells the runner to interpret those lines as Python commands.

---

**Page 71 of 75**

**Question:** What is a valid scenario regarding environment secrets?

**Options:**
- ensuring only a specific step can access an environment secret
- configuring environment secrets to automatically pull from Azure Key Vault
- configuring environment secrets for connecting to GitHub Enterprise Server
- ensuring a job cannot access environment secrets until approval is obtained from a required reviewer

**Correct Answer:**
- **ensuring only a specific step can access an environment secret**

**Supporting Statement:** This scenario demonstrates a valid use case for controlling access to sensitive information within a workflow.

---

**Page 72 of 75**

**Question:** By default, which workflows can use an action stored in an internal repository? (Choose two)

**Options:**
- public repositories owned by the same organization as the enterprise
- internal repositories owned by the same organization as the enterprise
- private repositories owned by an organization of the enterprise
- selected public repositories outside of the enterprise

**Correct Answers:**
- **internal repositories owned by the same organization as the enterprise**
- **private repositories owned by an organization of the enterprise**

**Supporting Statement:** By default, workflows within an enterprise can access actions stored in internal repositories (private or internal) owned by organizations belonging to the same enterprise.

---

**Page 73 of 75**

**Question:** You are a DevOps engineer in ABC Corp. You need to schedule your deployment workflow twice a week at 7:45 AM on Wednesday and Saturday. What is the appropriate YAML structure?

**Options:**
- ```yaml
  on:
    cron: '45 7 * * 3,6'
  ```
- ```yaml
  on:
    cron:
      - schedule: '45 7 * * 3,6'
  ```
- ```yaml
  schedule: '45 7 * * 3,6'
  ```
- ```yaml
  on:
    schedule:
      - cron: '45 7 * * 3,6'
  ```

**Correct Answer:**
- ```yaml
  on:
    schedule:
      - cron: '45 7 * * 3,6'
  ```

**Supporting Statement:** This YAML structure correctly defines a cron schedule to trigger the workflow at 7:45 AM on Wednesdays and Saturdays.

---

**Page 74 of 75**

**Question:** You are reaching your organization's storage limit for GitHub artifacts and packages. What should you do to prevent the storage limit from being reached? (Choose two)

**Options:**
- Disable branch protections in the repository.
- Use self-hosted runners for all workflow runs.
- Configure the repo to use Git Large File Storage.
- Delete artifacts from the repositories manually.
- Configure the artifact and log retention period.

**Correct Answers:**
- **Configure the repo to use Git Large File Storage.**
- **Configure the artifact and log retention period.**

**Supporting Statement:** 
  * Git Large File Storage (LFS) stores large files outside the main repository, reducing storage usage.
  * Configuring retention periods for artifacts and logs helps automatically delete old data, freeing up space.

---

**Page 75 of 75**

**Question:** As a developer, you have configured an IP allow list on a GitHub organization. Which effects does the IP allow list have on GitHub Actions? (Choose two)

**Options:**
- You must allow GitHub Actions's IP address ranges in order to use marketplace actions.
- You can use standard GitHub-hosted runners since their IP addresses are automatically allowed.
- You can use GitHub-hosted larger runners since they can be configured with static IP addresses.
- You can use self-hosted runners with known IP addresses.

**Correct Answers:**
- **You must allow GitHub Actions's IP address ranges in order to use marketplace actions.**
- **You can use self-hosted runners with known IP addresses.**

**Supporting Statement:** 
* Marketplace actions run on GitHub's infrastructure, so their IP addresses need to be allowed for communication.
* With self-hosted runners, you control the IP addresses, allowing you to add them explicitly to the allow list for security. 

