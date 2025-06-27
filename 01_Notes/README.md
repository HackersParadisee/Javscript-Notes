# JavaScript-Notes

---

## 📘 Chapter 1: Setup and Configuration – Dev Container with GitHub Codespaces

Before writing any JavaScript or Node.js code, it’s important to have a consistent and reliable development environment — and that’s where GitHub Codespaces come in. Codespaces provide a full-featured, cloud-based coding environment with preinstalled tools, a terminal, and VS Code-like editor, all accessible directly from the browser. By setting up a Dev Container, you ensure that every developer (including your future self) works in the same environment with the correct Node.js version, required extensions, and project dependencies. This setup avoids the common “works on my machine” issues and saves time spent configuring systems, making your workflow cleaner, portable, and more professional.

---

**Step 1: Open GitHub Repository in Codespace**  
Navigate to your repository on GitHub.  
Click the **Code** button, then choose:  
> **Codespaces > Create codespace on main**

---

**Step 2: Add Dev Container Configuration**  
Once inside the Codespace, open the **Command Palette**:  
> Press `Ctrl+Shift+P` (or `F1`)  
Search for and select:  
> `Dev Containers: Add Dev Container Configuration Files`

---

**Step 3: Choose a Template**  
From the available templates, select:  
> `Node.js`  
Then, choose the Node.js version you need (e.g., `Node.js 20`).

This will create a `.devcontainer` folder with the following files:
- `devcontainer.json`
- A Docker-based image definition or reference

---

**Step 4: Optional – Customize Configuration**  
You can edit the `devcontainer.json` file to automatically include useful VS Code extensions and to install dependencies after setup:

```json
"customizations": {
  "vscode": {
    "extensions": [
      "dbaeumer.vscode-eslint",
      "esbenp.prettier-vscode"
    ]
  }
},
"postCreateCommand": "npm install"
```
---
---



