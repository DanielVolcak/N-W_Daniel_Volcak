# Git and GitHub Setup Guide

## Step 1: Configure Git (First Time Setup)

Run these commands to set your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Step 2: Authenticate with GitHub

You have two options:

### Option A: Using Personal Access Token (Recommended for beginners)

1. Go to GitHub.com → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate a new token with `repo` permissions
3. Copy the token (you'll use it as your password)

### Option B: Using SSH Keys (More secure, recommended for regular use)

1. Generate an SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```
2. Copy your public key:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
3. Go to GitHub.com → Settings → SSH and GPG keys → New SSH key
4. Paste your public key

## Step 3: Connect to Your GitHub Repository

### If you already created a repository on GitHub:

1. Get your repository URL from GitHub (click the green "Code" button)
2. Clone it:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   ```

### If you want to connect this folder to your GitHub repository:

1. Initialize git in this folder:
   ```bash
   git init
   ```

2. Add your GitHub repository as remote:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   ```

3. Pull existing files (if any):
   ```bash
   git pull origin main
   ```
   (or `git pull origin master` if your default branch is master)

## Step 4: Working with Your Repository

### Basic Workflow:

1. **Check status:**
   ```bash
   git status
   ```

2. **Add files:**
   ```bash
   git add .                    # Add all files
   git add filename.txt         # Add specific file
   ```

3. **Commit changes:**
   ```bash
   git commit -m "Your commit message"
   ```

4. **Push to GitHub:**
   ```bash
   git push origin main
   ```
   (or `git push origin master`)

5. **Pull latest changes:**
   ```bash
   git pull origin main
   ```

## Troubleshooting

- **Authentication issues:** Make sure you're using a Personal Access Token (not your GitHub password) when using HTTPS
- **Permission denied:** Check that your SSH key is added to GitHub (for SSH) or your token has correct permissions (for HTTPS)

