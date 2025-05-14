# Welcome To Github Actions on Power, Z, and LinuxONE

You can only install the Github Actions App on repositories (aka repos) in which you are the Owner. This includes repos in an Organization. Read more about personal repo access in the [Github official docs.](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-user-account-settings/permission-levels-for-a-personal-account-repository) Read more about repo permissions in Organizations on [the official Github docs.](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization)


## Steps to install

### 1. Install the Github App on the repo

[The app is located here.](https://github.com/apps/power-z-gha-runner/) The Github interface will guide you through the steps.

### 2. Create an IBMid

***The IBMid needs to be the same email address you use for your Github account.*** This step is part of the Github App installation process, you will be redirected to the proper page. [Read more about the IBMid here.](https://www.ibm.com/docs/en/ibmid?topic=introduction)


### 3. Setup your workfow file
After the app is installed on the repo, specify the proper runner in your YAML workflow file: 

```yaml
runs-on: ubuntu-xxx-s390x
runs-on: ubuntu-xxx-ppc64le
```

These runners are considerd self-hosted runners. Read more about self-hosted runners on [the official Github docs.](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/using-self-hosted-runners-in-a-workflow)

### 4. Use the Actions tab under the repo 

Just like any other workflow, the Actions tab can be used to manage triggers, manually run the Workflow, and read the output of the runners.


Any questions? Read more on our [FAQ page](./FAQ.md) located in this repo.
