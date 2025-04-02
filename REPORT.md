# Git and CI/CD Implementation Report

## Project Summary

This report summarizes the implementation of Git version control and CI/CD pipeline as part of the Software Build Automation Tools assignment. The project is hosted on GitHub at: https://github.com/egezamb/git-cicd-project

## Tasks Completed

### 1. Git Repository Initialization
- Created a new directory and initialized a Git repository
- Created a README.md file with project description
- Staged and committed the file
- Modified the file by adding a "Getting Started" section and committed the changes

### 2. Working with Branches
- Created a new branch named `feature-branch`
- Modified README.md by adding a "Features" section
- Committed the changes and merged `feature-branch` into `main`
- Pushed the changes to the GitHub repository

### 3. Handling Merge Conflicts
- Created two separate branches: `branch1` and `branch2`
- Modified the same line in README.md in both branches
- Merged `branch1` into `main`
- Attempted to merge `branch2` which created a merge conflict
- Resolved the conflict manually by combining both changes
- Committed the resolution and pushed to GitHub

### 4. Implementing a Git Hook
- Created a pre-commit hook that prevents committing `.log` files
- Made the hook executable
- Tested the hook by attempting to commit a `.log` file
- Verified that the hook successfully rejected the commit

### 5. Setting Up a CI/CD Pipeline
- Created a GitHub Actions workflow file in `.github/workflows/ci.yml`
- Configured the workflow to run on push events to the `main` branch
- Set up steps for installing dependencies, running tests, and linting code
- Committed and pushed the workflow file to GitHub

## Challenges and Solutions

### Challenge 1: Merge Conflicts
When merging `branch2` into `main` after already merging `branch1`, a conflict occurred because both branches modified the same line in the README.md file. This was resolved by manually editing the file to combine both changes in a meaningful way, then committing the resolution.

### Challenge 2: Git Hooks
Implementing the pre-commit hook required understanding the Git hooks mechanism and shell scripting. The solution involved creating a script that checks for `.log` files in the staged changes and rejects the commit if any are found. Making the script executable was crucial for the hook to function properly.

### Challenge 3: GitHub Actions Configuration
Setting up the CI/CD pipeline required understanding the YAML syntax for GitHub Actions workflows. The solution involved creating a workflow file that defines the build environment, dependencies, and test commands.

## Conclusion

This project successfully demonstrated the use of Git for version control, including branch management and conflict resolution, as well as implementing Git hooks for enforcing commit policies and setting up a CI/CD pipeline using GitHub Actions. These skills are essential for modern software development workflows and ensure code quality and consistency across team projects.
