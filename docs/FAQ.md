# Frequently Asked Questions (FAQ) about GitHub Actions for IBM Power, IBM Z and IBM LinuxONE

## How do I get on-boarded to this service?

Please read our [onboarding document](onboarding.md) located in this repo!

## What permissions are granted to the GitHub app?

This app requires read access to metadata, read and write access to actions, administration, checks, and workflows for the repository selected for install. Additionally this GitHub app requires reading the User account email address for security reasons. Read more about why adminstrative read and write access are required in the official GitHub API docs [here](https://docs.github.com/en/rest/actions/self-hosted-runners?apiVersion=2022-11-28#create-a-registration-token-for-a-repository).

## What about forked repos?

After our GitHub app is installed on specific repos or at the organization level, the repos are pending approval. We verify the repos match the request name and have a legitimate use case for Power and Z. Once the repo is approved, the project is allowed to use our images as they wish. Since forked repos would not be in our approved list, they cannot use our images. GitHub Actions for Power and Z will only work for repos that have the GitHub app properly installed AND they are in the approved list. Read more in this [issue](https://github.com/IBM/actionspz/issues/22) about options to use on your repo.

## Is there a fee to use this service? Do I need a credit card to sign up?

This service is no-cost and you will not be asked for a credit card upon
sign-up. You will need an IBMid (also no-cost).

## Why do I need to create an IBMid?

An IBMid is required to help with service security so we can ensure a safe
environment is maintainted for all users. IBM's official Privacy statement is located [here](https://www.ibm.com/trust/privacy).

## How do I make changes to workflows for seamless integration with existing platforms?

After the GitHub App is installed on your repo, add the ```runs-on:``` tag to your
existing workflow file.

## Are all actions supported out-of-the-box?

The actions themselves need to be functional on ppc64le and s390x. If you're
unsure, our team can work with your project to make this determination, and
identify the steps that may need to be taken to on-board your project.

## Are the runner images used for the jobs ephemeral?

Yes, the runners are ephemeral. For every job, a new runner is allocated and then deleted once the job completes.

## Can I specify the IBM hardware to execute my workflow on?

Yes, you can view our [supported images](./supported-images.txt) here. 
`ubuntu-24.04-ppc64le` image tag is to utilize IBM POWER9, `ubuntu-24.04-ppc64le-p10` for IBM POWER10, and `ubuntu-24.04-s390x` is for IBM Z.

## How do I report a problem?

Please use the [issue tracker](https://github.com/IBM/actionspz/issues) in this
repository.
