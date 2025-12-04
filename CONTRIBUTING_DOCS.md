# Contributing to Vrui
<!-- define abbreviations -->
*[PR]: Pull Request
*[PRs]: Pull Requests
*[Vrui]: Virtual Reality User Interface


First off, thank you for taking the time to contribute! 

This guide explains how outside contributors can report issues, submit fixes, create feature branches, and open PRs into the project. Following these steps keeps contributions predictable and reviewable, and makes it easier for us (the VRUI maintainers) to review and merge your work.

See the [Table of Contents](#table-of-contents) for details regarding how Vrui contributions are handled. Please make sure to read relevant sections before making your contribution. The community looks forward to your contributions. 


## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Asking Questions](#asking-questions)
- [Forking and Branching](#forking-and-branching)
- [Making changes](#making-changes)
- [Pull Requests](#pull-requests)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)
- [Documentation Updates](#documentation-updates)
- [Styleguides](#styleguides)


## Code of Conduct

This project and everyone participating in it is governed by the
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
By participating, you are expected to uphold this code. 


## Asking Questions

Before asking a question:
- Search for existing [Issues](/issues) that might help you. In case you have found a suitable issue and still need clarification, you can write your question in this issue. 
- Check the documentation.
- Search the internet.

If you then still feel the need to ask a question and need clarification, we recommend the following:

- Open an [Issue](/issues/new).
- Provide as much context as you can about what you're running into.
- Provide OS and versions, depending on what seems relevant.

Maintainers will respond to the issue as soon as possible.



## Forking and Branching

??? info "Heads up!"
    Angle brackets `<>` in commands below are placeholders, meaning that you have to replace everything between, and including, the angle brackets with some text that depends on your specific circumstances.

1. From the [Vrui GitHub](https://github.com/vrui-vr), navigate to the repository you would like to work on and fork (`Fork` button in top-right)

2. Clone your fork locally:
```sh
git clone https://github.com/<your-username>/<repo>.git
cd <repo>
```

3. Add the original repo as upstream (so your fork can stay up-to-date):
```sh
git remote add upstream https://github.com/vrui/<repo>.git
git fetch upstream
```

4. Create a branch on your fork, from origin/main
```sh
git checkout -b <issue-number-description>
```

??? note
    Use descriptive branch names, starting with the issue number and followed by a short description. This helps reviewers trace work back to issues.


## Making changes

Make small, focused commits with clear messages. Update or add documentation when functionality changes. 

To push your branch to your fork:

```sh
git add .
git commit -m "<issue-number>: short description of change"
git push origin <issue-number-description>
```

## Pull Requests

### Creating a Pull Request

1. Go to your fork on [GitHub](github.com) and click `Compare & pull request`.
2. Set the target branch to the `dev` branch of the Vrui repository you're contributing to.
3. Use a clear PR title and a descriptive body that explains:
    - What you changed
    - Why it is needed
    - Any user-facing changes
    - Testing instructions or reproduction steps
4. If your change fixes or is related to an issue, link the issue in the PR .
5. Ensure documentation is updated when applicable.

### Linking Pull Requests to Issues

If you are fixing an existing issue, your PR should link to the issue. 

One simple way to accomplish this is to reference specified keywords in your commit message. Supported keywords include: 
- `close`
- `closes`
- `closed`
- `fix`
- `fixes`
- `fixed`
- `resolve`
- `resolves`
- `resolved`

An example commit message using one of these linking keywords: 
```
Closes #<issue-number>
```

This message links your PR to a specific issue and will close the issue when the PR is merged by Vrui maintainers.

For more detailed instructions and alternative issue linking methods, please refer to the following GitHub guide: [Linking a pull request to an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue) 

### PR Reviews and Merges

PRs are reviewed by the Vrui organization maintainers and once approved, will be merged into main for deployment (after CI passes).


## Reporting Bugs


#### Before Submitting a Bug Report 

A good bug report shouldn't leave others needing to chase you up for more information. Therefore, we ask you to investigate carefully, collect information and describe the issue in detail in your report. Please complete the following steps in advance to help Vrui maintainers fix any potential bug as fast as possible.

- Ensure that you are using the latest version. If not, update to the latest `dev` branch and confirm that the bug still occurs.
- Determine if your bug is really a bug and not an error on your side e.g. using incompatible environment components/versions. 
- To see if other users have experienced (and potentially already solved) the same issue you are having, check if there is not already a bug report (issue) existing for your bug or error.
- Also make sure to search the internet (including Stack Overflow) to see if users outside of the GitHub community have discussed the issue.
- Collect information about the bug:
    - Stack trace (Traceback)
    - OS, Platform and Version (Windows, Linux, macOS, x86, ARM)
    - Version of the interpreter, compiler, SDK, runtime environment, package manager
    - Minimal reproduction (code example) and steps to reproduction

#### Submitting a Bug Report

!!! warning
    You must never report security related issues, vulnerabilities or bugs including sensitive information to the issue tracker, or elsewhere in public. 

To submit a bug: 

- Open an [Issue](/issues/new). 
- Explain the behavior you would expect and the actual behavior.
- Please provide as much context as possible and describe the *reproduction steps* that someone else can follow to recreate the issue on their own. This usually includes your code. For good bug reports you should isolate the problem and create a reduced test case.
- Provide the information you collected in the previous section.

Once it's filed:

- The project team will label the issue accordingly.
- A team member will try to reproduce the issue with your provided steps. If there are no reproduction steps or no obvious way to reproduce the issue, the team will ask you for those steps and mark the issue as `needs-repro`. Bugs with the `needs-repro` tag will not be addressed until they are reproduced.
- If the team is able to reproduce the issue, it will be marked `needs-fix`, as well as possibly other tags (such as `critical`), and the issue will be left to be [implemented by someone](#your-first-code-contribution).


### Suggesting Enhancements


#### Before Submitting an Enhancement Suggestion

- Make sure that you are using the latest version.
- Read the documentation carefully and find out if the functionality is already covered.
- Perform a [search](/issues) to see if the enhancement has already been suggested. If it has, add a comment to the existing issue instead of opening a new one.
- Find out whether your idea fits with the scope and aims of the project.


#### Submitting an Enhancement Suggestion

Enhancement suggestions are tracked as [GitHub issues](/issues).

- Use a **clear and descriptive title** for the issue to identify the suggestion.
- Provide a **step-by-step description of the suggested enhancement** in as many details as possible.
- **Describe the current behavior** and **explain which behavior you expected to see instead** and why. At this point you can also tell which alternatives do not work for you.
- **Explain why this enhancement would be useful** to most contributing users. 


### Documentation Updates

Small doc fixes can be included in any PR that touches relevant code. Keep docs consistent with code, updating examples and command snippets when you change functionality.

### Styleguide

## Attribution
This guide is based on the contributing.md.