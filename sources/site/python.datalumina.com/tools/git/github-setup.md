# Source: https://python.datalumina.com/tools/git/github-setup

## 

[​](https://python.datalumina.com/#create-your-github-account)

Create your GitHub account

GitHub is free and takes 5 minutes to set up. You’ll need it to:

- Back up your code
- Share your projects
- Download AI tools and examples

## 

[​](https://python.datalumina.com/#step-1-sign-up)

Step 1: Sign up

1. Go to [github.com](https://github.com)
2. Click “Sign up”
3. Enter:
 - **Username**: Pick something professional (employers will see this)
 - **Email**: Use one you check regularly
 - **Password**: Make it strong

## 

[​](https://python.datalumina.com/#step-2-verify-your-account)

Step 2: Verify your account

GitHub will send you an email. Click the link to verify.

## 

[​](https://python.datalumina.com/#step-3-set-up-your-profile)

Step 3: Set up your profile

Once logged in:

1. Click your profile picture (top right) > “Your profile”
2. Click “Edit profile”
3. Add:
 - **Name**: Your real name
 - **Image**: Add a profile picture
 - **Bio**: “Learning Python for AI development” (or similar)

## 

[​](https://python.datalumina.com/#step-4-configure-git-locally)

Step 4: Configure Git locally

Tell Git who you are (one-time setup):

```
# Open terminal in VS Code (Terminal > New Terminal)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Use the same email you used for GitHub.

## 

[​](https://python.datalumina.com/#step-5-choose-your-authentication-method)

Step 5: Choose your authentication method

There are three ways to authenticate with GitHub. Choose one:

**Recommended**: We suggest using GitHub CLI for the easiest setup experience. It’s modern, simple, and handles authentication automatically.

- GitHub CLI (Recommended)
 
- HTTPS with Token
 
- SSH Keys
 

### 

[​](https://python.datalumina.com/#github-cli-gh)

GitHub CLI (gh)

Modern approach using GitHub’s official tool:

1. Install GitHub CLI:
 - **Windows**: Download from [cli.github.com](https://cli.github.com)
 - **macOS**: `brew install gh`
 - **Linux**: See [installation guide](https://github.com/cli/cli#installation)
2. Authenticate:

```
gh auth login
```

3. Follow the prompts:
 - Choose GitHub.com
 - Choose SSH (recommended) or HTTPS
 - Authenticate with browser

That’s it! Git will automatically use your gh credentials.

### 

[​](https://python.datalumina.com/#personal-access-token)

Personal Access Token

Traditional method using tokens:

1. Go to GitHub Settings (click profile > Settings)
2. Scroll down to “Developer settings” (left sidebar)
3. Click “Personal access tokens” > “Tokens (classic)”
4. Click “Generate new token” > “Generate new token (classic)”
5. Give it a name like “My Laptop” or “VS Code”
6. Select scopes: check `repo` (full control of repositories)
7. Set expiration (or no expiration for convenience)
8. Click “Generate token”
9. **Copy the token immediately** (you won’t see it again!)

Save your token somewhere safe! You’ll need it when pushing code.

### 

[​](https://python.datalumina.com/#using-your-token)

Using your token

When you push code for the first time:

```
git push

# GitHub will ask for:
Username: your-github-username
Password: paste-your-token-here (NOT your GitHub password!)
```

### 

[​](https://python.datalumina.com/#ssh-keys)

SSH Keys

The most secure method - no passwords needed:

1. Generate SSH key:

```
ssh-keygen -t ed25519 -C "your_email@example.com"
# Just press Enter for all prompts (accept defaults)
```

2. Add to ssh-agent:

- macOS/Linux
 
- Windows
 

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

```
# In Git Bash (not Command Prompt):
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

3. Copy your public key:

```
# macOS
pbcopy < ~/.ssh/id_ed25519.pub

# Windows (Git Bash)
cat ~/.ssh/id_ed25519.pub | clip

# Linux
cat ~/.ssh/id_ed25519.pub
# Then manually copy the output
```

4. Add to GitHub:
 - Go to [GitHub Settings > SSH Keys](https://github.com/settings/keys)
 - Click “New SSH key”
 - Give it a title (e.g., “My Laptop”)
 - Paste your key
 - Click “Add SSH key”
5. Test the connection:

```
ssh -T git@github.com
# You should see: "Hi username! You've successfully authenticated..."
```

**Important**: When cloning, use SSH URLs:

```
# SSH URL (what you want)
git clone git@github.com:username/repo.git

# Not HTTPS URL
git clone https://github.com/username/repo.git
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now let’s learn how to create your first repository and clone existing projects.

[**Clone and create**\\ \\ Start using GitHub](https://python.datalumina.com/tools/git/clone-create)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/git/github-setup.mdx)

[Version control](https://python.datalumina.com/tools/git/version-control) [Clone and create](https://python.datalumina.com/tools/git/clone-create)

Ctrl+I