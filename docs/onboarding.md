# Welcome to GitHub Actions on Power, Z, and LinuxONE

You can only install the GitHub Actions App on repositories (aka repos) in which you are the owner or admin. If the repo is part of a GitHub Organization, the org admin can select specific repos for installation (or all the repos). A repo admin/owner can install the app on the repo they have permissions for, even if it's part of an organization. Read more about GitHub App installations on the [official GitHub website.](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/differences-between-github-apps-and-oauth-apps#who-can-install-github-apps-and-authorize-oauth-apps)

Read more about personal repo access in the [GitHub official docs.](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-user-account-settings/permission-levels-for-a-personal-account-repository) Read more about repo permissions in organizations on [the official GitHub docs.](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization)

[Read our criteria doc here.](./criteria.md)

## Steps to install

### 1. Install the GitHub App on the repo

Please [submit a new issue](https://github.com/IBM/actionspz/issues) on this repo to access GitHub Actions on Power and Z.

Read more about [using GitHub Apps.](https://docs.github.com/en/apps/using-github-apps/about-using-github-apps)

### 2. Create an IBMid

***The IBMid needs to be the same email address you use for your GitHub account.*** This step is part of the GitHub App installation process, you will be redirected to the proper page. [Read more about the IBMid here.](https://www.ibm.com/docs/en/ibmid?topic=introduction)

### 3. Configure Organization & Repository Settings

To ensure workflows run correctly—especially for public repositories and forks—Organization Admins and Repository Owners must update the following settings.

#### **For Organization Admins: Update Runner Groups**

1. Navigate to **Organization Settings** > **Actions** > **Runner groups**.
2. Select the **Default** group.
3. Update the following settings:

- [ ] Check  **"Allow public repositories"**  to enable it. (This is necessary to allow forks of repositories to execute CI workflows via Pull Requests.)
- [ ] Ensure  **"Repository access"**  is set to  **"All repositories"**  (or verify the specific repositories are included in the "Selected repositories" list).

#### **Enable Approval for Fork Pull Requests (Optional, but Recommended)**

To require approval before running GitHub Actions CI when a PR is raised from a fork, adjust the settings below at the Repository or Organization level.

**Repository Level**

1. Go to your **Repository**.
2. Click **Settings** (top tabs).
3. In the left sidebar, click **Actions** > **General**.
4. Scroll to  **"Approval for running fork pull request workflows from contributors"** .
5. Select **Require approval for all external contributors**.

**Organization Level**

1. Go to your **Organization** profile page.
2. Click **Settings** (top tabs).
3. In the left sidebar, click **Actions** > **General**.
4. Scroll to  **"Approval for running fork pull request workflows from contributors"** .
5. Select **Require approval for all external contributors**.

### 4. Setup your workflow file

After the app is installed on the repo and settings are configured, specify the proper runner in your YAML workflow file:

```yaml
runs-on: ubuntu-xxx-s390x
runs-on: ubuntu-xxx-ppc64le
```

View a list of our [supported images](./supported-images.txt) in this repo.

These runners are considered self-hosted. Read more about self-hosted runners on [the official GitHub docs.](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/using-self-hosted-runners-in-a-workflow)

### 5. Use the Actions tab under the repo

Just like any other workflow, the Actions tab can be used to manage triggers, run the Workflow manually, and view the runners' output.


Any questions? Read more on our [FAQ page](./FAQ.md) located in this repo.
