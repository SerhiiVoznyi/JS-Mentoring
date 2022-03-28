# [JavaScript Mentoring Program](../README.md)

## 1 Source Code Management (SCM) Tools For Version Control

## 1.1 Source code management

Source code management (SCM) is used to track modifications to a source code repository. SCM tracks a running history of changes to a code base and helps resolve conflicts when merging updates from multiple contributors. SCM is also synonymous with Version control.

As software projects grow in lines of code and contributor head count, the costs of communication overhead and management complexity also grow. SCM is a critical tool to alleviate the organizational strain of growing development costs.

## The benefits of source code management

In addition to version control SCM provides a suite of other helpful features to make collaborative code development a more user friendly experience. Once SCM has started tracking all the changes to a project over time, a detailed historical record of the projects life is created. This historical record can then be used to ‘undo’ changes to the codebase. The SCM can instantly revert the codebase back to a previous point in time. This is extremely valuable for preventing regressions on updates and undoing mistakes.

The SCM archive of every change over a project's life time provides valuable record keeping for a project's release version notes. A clean and maintained SCM history log can be used interchangeably as release notes. This offers insight and transparency into the progress of a project that can be shared with end users or non-development teams.

SCM will reduce a team’s communication overhead and increase release velocity. Without SCM development is slower because contributors have to take extra effort to plan a non-overlapping sequence of develop for release. With SCM developers can work independently on separate branches of feature development, eventually merging them together.

Overall SCM is a huge aid to engineering teams that will lower development costs by allowing engineering resources to execute more efficiently. SCM is a must have in the modern age of software development. Professional teams use version control and your team should too.

## Source code management best practices

* ### Commit often

Commits are cheap and easy to make. They should be made frequently to capture updates to a code base. Each commit is a snapshot that the codebase can be reverted to if needed. Frequent commits give many opportunities to revert or undo work. A group of commits can be combined into a single commit using a rebase to clarify the development log.

* ### Ensure you're working from latest version

SCM enables rapid updates from multiple developers. It’s easy to have a local copy of the codebase fall behind the global copy. Make sure to git pull or fetch the latest code before making updates. This will help avoid conflicts at merge time.

* ### Make detailed notes

Each commit has a corresponding log entry. At the time of commit creation, this log entry is populated with a message. It is important to leave descriptive explanatory commit log messages. These commit log messages should explain the “why” and “what” that encompass the commits content. These log messages become the canonical history of the project’s development and leave a trail for future contributors to review.

* ### Review changes before committing

SCM’s offer a ‘staging area’. The staging area can be used to collect a group of edits before writing them to a commit. The staging area can be used to manage and review changes before creating the commit snapshot. Utilizing the staging area in this manner provides a buffer area to help refine the contents of the commit.

* ### Use Branches

Branching is a powerful SCM mechanism that allows developers to create a separate line of development. Branches should be used frequently as they are quick and inexpensive. Branches enable multiple developers to work in parallel on separate lines of development. These lines of development are generally different product features. When development is complete on a branch it is then merged into the main line of development.

* ### Agree on a Workflow

By default SCMs offer very free form methods of contribution. It is important that teams establish shared patterns of collaboration. SCM workflows establish patterns and processes for merging branches. If a team doesn't agree on a shared workflow it can lead to inefficient communication overhead when it comes time to merge branches.

## Summary

SCM is an invaluable tool for modern software development. The best software teams use SCM and your team should too. SCM is very easy to set up on a new project and the return on investment is high. Atlassian offers some of the best SCM integration tools in the world that will help you get started.

## Learning materials

### Videos

* [Что такое Git?](https://www.youtube.com/watch?v=W4hoc24K93E&list=PLDyvV36pndZFHXjXuwA_NywNrVQO0aQqb&ab_channel=JavaScript.ru)
* [Git vs GitHub](https://youtu.be/21Gl97tkbHU)

### Articles

* [What source control](https://www.perforce.com/blog/vcs/what-source-control)

### Desktop Tools

* [GitHub Desktop](https://desktop.github.com/)
* [SourceTree](https://www.sourcetreeapp.com/)
* [TortoiseGit](https://tortoisegit.org/)

## Home Tasks

1. Create your professional GitHub account with this **[Join GitHub](https://github.com/join)**.
2. Install source code management app. Preferable **[GitHub Desktop](https://desktop.github.com/)**.
3. Link your app with your GitHub account. **Search and learn how to do that**.
4. Create specific folder for your repositories. For example '`C:\Development\Repositories`'.
5. Clone remote repository to your working station. **[Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)**.
6. Create your working branch with the name `js-course-m1-`*your name*`-home-task`. [Git Branching](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
7. Modify this README.md file under folder **M1-SourceCodeManagement**. Add text to the end **`I done with all tasks`**.
8. Commit your changes using your app or git command.
9. Push your changes to remote repository.
10. Create a pull request with your changes.
