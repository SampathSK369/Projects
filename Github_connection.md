# Connecting GitHub and Git with Visual Studio Code (VSCode)

Here's a step-by-step guide to connect your GitHub repository with Git on your laptop and access/manage it through Visual Studio Code:

## Prerequisites
- Git installed on your laptop ([download here](https://git-scm.com/))
- GitHub account
- Visual Studio Code installed
- GitHub extension for VSCode (recommended)

## Step 1: Set Up Git in VSCode

1. **Open VSCode**
2. **Install the GitHub Extension**:
   - Go to Extensions (Ctrl+Shift+X)
   - Search for "GitHub"
   - Install "GitHub Pull Requests and Issues" by GitHub

3. **Configure Git in VSCode**:
   - Open Command Palette (Ctrl+Shift+P)
   - Type "Git: Enable" and select it
   - Set your Git path if not automatically detected

## Step 2: Connect GitHub Account to VSCode

1. **Sign in to GitHub**:
   - Open Command Palette (Ctrl+Shift+P)
   - Type "GitHub: Sign In" and select it
   - Choose "Sign in with GitHub.com"
   - Follow the browser authentication process

2. **Verify Connection**:
   - Check the bottom-left corner of VSCode
   - You should see your GitHub username

## Step 3: Clone a Repository (Two Methods)

### Method 1: Using VSCode Interface
1. Click the Source Control icon (left sidebar)
2. Click "Clone Repository"
3. Choose "Clone from GitHub"
4. Select a repository from your list or enter a URL
5. Choose a local folder to save it

### Method 2: Using Terminal
1. Open terminal in VSCode (Ctrl+`)
2. Navigate to your desired folder:
   ```bash
   cd path/to/your/folder
   ```
3. Clone the repository:
   ```bash
   git clone https://github.com/username/repository.git
   ```
4. Open the folder in VSCode:
   ```bash
   code repository-name
   ```

## Step 4: Daily Workflow in VSCode

### 1. Making Changes
- Edit files in VSCode as normal
- Changed files appear in Source Control view

### 2. Staging Changes
1. Open Source Control view (Ctrl+Shift+G)
2. Hover over changed files and click "+" to stage
3. Or stage all changes with the "+" at top

### 3. Committing Changes
1. Enter commit message in the text box
2. Click the checkmark icon to commit
3. (Optional) Check "Commit & Push" to push immediately

### 4. Pushing Changes
1. Click the "..." menu in Source Control
2. Select "Push"
3. Or use the sync icon in the status bar

### 5. Pulling Updates
1. Click the "..." menu in Source Control
2. Select "Pull"
3. Or use the sync icon in the status bar

## Step 5: Branch Management

### Create a New Branch
1. Click the branch name in bottom-left
2. Select "Create new branch"
3. Enter branch name
4. Select whether to switch to it immediately

### Switch Between Branches
1. Click the branch name in bottom-left
2. Select from the list of available branches

## Step 6: Handling GitHub Features in VSCode

### Create Pull Requests
1. Make changes and push to a branch
2. Open Command Palette (Ctrl+Shift+P)
3. Type "GitHub: Create Pull Request"
4. Fill in details and submit

### Review Pull Requests
1. Open Command Palette
2. Type "GitHub: View Pull Requests"
3. Select a PR to review
4. Add comments directly in the code

## Troubleshooting Common Issues

1. **Authentication Problems**:
   - Re-authenticate via Command Palette > "GitHub: Sign In"
   - Or set up SSH keys (more secure)

2. **Git Not Detected**:
   - Check Git is installed (`git --version` in terminal)
   - Set path in VSCode settings: `"git.path": "C:/path/to/git.exe"`

3. **Merge Conflicts**:
   - VSCode will highlight conflicts
   - Use the merge editor to resolve
   - Stage resolved files before committing

## Recommended VSCode Settings

Add these to your settings.json (Ctrl+, then open JSON):
```json
{
  "git.enableSmartCommit": true,
  "git.autofetch": true,
  "git.confirmSync": false,
  "github.gitProtocol": "https", // or "ssh" if configured
  "git.pruneOnFetch": true
}
```

## Summary

You now have a fully integrated Git/GitHub workflow in VSCode:
1. **Connect** your GitHub account
2. **Clone** repositories directly in VSCode
3. **Edit** files with full version control visibility
4. **Commit** and **push** changes with GUI or commands
5. **Manage branches** and **pull requests** without leaving your editor

This setup gives you seamless version control while you focus on coding in your preferred editor.