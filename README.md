# Readme

## Requirements (AWS)

The role you are using needs IAM CodeCommit permissions to at least the repo you are going to work on

## Requirements (Workstation)

Your machine needs to be authenticated to AWS

You need the following packages:

* `python3`
* `boto3`
* `awscli`
* `git`

Example to meet these on Amazon Linux 2023:

```shell
dnf install python3-boto3 awscli git
```

## Installing

Place the `git-remote-codecommit` script somewhere in your system path and ensure it is executable

Example:

```
curl https://raw.githubusercontent.com/dkw-versent/git-remote-codecommit/local-install/git-remote-codecommit > ~/.bin/git-remote-codecommit
chmod 0755 ~/.bin/git-remote-codecommit
```

## The following will now work

```
$ git clone|pull|push codecommit://MyRepositoryName
$ git clone|pull|push codecommit://demo-profile@MyRepositoryName
$ git clone|pull|push codecommit::ap-southeast02://demo-profile@MyRepositoryName
```

## How does this work?

https://git-scm.com/docs/gitremote-helpers
