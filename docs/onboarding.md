# Welcome to GitHub Actions on Power, Z, and LinuxONE

You can only install the GitHub Actions App on repositories (aka repos) in which you are the owner. This includes repos in an organization. Read more about personal repo access in the [GitHub official docs.](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-user-account-settings/permission-levels-for-a-personal-account-repository) Read more about repo permissions in organizations on [the official GitHub docs.](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization)


## Steps to install

### 1. Install the GitHub App on the repo

Please [submit a new issue](https://github.com/IBM/actionspz/issues) on this repo to access GitHub Actions on Power and Z.

### 2. Create an IBMid

***The IBMid needs to be the same email address you use for your GitHub account.*** This step is part of the GitHub App installation process, you will be redirected to the proper page. [Read more about the IBMid here.](https://www.ibm.com/docs/en/ibmid?topic=introduction)


### 3. Setup your workflow file
After the app is installed on the repo, specify the proper runner in your YAML workflow file: 

```yaml
runs-on: ubuntu-xxx-s390x
runs-on: ubuntu-xxx-ppc64le
```

These runners are considered self-hosted. Read more about self-hosted runners on [the official GitHub docs.](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/using-self-hosted-runners-in-a-workflow)

### 4. Use the Actions tab under the repo 

Just like any other workflow, the Actions tab can be used to manage triggers, run the Workflow manually, and view the runners' output.


Any questions? Read more on our [FAQ page](./FAQ.md) located in this repo.
