# Homework #1: Git Workflow and History Management

## Overview
This repository contains the completed tasks for Homework #1. It demonstrates practical knowledge of Git workflows, history rewriting, commit recovery, and visual history management.

## Completed Tasks Breakdown

### 1 & 2. Initialization and Initial Commits
* Initialized a local Git repository.
* Created initial project files and made several sequential commits with unclear, non-descriptive messages.

### 3. History Cleanup
* Used interactive rebase (`git rebase -i`) to squash the messy history.
* Rewrote the commit history into a single, logical commit with a clear, descriptive multi-line message representing the complete initial setup.

### 4 & 5. Simulating a Mistake and Recovering Lost Work
* Purposely created a bad commit ("bad commit") and simulated losing it by performing a hard reset (`git reset --hard HEAD~1`).
* Utilized `git reflog` to trace the repository's action history, located the orphaned commit hash, and successfully recovered it.

### 6. Creating a New Branch
* Created and checked out a new branch named `recovered-branch` based directly on the recovered "bad commit" to safely isolate it from the clean `main` history.

### 7. Custom Git Alias
* Created a custom global Git alias to format the log into a readable, colorful tree graph.
* **Alias Command Used:** `git config --global alias.visual "log --oneline --graph --all"`

### 8. Tagging the Release
* Tagged the original, cleaned-up base commit of the project as version `1.0`.

### 9. Remote Push
* Pushed the cleaned `main` branch, the `recovered-branch`, and the `1.0` tag to this remote GitHub repository.

## Visual Verification

Below are the terminal outputs demonstrating the final state of the repository, the tags, the branches, and the successful execution of the custom alias.

### 1. Detailed Git Log
Shows the commit authors, dates, merge commits, the `1.0` tag, and the recovered branch.
![Git Log Detail](images/git-log.png)

### 2. Custom Visual Alias Output (`git visual`)
Displays the clean graph history, proving the successful squash, branching, and custom alias functionality.
![Git Visual Graph](images/git-visual.png)