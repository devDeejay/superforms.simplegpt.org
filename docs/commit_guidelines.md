# commit_guidelines.md

## Git Basics

Git is a version control system that helps you track changes in your code over time. It allows multiple developers to work on the same codebase and manage their changes efficiently.

Before diving into contribution guidelines, let's cover some basic Git concepts:

- **Repository**: A Git repository (repo) is a collection of files and their revision history.
- **Commit**: A commit is a snapshot of your code at a particular point in time. Each commit has a unique identifier called a hash.
- **Branch**: A branch is a separate line of development within a repository. By default, a repo has a main branch called `master` or `main`.
- **Fork**: A fork is a personal copy of someone else's repository. You can make changes to a fork without affecting the original repo.
- **Clone**: Cloning a repo creates a local copy on your computer.
- **Pull**: Pulling updates your local copy with changes from the remote repo.
- **Push**: Pushing sends your local changes to the remote repo.
- **Pull Request**: A pull request (PR) is a request to merge changes from one branch into another, usually from a forked repo to the original repo.

## Setting Up Git

1. Download and install Git from https://git-scm.com/downloads.
2. Configure your Git username and email:

```sh
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

## Cloning the Repository

1. Fork the repository on the platform (e.g., GitHub, GitLab) by clicking the "Fork" button.
2. Clone your forked repository to your local machine:

```sh
git clone https://github.com/yourusername/repository.git
```

## Branching and Committing

1. Always create a new branch for your changes. This keeps the main branch clean and makes it easier to manage your changes.

```sh
git checkout -b feature/your-feature-name
```

2. Make changes to the code.
3. Stage your changes:

```sh
git add .
```

4. Commit your changes with a descriptive commit message:

```sh
git commit -m "Your descriptive commit message"
```

## Commit Message Best Practices

A good commit message should:

- Be concise and clear.
- Describe the changes made.
- Use the present tense and imperative mood ("Add feature" instead of "Added feature" or "Adds feature").

A framework for commit messages:

```
[Type]: [Short description (max 50 characters)]

[Optional: Longer description (wrap at 72 characters)]

[Optional: Issue reference (e.g., "Closes #123")]
```

Example:

```
Feature: Add user authentication

Implement user authentication using JWT tokens. This includes login, logout, and registration functionality. Users can now securely access the application.

Closes #42
```

## Branch Naming Conventions

Use the following naming conventions for branches:

- `master` or `main`: The main branch containing production-ready code.
- `develop`: A branch for staging and integrating new features.
- `feature/feature-name`: A branch for developing a specific feature.
- `bugfix/bugfix-name`: A branch for fixing a specific bug.
- `hotfix/hotfix-name`: A branch for fixing critical issues in the production code.

## Pushing Changes and Creating Pull Requests

1. Push your changes to your fork:

```sh
git push origin feature/your-feature-name
```

2. Create a pull request from your fork to the original repo.

- Go to the original repository on the platform (e.g., GitHub, GitLab).
- Click the ""New Pull Request" button.
- Choose your fork and the branch you pushed your changes to.
- Review the changes and provide a clear title and description for the pull request.
- Click "Create Pull Request."

## Review and Merging

1. The project maintainers will review your pull request and provide feedback, if necessary.
2. If any changes are requested, make the necessary updates and push the changes to your branch.
3. Once the pull request is approved, the maintainers will merge your changes into the main branch.

## Keeping Your Fork Updated

To keep your fork updated with the latest changes from the original repository, follow these steps:

1. Add the original repository as a remote:

```sh
git remote add upstream https://github.com/originalowner/repository.git
```

2. Fetch the latest changes from the original repository:

```sh
git fetch upstream
```

3. Update your local main branch (replace `master` with `main` if your main branch is named `main`):

```sh
git checkout master
git merge upstream/master
```

4. Push the updated main branch to your fork:

```sh
git push origin master
```

Now your fork is up to date with the latest changes from the original repository.

By following these guidelines and best practices, you'll contribute effectively to the open-source project and maintain a clean, well-organized repository. Happy coding!