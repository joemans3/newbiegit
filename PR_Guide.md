# Beginner's Guide to Pull Requests

This guide will walk you through the process of creating a pull request (PR) on GitHub. We've made this guide especially for beginners who are new to GitHub and coding!

## What is a Pull Request?

A pull request is a way to suggest changes to a project's code. Instead of just pointing out a problem (an issue), you're actually providing the solution too!

## Prerequisites

Before making a pull request, you'll need:
1. A GitHub account
2. Git installed on your computer
3. Basic knowledge of the command line

Don't worry if these seem intimidating - we'll guide you through each step!

## Step-by-Step Process

### Step 1: Fork the Repository
1. Go to our GitHub repository page
2. Click the "Fork" button in the upper right corner
3. This creates a copy of the repository in your GitHub account

### Step 2: Clone Your Fork to Your Computer
1. On your forked repository page, click the green "Code" button
2. Copy the URL shown
3. Open your command line/terminal
4. Navigate to where you want to store the project
5. Type: `git clone [paste-the-URL-you-copied]` and press Enter
   ```
   git clone https://github.com/YOUR-USERNAME/repository-name.git
   ```
6. Press Enter to create a local copy on your computer

### Step 3: Create a Branch
1. Change into the project directory:
   ```
   cd repository-name
   ```
2. Create a new branch with a descriptive name:
   ```
   git checkout -b descriptive-branch-name
   ```
   (Example: `git checkout -b fix-login-button` or `git checkout -b add-dark-mode`)

### Step 4: Make Your Changes
1. Open the project in your code editor
2. Make the changes you want to contribute
3. Save your changes

### Step 5: Commit Your Changes
1. Add your changes to the staging area:
   ```
   git add .
   ```
   (The period means "all files." You can also specify individual files)
2. Commit your changes with a meaningful message:
   ```
   git commit -m "Brief description of the changes you made"
   ```

### Step 6: Push Your Changes
1. Push your branch to your fork on GitHub:
   ```
   git push origin descriptive-branch-name
   ```

### Step 7: Create the Pull Request
1. Go to your fork on GitHub
2. You should see a prompt to create a pull request for your recently pushed branch
3. If not, click the "Pull requests" tab and then the "New pull request" button
4. Make sure the base repository is the original project and the base branch is usually "main" or "master"
5. Make sure the head repository is your fork and the compare branch is your branch
6. Click "Create pull request"

### Step 8: Fill Out the Pull Request Form
1. Give your pull request a clear title
2. In the description, explain:
   - What changes you made
   - Why you made them
   - How you tested them
   - Reference any related issues (type # followed by the issue number)
3. Click "Create pull request"

## After Submitting a Pull Request

1. Project maintainers will review your PR
2. They might ask for changes
3. If they request changes:
   - Make the changes on your local branch
   - Commit and push them to your fork
   - The PR will update automatically
4. Once approved, your changes will be merged into the main project!

## Common Issues and Solutions

### "My fork is behind the original repository"
If the original repository has been updated since you forked it:
1. Add the original repository as a remote:
   ```
   git remote add upstream https://github.com/original-owner/original-repository.git
   ```
2. Fetch the updates:
   ```
   git fetch upstream
   ```
3. Update your main branch:
   ```
   git checkout main
   git merge upstream/main
   ```
4. Create a new branch for your changes:
   ```
   git checkout -b new-feature-branch
   ```

### "I have merge conflicts"
If GitHub says you have merge conflicts:
1. Update your fork as described above
2. Merge the main branch into your feature branch:
   ```
   git checkout your-feature-branch
   git merge main
   ```
3. Resolve the conflicts in your code editor
4. Commit the resolved changes and push again

## Final Tips

- **Small PRs are better**: Focus on a single bug fix or feature per PR
- **Be patient**: Maintainers are often volunteers with limited time
- **Respond to feedback**: Be open to making changes based on reviews
- **Test your changes**: Make sure your code works before submitting
- **Follow project guidelines**: Check for any specific contributing rules

Thank you for contributing to our project by submitting a pull request!
