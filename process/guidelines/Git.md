| Issue | #34 |
| ----- | -- |
| author | Thomas Stoiber @11777755 |
| released by | Nicolas Griebenow @01617265 |
| release date | 2020-11-01 |

| Issue | #18 |
| ----- | -- |
| author | Thomas Stoiber @11777755 |
| released by | Nicolas Griebenow @01617265 |
| release date | 2020-10-18 |

## Commit Messages
The commit message describes what happens in this commit. The following rules apply both for the code repository as well as the Wiki repository.
A commit message fulfills the following restrictions:
 - The commit starts with the issue number prefixed with the hash (#) in square brackets, e.g. \[#18\]
 - After that a short summary is given in max. 70 characters.
 - The subject line is capitalized (it starts with a capital letter).
 - The subject line starts with a verb in imperative mood, e.g. Add, Remove, Move, Delete, Change, Fix ...
 - The subject line must not end with a period.
 - An empty line separates the subject line from the body.
 - A commit can, but don't have to have a body.
 - The body contains a more detailed description of the commit.
 - A line in the body does not exceed 80 characters in length.
 - In the wiki, commits generally don't have a body.

### Examples

[#34] Add feature description for project proposal<br>
[#20] Remove colon in the subsection Detailed Risk Analysis<br>
[#4] Fix bug in getAnimals method<br>

### More Information
 * These rules are best practices and follow the "How to Write a Git Commit Message" guide by Chris Beams (https://chris.beams.io/posts/git-commit/)

## Git Workflow

The project has the following branches:
* `master`: The master branch is the branch whose code should be continously deployed to production. All tests (unit, integration, e2e) must be green.
On the one hand, a hotfix branch can be merged into the master (for bugs that are crucial to business and operation). In this case the commit is tagged and the minor version is increased by 1 (for instance: v4.2 -> v4.3).
On the other hand, the dev branch can be merged into the master for new features. In this case the major version is increased and the minor version is reset to zero (for instance: v4.3 -> v5.0).  
* `dev`: This is the branch which holds all current developements. A feature branch can be merged into the dev it at least the integration tests are green. When a branch in merged into the `dev`.  
* `feat/concise-feature-or-purpose-descripton`: This is a branch that focuses on a concrete feature as described in the text after `feat/`.
* `bug/concise-purpose-descripton`: This is a branch that focuses on a bug that is not business critical, but still needs to be fixed (for instance a bug that is due to a new feature in the dev branch).
* `hotfix/concise-purpose-descripton`: This is a branch that focuses on a bug that is business critical and requires immediate action because the production system is affected. It can be merged into the master immediately, but also needs to be merged into the dev branch.
* `refactor/concise-purpose-description`: This is a branch that solely focuses on refactoring. It should not change the system behaviour or add new features.

If a developer wants to change an existing feature or add a new feature, they have to check out the latest commit of the `dev` branch, and then start a new `feat/` branch. After implementing the feature using a number of commits, the developer has to create a new merge request so that the `feat/` branch gets merged into the `dev` branch. This merge request should be approved or rejected by another developer to stick to the 4-eyes-principle. Before merging, it is mandatory to run our CI pipeline (hence it must not be immediately merged). The developer is not allowed to merge locally into `dev`. This should be done via GitLab.

There should not be any development on the `dev` and `master` branches. The development is done on a feature, bug or hotfix branch and afterwards merged into the `dev` or `master` respectively using a merge request.
