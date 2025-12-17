Git and GitHub Hands-On Practice

Overview
This repository documents my hands-on learning with Git and GitHub. The focus of this practice was to work through real-world Git scenarios rather than only basic commands. I intentionally encountered common Git errors and learned how to resolve them step by step, similar to what happens in real development and DevOps environments.

Objectives

* Connect a local Git repository with GitHub
* Practice git fetch, git pull, and git push
* Understand GitHub authentication using Personal Access Tokens
* Resolve non-fast-forward push errors
* Handle divergent branches
* Merge unrelated histories
* Resolve merge conflicts manually

Step-by-Step Learning Process

1. Local and Remote Repository Setup
   I initialized a local Git repository and connected it to a remote repository on GitHub.

Commands used:
git init
git remote add origin [https://github.com/IPOUL2208/git-practice.git](https://github.com/IPOUL2208/git-practice.git)

2. Authentication Issue
   GitHub no longer supports password-based authentication for Git operations.

Resolution:

* Created a GitHub Personal Access Token
* Used the token as the password when performing Git operations over HTTPS

3. Non-Fast-Forward Push Error
   While pushing local commits, Git rejected the push because the remote branch had commits that were not present locally.

Reason:

* The GitHub repository already contained commits created directly on GitHub.

Resolution:
git pull origin main

4. Divergent Branches
   Git reported that local and remote branches had diverged and required a reconciliation strategy.

Resolution:
Explicitly chose how to integrate changes using pull options instead of default behavior.

5. Unrelated Histories Error
   Git refused to merge because the local repository and the GitHub repository were created independently.

Resolution:
git pull origin main --allow-unrelated-histories

6. Merge Conflict Resolution
   A merge conflict occurred because both local and remote repositories contained a README file.

Resolution steps:

* Opened the conflicted file
* Manually reviewed and edited the content
* Removed conflict markers
* Staged the resolved file

Commands used:
git add README.md
git rebase --continue

7. Final Push
   After resolving conflicts and completing the merge, the repository was successfully pushed to GitHub.

Command used:
git push origin main

Key Learnings

* Git errors provide guidance on how to safely manage version control
* Pulling before pushing is essential in collaborative environments
* Merge conflicts are normal and manageable
* Understanding merge vs rebase is critical for clean Git history
* These scenarios are common in real-world DevOps and software development teams

Conclusion
This hands-on practice strengthened my understanding of Git and GitHub workflows. It helped me gain confidence in troubleshooting and resolving real issues that occur during collaboration, which is essential for DevOps and software engineering roles.

Continuous learning in progress.
