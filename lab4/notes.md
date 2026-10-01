Here are clear, concise answers for **Questions 1 through 8** to add to your `lab4/notes.md` file:

---

### **Question 1**

* **Question:** What did `--global` mean here? What would happen if you left it out?
* **Answer:**
* `--global` tells Git to apply this configuration setting (your name and email) system-wide for your user account across all repositories on your computer, rather than just the current repository.
* If you left it out, the configuration would only apply to the current directory/repository, and Git wouldn't know your identity if you started a new project elsewhere unless you configured it again.



---

### **Question 2**

* **Question:** What appeared in `ls -a` but not in `ls`? What is inside it?
* **Answer:**
* The hidden `.git` directory appeared in `ls -a` (hidden files/folders starting with a dot are omitted by standard `ls`).
* Inside it are Git's internal metadata and database files (such as objects, refs, config, and hooks) that track your repository's history and configuration. *(Remember: never manually delete or edit files inside `.git`!)*



---

### **Question 3**

* **Question:** Roughly how many files and folders is Git offering to track? Does anything in that list look like something you did not write?
* **Answer:**
* *[Fill in the approximate number based on what your `git status` showed, e.g., around 5–6 folders/files like `README.md`, `.DS_Store`, and folder directories like `week02/`, `week03/`, etc.]*
* Yes, `.DS_Store` (on macOS) and the thousands of files inside the `.venv/` folder are things you did not explicitly write; `.venv/` is someone else's virtual environment code.



---

### **Question 4**

* **Question:** Compare this `git status` with the one from Question 3. What disappeared?
* **Answer:**
* The `.venv/` folder and everything inside it disappeared from the untracked files list because `.gitignore` told Git to ignore it.



---

### **Question 5**

* **Question:** `.gitignore` itself shows up as untracked. Should it be committed, or ignored too? Why?
* **Answer:**
* It should be **committed**. `.gitignore` is a configuration file that dictates project rules for everyone working on the repository, so it needs to be tracked and shared via version control so that anyone who clones the repo also ignores those same unwanted files.



---

### **Question 6**

* **Question:** `README.md` moved from one heading to another in the `git status` output. Which two? In the three-places model from the session, what just happened to it?
* **Answer:**
* It moved from **"Untracked files"** into **"Changes to be committed"**.
* In the three-places model, it moved from the **Working Directory** into the **Staging Area** (Index).



---

### **Question 7**
What did Git print after the commit? How many files did it say changed?
* **Answer:**
* Git printed a summary message showing the branch name (`main`), root-commit indicator, commit hash, commit message, and statistics.
* It stated that **8 files changed** with corresponding insertions.





### **Question 8**
What are the first seven characters of your commit called, and what are they for?

They are called the commit hash (or short commit ID / SHA-1 hash prefix). They also provide a unique identifier for that specific commit/snapshot so you can reference, inspect, or revert to it in the history.


