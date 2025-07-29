# GitLab Console Access

All private repositories are stored on the School's internal gitlab server. 


To access it via the console without username/password, **add your SSH key to Gitlab** by clicking on your **Avatar -> Edit Profile -> SSH Keys -> Add new key**


### 🔐 1. Check for existing SSH keys
Open a terminal and run:

```ls -al ~/.ssh```

Look for files like id_rsa and id_rsa.pub (or id_ed25519 and id_ed25519.pub). If they exist, you may already have an SSH key.

### 🗝️ 2. Generate a new SSH key (if needed)
If you don’t have one or want a new key:

```ssh-keygen -t ed25519 -C "your_email@example.com"```

If your system doesn’t support ed25519, use:

```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```

Press Enter to accept the default file location, and optionally set a passphrase.

### 📋 3. Add your SSH key to the SSH agent
Start the agent:

```eval "$(ssh-agent -s)"```

Then add your key:

```ssh-add ~/.ssh/id_ed25519```


### 📤 4. Copy your public key
Run:

```cat ~/.ssh/id_ed25519.pub```

Copy the output to your clipboard.

### 🧷 5. Add the key to GitLab
  - Go to GitLab.
  - Click your avatar → Edit profile → SSH Keys.
  - Paste your key into the "Key" field.
  - Add a title and expiration date (optional).
  - Click Add key.

### ✅ 6. Test the connection

Run:

```ssh -T git@gitlab.com```


You should see a message like:

```Welcome to GitLab, @yourusername!```

