# Lab work dedicated to deploying a simple static website
http://az-testbucket-virginia.s3-website-us-east-1.amazonaws.com
using GitHub Actions technology


### Laboratory work progress:

[1] - Preparing AWS Services
----------------------------

[1.1] - A root AWS account was created in the standard way, using the web interface.

[1.2] - A user named `az` was created using AWS IAM, with a 12-digit ID, different from root. The `az` account is placed in the `admins` group with AdministratorAccess rights, without the ability to control or even view financial accounts.

[1.3] - AWS IAM has created a user called `labworker` that is not able to sign in to the web management console. This user has been granted the single permission AmazonS3FullAccess.

[1.4] - An access key has been created for the user `labworker`.

[1.5] - AWS S3 bucket `az-testbucket-virginia` has been created. This resource has versioning enabled for stored objects.

[1.6] - Access permissions and website hosting settings have been configured for `az-testbucket-virginia`.

[1.7] - Using the AWS S3 web interface, a small image `FlagSmall.jpg` was uploaded and access to this object was checked from another browser using the link:
https://az-testbucket-virginia.s3.amazonaws.com/FlagSmall.jpg



[2] - Preparing a GitHub repository
-----------------------------------

[2.1] -On the local host Xubuntu22.04 the project text files were prepared:
```bash
$ tree -a
    .
    ├── error.html
    ├── index.html
    ├── .github
    │   └── workflows
    │       └── deploy-to-S3-github-actions.yaml
    ├── .gitignore
    └── README.md
```

[2.2] - A repository `EPAM-AWS-S3-Lab-GitHub-actions` has been created using the GitHub web interface.

[2.3] - The repository has been initialized on the local host, the first commits have been created, and the local .git database has been synchronized with the remote repository:
```bash
$ git init
$ git remote add origin git@github.com:Azrubael/EPAM-AWS-S3-Lab-GitHub-actions.git
$ git add README.md
$ git commit -m "Added -- README.md"
    ...
$ git push -u origin main
```
`Note: Settings of Git on the local host automatically create a first branch called main.`

[2.4] - Using the web interface for the GitHub repository, two hidden variables KID and SAC (key and secret) were created. These variables provide access to the AWS S3 bucket 'az-testbucket-virginia'.



[3] - Debugging
---------------

[3.1] - Copied AWS S3 enpoint link with static content:
`http://az-testbucket-virginia.s3-website-us-east-1.amazonaws.com`

[3.2] - Debugging of `./.github/workflows/deploy-to-S3-github-actions.yaml` was done by method of attempt and error. All works were done only on the main branch of the Git Hub repository.



[4] - Final operations
----------------------

[4.1] - A detailed report on the progress of the laboratory work has been compiled.

[4.2] - The GitHub repository has been updated:
`https://github.com/Azrubael/EPAM-AWS-S3-Lab-GitHub-actions`
