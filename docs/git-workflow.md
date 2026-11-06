# Git workflow
Use Git Bash. Start in the prepared project folder. For a NEW remote repository, leave automatic README/license/.gitignore creation off.

```bash
git init
git branch -M main
git status
git add README.md .gitignore configs diagrams docs labs screenshots
git diff --cached --stat
git diff --cached
git commit -m "docs: initialize troubleshooting casebook and baseline"
git remote add origin https://github.com/kahrhm2970-source/network-troubleshooting-casebook.git
git remote -v
git push -u origin main
```

This published repository already has history. To continue it instead, clone it:

```bash
git clone https://github.com/kahrhm2970-source/network-troubleshooting-casebook.git
cd network-troubleshooting-casebook
```

After actual execution and evidence capture:

```bash
git add docs/incidents/INC-001-wrong-access-vlan.md screenshots/INC-001-before.png screenshots/INC-001-after.png labs/baseline.pkt
git diff --cached
git commit -m "lab: document access VLAN incident and recovery"
git push
```

Future messages: lab: document missing trunk VLAN incident; lab: document incorrect default gateway incident; docs: summarize verified results and lessons learned.

Review secrets, real IP addresses, credentials, .pkt content, and screenshots before staging. Use simulated addresses. Gitignore does not scrub tracked files or previous commits.
