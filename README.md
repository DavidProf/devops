# Xarlyu DevOps

DevOps repository with information, tutorials and configurations related to DevOps

[Please see our **glossary** to understand this repo](#glossary)


## Docs

Both links below have the same doc only displayed in different ways:

-   [Docs wiki](https://github.com/Xarlyu/devops/wiki)
-   [Docs WebSite *Unavailable*]()

## How to contribute

See the instructions about how to make contributions to the repo.

### Add a new module

To add a new module:

-   [Fork this repo](https://github.com/Xarlyu/devops/fork?fragment=1)
-   In the forked repo create a new folder in `/modules` with the name of the module
    -   E.g. `mkdir modules/mongodb`
-   For each subject or tool related, add a folder to hold the files related
    -   E.g.
        -   Docker: `modules/mongodb/docker`
        -   docker-compose: `modules/mongodb/docker-compose`
        -   Kubernetes: `modules/mongodb/kubernetes`
        -   Config Files: `modules/mongodb/config`
        -   backup: `modules/mongodb/backup`
-   Then you will only need to add your files

Tips:
-   Do not add readmes or any doc here, please edit the wiki
-   It's recommended to add comments in files or configurations that support it

## Glossary

| Term  | Definition  |
| ------------ | ------------ |
| Module  | A set of items for a particular subject or tool  |
