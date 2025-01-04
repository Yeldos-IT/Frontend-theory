### **Git — Complete and Concise Overview**

---

#### **1. Key Concepts**
- **Repository:** A storage for your code and its change history.
  ```bash
  git init             # Initialize a new repository
  git clone [URL]      # Clone an existing repository
  git status           # Check repository status
  ```

- **Commits:** Snapshots of your code changes.
  ```bash
  git add [file]       # Stage changes
  git commit -m "Message"  # Commit changes with a message
  git log              # View commit history
  ```

- **Branches:** Work on different code versions simultaneously.
  ```bash
  git branch [name]    # Create a new branch
  git checkout [name]  # Switch to a branch
  git merge [name]     # Merge a branch into the current one
  ```

- **Remote Repositories:** Work with remote servers like GitHub.
  ```bash
  git remote add origin [URL]  # Connect to a remote repository
  git push origin [branch]     # Push changes to remote
  git pull origin [branch]     # Fetch and merge changes from remote
  ```

#### **2. Advanced Topics**

- **Undoing Changes:**
  ```bash
  git reset HEAD [file]        # Unstage changes
  git checkout -- [file]       # Discard changes in a file
  ```

- **Handling Conflicts:**
  - Occurs when merging branches with conflicting changes.
  - Steps:
    1. Attempt merge: `git merge [branch]`
    2. Manually resolve conflicts in files.
    3. Stage resolved files: `git add [file]`
    4. Commit: `git commit`

- **Rebase:**
  - Reapply commits from one branch onto another.
  ```bash
  git rebase [branch]
  ```

#### **3. Helpful Commands**

- **View Changes:**
  ```bash
  git diff             # Show changes between commits or working directory
  ```

- **Tags:**
  - Mark specific points in history.
  ```bash
  git tag [name]       # Create a tag
  git push origin [name] # Push a tag to remote
  ```

- **Stashing:** Temporarily save changes.
  ```bash
  git stash            # Save changes
  git stash apply      # Reapply stashed changes
  ```
