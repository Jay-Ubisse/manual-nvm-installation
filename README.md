# 📘 Manual Installation of NVM for Windows (ZIP Version)

This guide walks you through installing [NVM for Windows](https://github.com/coreybutler/nvm-windows) manually using the `nvm-noinstall.zip` file. This is useful if you prefer not to use the installer.

---

## 🧰 Requirements

- Windows OS
- Admin permissions (for editing environment variables)
- Access to GitHub to download the ZIP file

---

## 🔽 Step 1: Download NVM ZIP

1. Go to the [NVM for Windows GitHub releases page](https://github.com/coreybutler/nvm-windows/releases).
2. Download the latest `nvm-noinstall.zip` file.

---

## 📂 Step 2: Extract Files

1. Extract the contents of the ZIP file to a folder of your choice, e.g.:

```
C:\nvm
```

---

## ⚙️ Step 3: Configure Environment Variables

### 3.1 Open Environment Variables

- Press `Win + R`, type `sysdm.cpl`, and press **Enter**.
- Go to the **Advanced** tab → click **Environment Variables**.

### 3.2 Add User Variables

| Variable Name | Value                      |
|---------------|----------------------------|
| `NVM_HOME`    | `C:\nvm`                   |
| `NVM_SYMLINK` | `C:\Program Files\nodejs`  |

> 🔁 Replace the paths if you used a custom directory.

### 3.3 Add to System/User `Path`

Add the following to the **Path** variable:

```
%NVM_HOME%
%NVM_SYMLINK%
```

---

## 📝 Step 4: Create `settings.txt`

In the `C:\nvm` folder, create a new file named `settings.txt` with the following content:

```ini
root: C:\nvm
path: C:\Program Files\nodejs
arch: 64
proxy: none
node_mirror: https://nodejs.org/dist/
npm_mirror: https://github.com/npm/cli/archive/
```

> 📌 Adjust paths if you extracted to a different location.

---

## 📁 Step 5: Create Symlink Folder

Make sure this folder exists (create manually if needed):

```
C:\Program Files\nodejs
```

This is where NVM will place the active Node.js version.

---

## ✅ Step 6: Test NVM

Open **Command Prompt** and run:

```bash
nvm version
```

You should see the NVM version printed in the terminal. If not, double-check the steps above.

---

## 🚀 Step 7: Install and Use Node.js

Use NVM to install and switch between Node.js versions:

```bash
nvm install 20.11.1
nvm use 20.11.1
node -v
```

---

## 🎉 Done!

You're now ready to manage multiple Node.js versions on Windows using NVM manually.

---

## 📚 Resources

- [NVM for Windows GitHub](https://github.com/coreybutler/nvm-windows)
- [Node.js Downloads](https://nodejs.org/en/download)
