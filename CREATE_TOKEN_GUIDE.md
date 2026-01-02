# How to Create a GitHub Personal Access Token

## Step-by-Step Instructions:

### 1. Go to GitHub Token Settings
- Open your web browser
- Go to: **https://github.com/settings/tokens**
- Or navigate: GitHub.com → Click your profile picture (top right) → **Settings** → Scroll down to **Developer settings** (left sidebar) → **Personal access tokens** → **Tokens (classic)**

### 2. Generate New Token
- Click the **"Generate new token"** button
- Select **"Generate new token (classic)"**

### 3. Configure Your Token
- **Note**: Give it a name like "My MacBook Token" or "GIT_NW Repository"
- **Expiration**: Choose how long it should last (30 days, 90 days, or no expiration)
- **Select scopes**: Check the box for **`repo`** (this gives full control of private repositories)
  - This includes all the permissions you need to push/pull

### 4. Generate and Copy
- Click **"Generate token"** at the bottom
- **IMPORTANT**: Copy the token immediately! It looks like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`
- You won't be able to see it again after you leave this page
- Save it somewhere safe (password manager, notes app, etc.)

### 5. Use the Token When Pushing
When you run `git push origin main`, it will ask for:
- **Username**: Your GitHub username
- **Password**: Paste your Personal Access Token (NOT your GitHub password)

### Alternative: Store Token in Git Credential Helper
After the first push, you can configure Git to remember your token:

```bash
git config --global credential.helper osxkeychain
```

This will save your token in macOS Keychain so you don't have to enter it every time.

