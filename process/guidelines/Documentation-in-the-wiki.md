| Issue | #4 |
| ----- | -- |
| author | Stefan Puntigam @11776838 |
| released by | Nicolas Griebenow @01617265 |
| release date | 2020-10-14 |

| Issue | #25 |
| ----- | -- |
| author | Stefan Puntigam @11776838 |
| released by |  |
| release date | 2020-11-DD |

# Documentation in the wiki

Process documentation is always in the wiki. Also some more high-level or explanatory product documentation can be found here.

## Wiki Structure

The Wiki is structured into two main categories: product documentation and process documentation. Product documentation describes qualities of the product of the project at a certain point in time; it will change over the course of the project. Process documentation encompasses information about the development process such as meeting protocols and sprint backlogs.

Additionally there is a directory for text templates for recurring documentation tasks such as meeting protocols.


## Four eyes principle

Important documents in the Wiki are checked by at least two people before they are considered an accepted source of truth: an author and another person called approver. Someone who creates a new artifact that involves some important decision-making would use the template at `templates/Reviewed-Document.md` and fill out the author field and put the unreviewed document into the wiki. The author would then find someone willing to review the new contents. He is called the approver.

The approver who finds the document acceptable would signify that by adding the own name in the `released by` field and the current date.


## Conventions

### Date and Time
Dates are formatted as defined in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601): A date would be written in the form `YYYY-MM-DD`. If a date should appear in a title/filename in the wiki, using an en dash ("–") in place of the minus is customary; a minus in a filename would be displayed as a space. 

Time is written as `hh:mm` and can be assumed to use the Central European Time.

### Units
All measurements use units defined by the [International System of Units](https://www.bipm.org/utils/common/pdf/si-brochure/SI-Brochure-9-EN.pdf) or units that are accepted for use together with SI (minutes, hours).

## Offline Work
Optionally, the wiki is also accessible as a git repository as explained by the [GitLab documentation](https://reset.inso.tuwien.ac.at/repo/2020ws-ase-pr-group/20ws_ase-pr_inso_01/-/wikis/git_access). [^1] That is recommended for changes that affect multiple files, as the commit message can be used to describe what is done. Otherwise, using the online interface is fine too.

[^1]: `gem` is available on most Linux distributions under the package name `rubygems`, for Windows there is an [installer](https://rubyinstaller.org). 
