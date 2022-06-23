# Open Source Project Analysis

For this [homework assignment](https://github.com/rcos/CSCI-4470-OpenSource/blob/1b949d62d9e43b790558f61c51554471a97e0467/Assignments/Analysis%20Homework/Analysis%20Homework.md), three open-source projects were chosen for analysis.  I chose to analyze ShellCheck, NetworkX, and Submitty.  All three projects are large projects with active user bases.  For the second part of the assignment, I chose to analyze Submitty in greater depth.  I have made contributions to each of the three projects analyzed, and I am currently one of the primary developers of Submitty.  

## Part 1: Project Analysis

### ShellCheck

| Evaluation Factor | Level (0-2) | Evaluation Data |
|---|---|---|
| Licensing | 2 | GPL-3 |
| Language | 2 | Haskell |
| Level of Activity | 2 | Sporadic commits, mostly by single contributor |
| Number of Contributors | 1 | Single contributor has majority of commits.  129 contributors total. |
| Product Size | 2 | Moderate |
| Issue Tracker | 1 | Many abandoned issues |
| New Contributor | 0 | No guidelines observed |
| Community Norms | 1 | No guidelines observed |
| User Base | 2 | Active user base, common real-world usage |
| Total Score | 13 |  |

[ShellCheck](https://github.com/koalaman/shellcheck) is an open-source shell script linter licensed under GPL-3.  A score of 2 is awarded in the license category for using an open-source license.

The project is written primarily in Haskell, and is deployed via GitHub Actions.  Beyond a small handful of shell scripts for managing building, installation and deployment, the entire codebase is written in Haskell, which simplifies dependencies.  Perhaps hypocritically, ShellCheck does not use a CI/CD pipeline to lint their shell scripts.  Likewise, there is no code style enforcement for Haskell.  Although I consider the lack of clear, automated, code style enforcement to be an egregious shortcoming, it is not enough to warrant a score reduction.  Haskell is often used in the field of syntax trees, and has many relevant libraries available, so provides a good language option for this project.

ShellCheck is a moderately active project with short bursts of activity spaced throughout the year.  Each of the previous four quarters had some amount of activity, which warrants a score of 2.

Only one primary contributor makes regular contributions to this project.  A handful of other individuals have made multiple contributions, but these are ultimately dwarfed by the 1100+ commits made by the primary contributor.  Due to a lack of major contributors, I have scored this with a 1.

The code base for ShellCheck is reasonable in size, and organized in a manner such that even brand new contributors can find relevant code.  Thus, a 2 is awarded in the product size category.

ShellCheck has almost 800 open issues as of the time of this writing, and few issues show signs of engagement.  Most issues are left to rot, including issues which report critical issues.  Additionally, the documentation pages say to ask questions by creating issues, but few of the issues with questions have helpful responses.  At the same time, some activity is noted, which is enough to avoid a 0.  As such, a 1 is awarded in the issue tracker category.

ShellCheck lacks clear instructions for new contributors and information for newcomers is mostly targeted towards new users and those who wish to request new features or report bugs.  A complete lack of information for new contributors results in a score of 0 for the new contributor category.

There is no clear code of conduct and no attempt at community building can be observed on the repository.  At the same time, no outright hostile or undesirable behavior was observed.  This results in a 1 in the community norms category.  

ShellCheck is the only shell script linter in common usage today.  As such, ShellCheck has a substantial user base with popular plugins for many IDEs, as well as integration with several major CI/CD providers such as Travis.  A 2 is awarded for the user base category as a result.

### NetworkX

| Evaluation Factor | Level (0-2) | Evaluation Data |
|---|---|---|
| Licensing | 2 | BSD 3-Clause |
| Language | 2 | Python |
| Level of Activity | 2 | Highly active for sustained period of time |
| Number of Contributors | 2 | Many frequent contributors in addition to substantial volume of community contributions |
| Product Size | 2 | Good project organization without excess code |
| Issue Tracker | 2 | Frequent activity, including frequent engagement by maintainers |
| New Contributor | 2 | Welcoming information, advice, and support channels for new contributors |
| Community Norms | 2 | Community guidelines documented and enforced.  No evidence of rude or hostile behavior. |
| User Base | 2 | NetworkX is often used in the real world, particularly in academia, and has a large user base. |
| Total Score | 18 | |

[NetworkX](https://github.com/networkx/networkx) is a graph library written in pure Python and primarily maintained by the Berkeley Institute for Data Science.  The project is licensed under the BSD 3-Clause license and is included in a range of other extremely popular Python libraries.

A core principle of the NetworkX project is that everything is written in pure Python, with a handful of optional extensions which use the underlying C implementations of NumPy and SciPy functions.  In addition, the dependencies required to use NetworkX are limited to only four dependencies which are commonly used in other parts of projects which use NetworkX anyway.  The only dependencies are: NumPy, SciPy, Matplotlib, and Pandas.  This commitment to Python with only minimal dependencies makes NetworkX easy to include in other projects, which contributes to its success.

Several organizations sponsor full-time developers to maintain NetworkX.  In addition, members of the broader community frequently make pull requests to add new features or fix bugs in existing ones.  In total, GitHub lists 553 contributors for the project.  As such, NetworkX is deserving of a score of 2 for the number of contributors category.

The NetworkX codebase is substantial in size and there are a number of functions which are not documented in detail.  A well-maintained testing suite and clean project structure ensures that functionality is rarely inadvertently affected.  As such, I believe that the amount of code present is appropriate for the project and have awarded a score of 2 in the product size category.

NetworkX uses their issue tracker effectively.  Maintainers respond to almost every issue promptly and issues are either closed or fixed in a reasonable amount of time without becoming stale.  The overall issue list is under 200 issues which is commendable for a project of this size.

New contributor guidelines are clear and posted prominently, thus earning NetworkX a 2 in the new contributor category.  The project maintainers seem to be quite effective at responding to issues in helpful ways such that those who report issues can easily fix the issues as well.  Likewise, the community guidelines are clearly posted and enforced by the maintainers which results in a score of 2 for the community norms category as well.

The NetworkX user base is large and highly active, with several support channels available.  NetworkX is mostly used in academia but it has also been used in a range of industry products.

### Submitty

| Evaluation Factor | Level (0-2) | Evaluation Data |
|---|---|---|
| Licensing | 2 | BSD 3-Clause |
| Language | 1 | Many different languages/technologies |
| Level of Activity | 2 | Highly active with many different contributors |
| Number of Contributors | 2 | Large number of contributors.  Mostly inactive, but 5-10 active at any given point. |
| Product Size | 1 | Code base is bloated and could be restructured to make the project more manageable in size. |
| Issue Tracker | 2 | Issue tracker is used effectively, despite having a large number of stale issues. |
| New Contributor | 2 | Instructions for new contributors are clearly marked and community is welcoming of outside contributions. |
| Community Norms | 1 | No signs of poor conduct, but no code of conduct posted. |
| User Base | 2 | Submitty is used at several different universities, serving thousands of students each term. |
| Total Score | 14 |  |

Submitty is a code autograding platform developed primarily by Rensselaer Polytechnic Institute.  The project is licensed under the BSD 3-Clause license, which justifies a 2 in the licensing category.

Submitty's codebase is a concoction of dozens of different, and sometimes overlapping, languages and libraries.  The website backend is primarily developed in PHP with the Twig extension, while the autograder is primarily written in C++ and Python, with a handful of additional shell scripts.  The website frontend uses a mix of Javascript and Typescript, with multiple versions of Bootstrap for styling, as well as the JQuery library.  Haskell and Node.js are also used in various places for autograding tools.  The extensive array of technologies present in this project results in a large dependency footprint and poses a number of maintenance issues.  At the same time, this is a large project with many different performance and security needs, with a practical use case for each technology used, so I have rated the language category a 1.

Submitty is a highly active project with a number of paid student developers.  GitHub lists more than 150 contributors to the project, but the vast majority of the contributors are former students who have been inactive since leaving RPI.  The activity for this project has been continuous throughout the year for many consecutive years, which results in a 2 in the level of activity category.  The number of contributors category also receives a 2 due to the large number of developers with non-negligible commit counts.

In my opinion, Submitty's codebase is quite bloated and structured poorly such that it is challenging to find all of the relevant pieces when diagnosing some issues.  As such, I have awarded a 1 in the product size category.

An issue tracker is used effectively to manage bugs and outstanding development goals.  Submitty could benefit from being more proactive about closing stale or irrelevant issues.  Due to the high amount of activity in the issue tracker, a 2 is justified in the issue tracker category.

As a largely student-maintained project with a high developer turnover rate, Submitty has clear instructions for new developers which results in a 2 in the new contributor category.

Submitty lacks a posted code of conduct, but no hostile or inappropriate behavior was observed, which results in a 1 in the community norms category as per the rubric.

Submitty has an active user base at several different colleges and serves thousands of users throughout the year.  As per the rubric, a 2 is awarded in the user base category.

## Part 2: Detailed Project Analysis

Submitty is a code autograding and assignment submission platform primarily maintained by Rensselaer Polytechnic Institute students through the Rensselaer Center for Open Source (RCOS).  During the academic year, Submitty supports thousands of students at universities worldwide, including at Rensselaer, which hosts Submitty at https://submitty.cs.rpi.edu.  Submitty is licensed under the permissive BSD 3-Clause license, which allows others to develop and use Submitty at other campuses with no usage restrictions.

Submitty is divided into several modules, each with its own requirements and associated technologies.  There is a solid rationale for the usage of each technology present for each specific use-case, but the overall collection of technologies can be overwhelming to maintain.  GitHub lists nearly 100 direct dependencies for the main Submitty repository, only counting JS, Python, and PHP dependencies.  Even excluding the development-only dependencies, Submitty depends heavily upon dozens of different libraries, which increases the chances of becoming collateral damage as part of a supply-chain attack or accidentally breaking lesser-used, and largely untested, portions of Submitty as dependencies evolve.  

The autograder is primarily written in C++, with small portions of Python.  A handful of shell scripts link everything together.  The website is developed largely in PHP on the server side, and uses the Twig plugin to render templates.  For more interactive parts of the site, JQuery is used on the client side to dynamically update pages.  Web sockets are also used for dynamic content in various places.  This combination of technologies leads to slow development and frequent bugs since a portion of the content is rendered on the server side and the rest is rendered on the client side, often including duplicate code.  I only awarded a 1 in the language category because of the confusion introduced by having an excessive number of dependencies, and the clumsiness with which even the simplest features must be implemented due to the languages chosen.

Submitty is maintained by a team of mostly undergraduate students at Rensselaer Polytechnic Institute.  Summer is typically the most active time, but there have been commits made during every single month of Submitty's existence.  In the last month alone, 37 issues have been closed and 124 pull requests have been merged by 22 unique individuals.  GitHub lists 161 contributors in total, of which 61 have made more than 10 commits.  I consider this to be enough activity to be considered a  highly active project and have thus awarded a 2 in the level of activity category.  Similarly, there is a continuous stream of new developers joining the project, and a large collection of past developers who were active in the past, so I have awarded a 2 in the number of contributors category.  For some projects, the number of inactive contributors might be concerning, but it is understandable for a project like Submitty where most contributors only contribute to the project while they are enrolled in college.

The main repository is quite disorganized after many years of development, which makes the project feel larger and bulkier than it is.  Regardless of the number of lines of code present, it is sometimes unclear even to active developers where relevant code lies within the codebase.  Code style is enforced for PHP, JS, and CSS, but most of the style enforcement was added in recent years and older code is often messy.  Additionally, CSS and JS snippets are frequently added to Twig files where the code style cannot be enforced.  Submitty has several submodules which are maintained in separate repositories and included via a dependency system.  Submitty's product itself is feature-rich, but is prone to breakage due to poor test coverage.  Many features overlap significantly and could be simplified if proper thought was given to the layout and design.  A score of 1 was given in the product size category as a result.

A single issue tracker on the main Submitty repository tracks issues for all of the repositories in the organization.  Since all of the repositories in the Submitty organization are closely related, and ultimately integrate with the main Submitty repository, this issue-tracking structure is effective at reducing issue duplication and makes it easier to search for related issues.  Issues are properly linked to pull requests and closed when resolved, and the issue turnover rate is high, which is enough to justify a 2 in the issue tracker category of the table.  My only criticism of the issue tracker usage is what I consider an excessive number of stale issues which are impractical and extremely unlikely to be implemented in the future.  The vast majority of the 300+ open issues are "nice to have" feature requests, not reported bugs.  Even so, the list is well-maintained and urgent issues are addressed quickly, which satisfies the requirements listed in the rubric for this table entry.

Submitty has clear guidelines for new contributors, including a `CONTRIBUTING.md` file in the main code repository and several dedicated pages in the documentation repository.  A Slack channel is publicly available for new contributors to interact with current developers and ask questions.  In some cases, potential new contributors who make low-effort posts seeking for others to tell them how to fix issues go ignored, but many of these posts appear on issues tagged with the "good first issue" tag, and may often be classified as spam.  The clear guidelines observed are sufficient for a score of 2 for the new contributor category, despite the lack of interaction with potential new contributors on GitHub issues.  

No official code of conduct could be found on the GitHub repository or on the project website.  No signs of hostility or other inappropriate behavior were observed in either the Slack channels or on the GitHub repository.  These things in combination result in a score of 1 for the community norms entry in the evaluation table.
