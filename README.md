# Auto-Push

Auto-Push is designed to enhance your GitHub activity by using GitHub Actions to make daily commits. This project automatically adds a timestamped log entry to a file called daily-log.txt every 12 hours. As a result, your commit history remains consistent and active. It’s perfect for anyone looking to keep their GitHub profile lively or to automate repetitive tasks in their repositories.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Running Tests](#running-tests)
- [License](#license)
- [Authors](#authors)

## Prerequisites

Before you begin, ensure you have the following:

- A GitHub account.
- A repository created on GitHub where you want to implement this automation.
- Basic understanding of Git and GitHub.

## Setup Instructions

Follow these steps to set up the auto-push workflow:

### 1. Create a New Repository

1. Go to [GitHub](https://github.com/) and log in to your account.
2. Click on the **New** button to create a new repository.
3. Name your repository (e.g., `auto-push`) and initialize it with a README file.
4. Click on **Create repository**.

### 2. Set Repository Permissions

1. Go to your repository settings by clicking on the **Settings** tab.
2. Scroll down to the **Actions** section on the left sidebar.
3. Under **Actions permissions**, ensure that **Allow all actions and reusable workflows** is selected. This setting allows the GitHub Actions workflow to have the necessary permissions to read and write to your repository.

### 3. Create a Workflow Directory

1. In your new repository, create a directory called `.github/workflows`.
2. This is where you'll store your GitHub Actions workflow files.

### 4. Add the Workflow File

1. Inside the `.github/workflows` directory, create a new file named `twice-daily-commit.yml`.
2. Navigate to my repo [nycanshu/auto-push](https://github.com/nycanshu/auto-push) and copy the YAML code from the `twice-daily-commit.yml` file.
3. Paste the copied code into your `twice-daily-commit.yml` file.

### 5. Push Your Changes

1. Add and commit the workflow file to your repository:

   ```bash
   git add .github/workflows/twice-daily-commit.yml
   git commit -m "Add GitHub Actions workflow for daily commits"
   git push origin main
## Running Tests

To verify that the workflow is working as expected, you can follow these steps:

1. **Check GitHub Actions Log:**
   - After pushing your changes to the repository, go to the **Actions** tab in your GitHub repository.
   - Select the latest workflow run for your `twice-daily-commit.yml` file.
   - Review the logs to see if the workflow executed successfully. Look for any error messages in case something went wrong.

2. **Run Workflow Manually:**
   - You can manually trigger the workflow to ensure it’s functioning as intended.
   - Go to the **Actions** tab, select the workflow file, and look for the **Run workflow** button. This option lets you initiate a run without waiting for the scheduled time.
   - **Note**: To manually trigger workflows, you may need to add the following line under `on:` in your workflow file:
     ```yaml
     workflow_dispatch:
     ```
     This line allows you to manually trigger the workflow using the **Run workflow** button in the GitHub Actions tab.

3. **Verify Changes in Repository:**
   - Check if the `daily-log.txt` file was updated with the latest timestamp.
   - Confirm that the changes have been committed with the correct commit message format (e.g., `auto-commit-2024-11-03`).

4. **Troubleshoot Issues:**
   - If the workflow fails, review the error logs in the Actions tab. Common issues include permission errors, syntax errors in the workflow file, or misconfigured secrets.


## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/nycanshu/auto-push/blob/main/LICENSE.md) file for details.


## Authors
**Contact owner for any doubt or clearification**

- [Himanshu](https://www.linkedin.com/in/okay-anshu/)
- [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/okay-anshu/)
