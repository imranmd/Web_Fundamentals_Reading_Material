**Step-by-Step Guide to Create a Repository in GitHub, Clone It Locally, Make a Change, and Raise a Pull Request (PR)**

**Problem Statement:**

You want to contribute to an open-source project hosted on GitHub. To do this, you need to create a new repository on GitHub, clone it to your local machine, make changes to the code, and then propose those changes to the project maintainers by raising a Pull Request (PR). This step-by-step guide will walk you through the process using simple commands.

**Step 1: Create a Repository in GitHub:**

1. Log in to your GitHub account or create a new one if you don't have one.
2. Click on the "+" icon in the top-right corner and select "New repository."
3. Choose a repository name, add a brief description, and select the visibility (public or private) as per your preference.
4. Optionally, you can initialize the repository with a README file, license, or .gitignore file based on your project's needs.
5. Click on the "Create repository" button to create the repository.

**Step 2: Clone the Repository Locally:**

1. Open your terminal or command prompt on your local machine.
2. Go to the location where you want to clone the repository using the `cd` command.
3. Copy the repository URL from the green "Code" button on the GitHub repository page (you can choose between HTTPS or SSH URLs).
4. In the terminal, run the command: `git clone <repository-url>` (replace `<repository-url>` with the URL you copied).

**Step 3: Make a Change and Commit:**

1. Navigate into the cloned repository using the `cd` command.
2. Open the files you want to modify using your favorite code editor.
3. Make the necessary changes to the code.
4. Save the changes in your code editor.

**Step 4: Commit the Changes:**

1. In the terminal, run the command: `git status` to see the changes you made.
2. Use the command: `git add .` to stage all the changes or `git add <file-name>` to stage specific files.
3. Run the command: `git commit -m "Your commit message"` to commit the changes with a meaningful message explaining what you did.

**Step 5: Push the Changes to GitHub:**

1. In the terminal, run the command: `git push origin main` (replace `main` with the name of your branch if it's different from the default branch).

**Step 6: Raise a Pull Request (PR):**

1. Go to your GitHub repository page and click on the "Pull Requests" tab.
2. Click on the green "New pull request" button.
3. Select the base and compare branches for your PR (usually, the base is the main branch and the compare branch is your feature branch).
4. Click on "Create pull request."
5. Add a descriptive title and comment explaining the changes you made.
6. Click on "Create pull request" to submit your PR.

**Summary:**

Congratulations! You have successfully created a new repository on GitHub, cloned it to your local machine, made changes to the code, and raised a Pull Request to propose your changes to the project maintainers. Remember to keep your PRs concise and well-documented to increase the chances of getting your contributions accepted into the project. Happy collaborating!