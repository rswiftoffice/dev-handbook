# Collaborating on code

We use git to work on code together. Git is a version control tool that lets us track changes to a repository.

When using git and github, you should try to follow our best practices.

**DOs**

:heavy_check_mark: Do commit often so you can roll back easily.

:heavy_check_mark: Do commit with meaningful commit messages. It makes it easier for other people to review your code. It is recommended to use present tense for verbs, such as Add xx, Update xx, Delete xx.

:heavy_check_mark: Do use branches for development and merge them into master when it is stable. Here are some suggested naming conventions for branches:

```
feature/<feature name>      New features
bug/<issue description>     Bug fixes
```

:heavy_check_mark: Do use github to track issues. You can set labels like bug, maintenance, enhancement and question to make tracking easier.

**Don'ts**

:heavy_multiplication_x: Do not commit generated files, dependencies, configuration files, secrets, keys and certificates into any repository. Add them to .gitignore.

:heavy_multiplication_x: Try not to push directly into the master branch. It makes rolling back features/releases more difficult.
