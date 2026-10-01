### Question 1: What did `--global` mean here? What would happen if you left it out?
`--global` tells Git to apply this configuration setting (your name and email) system-wide for your user account across all repositories on your computer, rather than just the current repository. If you left it out, the configuration would only apply to the current directory/repository, and Git wouldn't know your identity if you started a new project elsewhere unless you configured it again.



### Question 2: What appeared in `ls -a` but not in `ls`? What is inside it?
The hidden `.git` directory appeared in `ls -a` (hidden files/folders starting with a dot are omitted by standard `ls`). Inside it are Git's internal metadata and database files (such as objects, refs, config, and hooks) that track your repository's history and configuration. 



### Question 3; Roughly how many files and folders is Git offering to track? Does anything in that list look like something you did not write?
6 files and folders
Yes, `.DS_Store`



### Question 4: Compare this `git status` with the one from Question 3. What disappeared?
The `.venv/` folder and everything inside it disappeared from the untracked files list because `.gitignore` told Git to ignore it.



### Question 5: `.gitignore` itself shows up as untracked. Should it be committed, or ignored too? Why?
It should be committed. `.gitignore` is a configuration file that dictates project rules for everyone working on the repository, so it needs to be tracked and shared via version control so that anyone who clones the repo also ignores those same unwanted files.



### Question 6: `README.md` moved from one heading to another in the `git status` output. Which two? In the three-places model from the session, what just happened to it?
It moved from "Untracked files" into "Changes to be committed". In the three-places model, it moved from the Working Directory into the Staging Area (Index).



### Question 7: What did Git print after the commit? How many files did it say changed?
Git printed a summary message showing the branch name (`main`), root-commit indicator, commit hash, commit message, and statistics. It stated that 8 files changed with corresponding insertions.



### Question 8: What are the first seven characters of your commit called, and what are they for?
They are called the commit hash(For example, mine is f100c75). They also provide a unique identifier for that specific commit/snapshot so you can reference, inspect, or revert to it in the history.



### Question 9: You now have two commits. Without looking it up: what are the four steps of the loop you just did twice?
Edit, Check status, Stage and Commit



### Question 10: Why does this file get a special name and a special place, rather than being called notes.md like everything else?
README.md sits in the root directory and has that specific name because code-hosting platforms like GitHub automatically look for it to render as the main front page / documentation when visitors land on my repository.



### Question 11: What did gh auth login do that means you will not be asked for a password when you push?
It securely stored an authentication token and configured Git's credential helper on my laptop so that my identity and permissions are authenticated automatically over HTTPS without requiring me to manually type a password or Personal Access Token for every push.



### Question 12: Refresh the repository page on GitHub. What is showing on the front page, and why that file?
README.md file contents are rendered on the front page because GitHub automatically scans the root directory of a repository for a README.md file to display as the default project overview.



### Question 13: Run git log --oneline again. Did pushing change your local history in any way?
No, pushing did not change my local history at all. Pushing simply copies my existing local commits and uploads them to the remote server on GitHub; it leaves my local commit hashes and history completely untouched.



### Question 14: Your repository is private but your TAs can now read it. In your own words, what is the difference between a repository being private and a repository not existing on GitHub at all?
A private repository exists securely on GitHub with all its history and code, but access is restricted exclusively to me and explicitly invited collaborators/TAs. If a repository does not exist on GitHub at all, no server holds a copy of it, meaning it is entirely unavailable online for anyone else to access, clone, or review.