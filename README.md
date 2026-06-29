# 💼 Rig Builder Community Workspace

Welcome to the **Rig Builder Community Workspace**! This repository serves as a centralized, open-source registry of community-contributed modules, tools, and scripts designed to run seamlessly within **[Rig Builder](https://github.com/azagoruyko/rigBuilder)**.

Whether you are a Technical Artist, Rigger, or Pipeline Developer, this workspace provides production-ready building blocks to accelerate your rigging and automation workflows across Autodesk Maya, Blender, Unreal Engine, and more.

## ⚙️ How to Setup and Use

The preferred way to use this repository is to clone it directly into your Rig Builder `workspaces` directory. This makes it instantly loadable as a first-class workspace in the application.

### Option A: Clone Directly to Workspaces Folder (Preferred)

1. **Navigate to your Rig Builder workspaces folder:**
   By default, workspaces are stored under your user directory at `~/rigBuilder/workspaces/` (e.g., `C:\Users\<YourUsername>\rigBuilder\workspaces` on Windows).

2. **Clone the repository:**
   Clone the repository directly into that folder under the name `community`:

   ```bash
   cd ~/rigBuilder/workspaces
   git clone https://github.com/azagoruyko/rigBuilder-community.git community
   ```

3. **Switch Workspace in Rig Builder:**
   * Launch **Rig Builder**.
   * Open the workspace selector and switch to the **`community`** workspace.
   * The community modules will instantly populate your **Module Browser**!

---

### Option B: Register from a Custom Folder

If you prefer to keep the cloned repository elsewhere:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/azagoruyko/rigBuilder-community.git
   ```

2. **Configure in Rig Builder:**
   * Launch **Rig Builder** and open the **Workspace Manager** (via the workspace selector or settings).
   * Click **➕ (New Workspace)** and name it `community` (or any preferred name).
   * Under **Modules Path**, click `...` and select the `modules` folder inside your cloned repository.
   * Switch your active workspace to this new workspace.

---

### Option C: Copy Specific Modules to Your Existing Workspace

If you want to merge specific tools into your current workspace:

1. Locate your active workspace directory (by default under `~/rigBuilder/workspaces/<workspace_name>/`).
2. Copy the desired module files (e.g., `.rb` files) from `modules/` in this repository into your active workspace's `modules/` folder.
3. Rig Builder will automatically detect the new files via auto-sync, and they will appear in your **Module Browser** immediately.

---

## 🧠 Semantic Search Support

This repository includes a pre-generated `moduleIndex.json` file.

If you are using **Ollama** for AI assistance and semantic search in Rig Builder:

* Rig Builder uses this file to perform instant, natural language semantic search across the community modules (e.g., searching for *"how to constraint a control to a mesh"* will suggest the `Rivet` module).
* No manual indexing is required on your side!

---

## 🤝 How to Contribute

We welcome and encourage contributions from the community! If you have built handy rigging scripts, pipeline utilities, or custom DCC tools, please share them:

1. **Fork** this repository.
2. Create folders for new host applications (e.g. `modules/blender/`, `modules/unreal/`) or new categories (e.g. `modules/maya/Rigging/`, `modules/maya/Utility/`).
3. Place your module files (saved from Rig Builder with the `.rb` extension) in the appropriate directories.
4. Submit a **Pull Request**!

### Contribution Guidelines

* **Documentation:** Ensure your module contains a rich `<doc>` element with clear instructions, summary, and use cases.
* **Attributes:** Use clear labels and tooltips. Use templates like `lineEditAndButton` or `listBox` to guide the user.
* **Compatibility:** Write robust Python code (using `pymel`, `cmds`, or native DCC APIs) that handles edge cases gracefully.

---

*Happy Rigging!*
