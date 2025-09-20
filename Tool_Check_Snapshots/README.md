### Step 1: Initialize a Git Repository

First, you need to create a local Git repository in the directory where your files are located. Navigate to the folder containing your document and images (`gtkwave.jpeg`, `iverilog.jpeg`, `yosys.jpg`).

```bash
cd /path/to/your/project
git init
```

This command initializes an empty Git repository.

### Step 2: Create a Repository on GitHub

Go to your GitHub account and create a **new repository**. You can give it a name like `RISC-V-Reference-SoC-Tools`. **Do not initialize the new repository with a README, .gitignore, or license file** as you will be pushing an existing project.

### Step 3: Add Files to the Repository

Next, add all your project files to the staging area.

```bash
git add .
```

This command stages all the new and modified files in the current directory.

### Step 4: Commit the Files

Commit the staged files with a descriptive message.

```bash
git commit -m "Initial commit of FPGA tool installation guide and images"
```

This creates the first commit in your local repository.

### Step 5: Connect to the Remote Repository

Now, you need to link your local repository to the one you created on GitHub. Replace `<your_username>` and `<your_repository_name>` with your actual GitHub username and repository name.

```bash
git remote add origin https://github.com/<your_username>/<your_repository_name>.git
```

This command tells Git where your remote repository is located.

### Step 6: Push to GitHub

Finally, push your committed files from your local repository to the remote repository on GitHub.

```bash
git push -u origin master
```

This uploads all the files, including the document and images, to your GitHub repository. The `-u` flag sets the upstream branch, so future `git push` commands will be simpler (`git push`).

Your files are now on GitHub. You can verify this by refreshing the repository page in your browser.
