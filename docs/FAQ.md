# Frequently Asked Questions (FAQ) about GitHub Actions for IBM Power, IBM Z and IBM LinuxONE

## How do I get on-boarded to this service?

Please read our [onboarding document](onboarding.md) located in this repo!

## Is there a fee to use this service? Do I need a credit card to sign up?

This service is no-cost and you will not be asked for a credit card upon
sign-up. You will need an IBMid (also no-cost).

## Why do I need to create an IBMid?

An IBMid is required to help with service security so we can ensure a safe
environment is maintainted for all users.

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
`ubuntu-24.0-ppc64le` image tag is to utilize IBM POWER9, `ubuntu-24.0-ppc64le-p10` for IBM POWER10, and `ubuntu-24.04-s390x` is for IBM Z.

## How do I report a problem?

Please use the [issue tracker](https://github.com/IBM/actionspz/issues) in this
repository.
