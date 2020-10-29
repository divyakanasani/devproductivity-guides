# Team Development Feature Parity is based on Needs

| Team Development                                                                                                                                   | Need                                                                                                    | Studio, Source Control, App Repo, and CI/CD                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Detecting and resolving conflicts prior to promoting                                                                                               | Code validation to minimize risk of production outage                                                   | Automated test coverage (e.g. ATF) as a part of running a CI build that triggers on source control Pull Request to merge feature branch into master branch                                                        |
| Large teams with many dev instances pull/push changes to a dev master to merge their changes before pushing up the stack (test, stage, prod, etc.) | Supporting many developers and teams each working on their own feature/bug stories and delivery cadence | Separate applications and separate branches, use Git flow to merge via Pull Requests. Many dev instances if working on the same app but different branches.                                                       |
| See where a set of changes are in their promotion journey.                                                                                         | Visualization for which “stage” a code change is in                                                     | Jenkins, Azure Pipelines, other popular CI/CD tooling provide ability to define stages and visualize progress as the pipeline runs.                                                                               |
| Enforce pull before push between parent and child instances                                                                                        | Merging code to detect conflicts prior to deploying code.                                               | Use Git branches and Pull Requests, code conflicts will automatically be detected between branches prior to merge. Publish, install, rollback applications when validating in test environments.                  |
| Do everything on-platform.                                                                                                                         | Reduce number of tools to manage.                                                                       | Customers benefit from adopting integration with Git repos and workflows, as it’s the standard for software development today. We provide both on-platform and off-platform options for building CI/CD pipelines. |
| Update sets work for global, scoped, and Store/OOTB customizations.                                                                                | Use one development model for everything, especially for global file customizations.                    | Post-Quebec, Source Control will work for scoped apps, global apps (Paris), and Store/OOTB customizations (Quebec). You’ll also be able to move these apps through App Repo either via UI or CI/CD APIs.          |