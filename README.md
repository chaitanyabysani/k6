# ⚡ k6-mastery — Performance Testing Journey

> A day-by-day hands-on learning journal for mastering **Grafana k6** — the modern open-source load testing tool.
> Tool: **k6** | Language: **JavaScript**

---

## 👋 About This Repository

This repository documents my complete hands-on learning journey with **k6 performance testing** — from installation to advanced load testing scenarios. Every day I learn something new, I push it here with scripts, notes, and explanations.

**What you will find here:**
- ✅ Step-by-step setup guide (anyone can follow from scratch)
- 📅 Daily learning logs with scripts and descriptions
- 🧪 All 8 load test types with real examples
- 📂 Well-organized folder structure

> 💡 **If you are a complete beginner** — just follow this README from top to bottom. By the end you will have k6 fully set up and your first test running!

---

## 🗂️ Project Structure

```
k6-mastery/
│
├── tests/
│   ├── day-01/                  ← Day 01 scripts and notes
│   │   ├── smoke-test.js        ← First smoke test script
│   │   └── notes.md             ← What I learned on Day 01
│   ├── day-02/                  ← Day 02 scripts (coming soon)
│   └── ...
│
├── scripts/                     ← Reusable helper scripts
├── results/                     ← Test output and reports
├── docs/                        ← Reference notes and cheatsheets
├── .gitignore                   ← Files to ignore in Git
├── package.json                 ← Node.js project config
└── README.md                    ← You are reading this!
```

---

## 🛠️ Complete Setup Guide

Follow these steps **in order** to set up everything from scratch on your Windows machine.

---

### ✅ Step 1 — Install k6 on Windows

k6 is the core tool we use for performance testing.

1. Open your browser and go to:
   👉 [https://grafana.com/docs/k6/latest/set-up/install-k6/](https://grafana.com/docs/k6/latest/set-up/install-k6/)

2. Scroll down to the **Windows** section

3. Click on the **Official Installer** link — an `.exe` file will download

4. Once downloaded, **double-click** the `.exe` file and follow the installation steps

5. Click **Next → Next → Install → Finish**

> ✅ k6 is now installed on your machine!

---

### ✅ Step 2 — Set the PATH (Environment Variables)

After installation, Windows needs to know where k6 is located. This is called setting the **PATH**.

1. Press **`Windows Key + S`** → search **"environment variables"**
2. Click **"Edit the system environment variables"**
3. Click **"Environment Variables"** button at the bottom
4. Under **System Variables** → find **`Path`** → click **"Edit"**
5. Check if `C:\Program Files\k6` is already in the list
   - ✅ **If it's there** — you are good, click OK and close
   - ❌ **If it's NOT there** — click **"New"** → type `C:\Program Files\k6` → click OK

> 💡 The official `.exe` installer usually adds the PATH automatically. This step is just to verify it was added correctly.

---

### ✅ Step 3 — Verify k6 Installation

1. Press **`Windows Key + S`** → search **"cmd"** → open **Command Prompt**
2. Type this command and press Enter:

```bash
k6 version
```

✅ You should see something like:
```
k6 v1.0.0 (go1.22.0, windows/amd64)
```

❌ If you see **"not recognized"** — close and reopen the Command Prompt, then try again. If still not working, re-check Step 2.

---

### ✅ Step 4 — Install VS Code (Code Editor)

VS Code is the best editor for writing k6 scripts. It gives you syntax highlighting, autocomplete, and a built-in terminal.

1. Go to 👉 [https://code.visualstudio.com](https://code.visualstudio.com)
2. Click **"Download for Windows"**
3. Open the downloaded `.exe` file
4. During installation — make sure to **check these boxes** ✅:
   ```
   ✅ Add "Open with Code" action to Windows Explorer file context menu
   ✅ Add to PATH
   ```
5. Click **Install → Finish**

---

### ✅ Step 5 — Install Node.js

Node.js is required to manage packages like k6 type definitions (which give VS Code autocomplete for k6 functions).

1. Go to 👉 [https://nodejs.org](https://nodejs.org)
2. Download the **LTS version** (recommended for most users)
3. Open the `.exe` file → click **Next → Next → Install → Finish**
4. Verify installation — open a new Command Prompt and type:

```bash
node --version
npm --version
```

✅ You should see version numbers like `v20.x.x` and `10.x.x`

---

### ✅ Step 6 — Create a GitHub Repository

GitHub is where we store and track all our work online.

1. Go to 👉 [https://github.com](https://github.com) and log in
2. Click the **`+`** icon (top right corner) → click **"New repository"**
3. Fill in the details:
   - **Repository name:** `k6-mastery`
   - **Description:** `⚡ My day-by-day k6 performance testing learning journey`
   - **Visibility:** `Public` ✅
   - ❌ Do NOT check "Add README" (we will add our own)
4. Click **"Create repository"**

5. Copy the repo URL — it looks like:
```
https://github.com/YOUR_USERNAME/k6-mastery.git
```

> ✅ Your GitHub repository is now created and ready!

---

### ✅ Step 7 — Clone the Repository to Your Local Machine

Cloning means downloading a copy of the GitHub repo to your Windows PC so you can work on it locally.

1. Open **File Explorer**
2. Navigate to the folder where you want to keep your projects
   for example: `C:\Projects\` or `Documents\`
3. **Right-click** inside the folder → select **"Open in Terminal"** or **"Git Bash Here"**
4. In the terminal that opens, type:

```bash
git clone https://github.com/YOUR_USERNAME/k6-mastery.git
```

> Replace `YOUR_USERNAME` with your actual GitHub username. For example:
> ```bash
> git clone https://github.com/chaitanyabysani/k6.git
> ```

5. Press **Enter** — you will see:
```
Cloning into 'k6-mastery'...
remote: Enumerating objects: done.
✅ done.
```

> ✅ The repository is now downloaded to your local machine!

---

### ✅ Step 8 — Open the Project in VS Code

1. Open **VS Code**
2. Click **File → Open Folder**
3. Navigate to and select the `k6-mastery` folder you just cloned
4. Click **"Select Folder"**

> 💡 **Shortcut:** You can also right-click the `k6-mastery` folder in File Explorer and select **"Open with Code"**

The project folder will now be open in VS Code on the left sidebar.

---

### ✅ Step 9 — Open the VS Code Terminal

All the following commands will be run inside VS Code's built-in terminal.

1. In VS Code, click **Terminal** in the top menu
2. Click **"New Terminal"**

OR press the keyboard shortcut:
```
Ctrl + `   (backtick key — top left of keyboard, below Escape)
```

You will see a terminal open at the bottom of VS Code.

---

### ✅ Step 10 — Initialize a Node.js Project

This creates a `package.json` file which is the configuration file for your project. It tracks all the packages and tools you install.

In the VS Code terminal, type:

```bash
npm init -y
```

✅ You will see a `package.json` file created in your project with content like:
```json
{
  "name": "k6-mastery",
  "version": "1.0.0",
  "description": "",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  }
}
```

> 💡 The `-y` flag means "yes to all default settings" — it skips all the manual questions.

---

### ✅ Step 11 — Add a .gitignore File

A `.gitignore` file tells Git which files and folders to **ignore** and NOT upload to GitHub. This is important because the `node_modules` folder can contain thousands of files that don't need to be in GitHub.

1. In VS Code, click the **"New File"** icon in the left sidebar
2. Name the file exactly: **`.gitignore`**
3. Press **Enter**
4. Add this content inside the file:

```gitignore
# Node modules — never upload this to GitHub (thousands of files)
node_modules/

# k6 test results and reports
results/
*.json
*.csv

# VS Code personal settings
.vscode/

# Windows junk files
Thumbs.db

# Mac junk files
.DS_Store

# Environment / secret files — never upload!
.env
```

5. Save with **`Ctrl + S`**

> ⚠️ **Important:** Never upload `node_modules/` to GitHub. It can be hundreds of MB in size and is automatically recreated by running `npm install`.

---

### ✅ Step 12 — Install k6 IntelliSense (Autocomplete)

This installs **k6 type definitions** which give you autocomplete suggestions in VS Code while writing k6 scripts. When you type `http.` it will suggest available functions automatically.

In the VS Code terminal, type:

```bash
npm install --save-dev @types/k6
```

✅ You will see `node_modules/` folder created and `package.json` updated with:
```json
"devDependencies": {
  "@types/k6": "^0.x.x"
}
```

> 💡 **What does `--save-dev` mean?** It means this package is only needed during development (writing code), not when actually running tests.

---

### ✅ Step 13 — Verify Everything is Set Up

Run these commands one by one to confirm everything is working:

```bash
# Check k6
k6 version

# Check Node.js
node --version

# Check npm
npm --version

# Check Git
git --version
```

✅ If all 4 commands show version numbers — your setup is **100% complete!** 🎉

---

### ✅ Day 1

**🎯 Topics Covered:**
- Complete setup of k6 on Windows
- GitHub repository creation and cloning
- VS Code setup and Node.js initialization
- Adding .gitignore and k6 type definitions
- Added different load testing types and their details in the README for quick reference

**🛠️ What I Did:**
- Created the `k6` GitHub repository
- Set up the project structure with folders for tests, scripts, results, and docs
- Added a detailed README with setup instructions and load testing types   

**📂 Files Created:**
- `README.md` — This file with all the setup instructions and reference information
- `.gitignore` — To ignore node_modules and other unnecessary files
- `package.json` — Node.js project configuration file
- `node_modules/` — Created after installing @types/k6 (not uploaded to GitHub)

---

## 🧪 All 8 Load Testing Types — Quick Reference

| # | Test | Users | Duration | What It Checks |
|---|------|-------|----------|----------------|
| 1 | 💨 Smoke | 1–2 | 1–5 min | Is the app alive? |
| 2 | 📈 Load | 10–100 | 5–30 min | Normal day performance |
| 3 | 🏋️ Stress | 100–500+ | 10–60 min | Where does it break? |
| 4 | ⚡ Spike | 10→1000→10 | 5–10 min | Sudden traffic surge |
| 5 | 🛁 Soak | 50–100 | Hours/Days | Long-term stability |
| 6 | 💥 Breakpoint | ∞ ramp | Until break | Exact max capacity |
| 7 | 📦 Volume | Moderate | Variable | Handling large data |
| 8 | 📐 Scalability | Stepped | Multi-run | Does scaling help? |

> 💡 **Beginner tip:** Always run Smoke → Load → Stress in that order. Never skip the Smoke test!

---

## 📤 Daily Git Workflow

Every day after completing your work, push it to GitHub using these 3 commands:

```bash
# Stage all your changes
git add .

# Commit with a meaningful message
git commit -m "📅 Day 02 - Load test with ramp up and ramp down"

# Push to GitHub
git push
```

> 💡 **Good commit message examples:**
> - `📅 Day 02 - Load test with stages`
> - `✅ Day 03 - Stress test script added`
> - `📝 Day 04 - Added notes on spike testing`

---

## 🆘 Common Issues & Fixes

| Problem | Cause | Fix |
|---------|-------|-----|
| `k6 not recognized` | PATH not set or terminal not restarted | Close and reopen terminal. Re-check Step 2 |
| `git not recognized` | Git not installed | Download from [git-scm.com](https://git-scm.com) |
| `npm not recognized` | Node.js not installed | Download from [nodejs.org](https://nodejs.org) |
| `code .` doesn't open VS Code | VS Code not in PATH | Reinstall VS Code with "Add to PATH" ✅ checked |
| `Repository not found` when cloning | Wrong URL | Double check the copied GitHub URL |
| `Permission denied` when pushing | Not logged into GitHub | Run `git config --global user.name "Your Name"` first |
| `node_modules` uploaded to GitHub | Missing `.gitignore` | Add `.gitignore` with `node_modules/` and push again |

---

## 🛠️ Tools & Technologies

| Tool | Purpose | Link |
|------|---------|-------|
| k6 | Load testing engine | [k6.io](https://k6.io) |
| VS Code | Code editor | [code.visualstudio.com](https://code.visualstudio.com) |
| Node.js | Package management | [nodejs.org](https://nodejs.org) |
| Git | Version control | [git-scm.com](https://git-scm.com) |
| GitHub | Remote repository | [github.com](https://github.com) |
| @types/k6 | k6 autocomplete in VS Code | npm package |

---

## 📚 Useful Resources

- 📖 [Official k6 Documentation](https://grafana.com/docs/k6/latest/)
- 🧪 [k6 Test Types Guide](https://grafana.com/docs/k6/latest/testing-guides/test-types/)
- 💬 [k6 Community Forum](https://community.grafana.com/c/grafana-k6/)
- ⭐ [k6 GitHub Repository](https://github.com/grafana/k6)
- 🎓 [k6 Examples](https://grafana.com/docs/k6/latest/examples/)

---

## 📝 Author

**Chaitanya Bysani** — Learning k6 performance testing in public, one day at a time.

🔗 GitHub: [github.com/chaitanyabysani](https://github.com/chaitanyabysani)

> ⭐ If you find this repository helpful, please give it a star — it motivates me to keep learning and sharing!

---

*Happy Testing! 🚀*