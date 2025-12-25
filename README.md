Elbette, işte "bizim usul" GitHub README.md dosyasının İngilizce versiyonu. Not defterine yazar gibi, kısa ve öz:

---

# Depones Python Template

A "Production Ready" project skeleton to skip the repetitive setup of VS Code settings, linters, formatters, and folder structures for every new Python project.

**Standards:**

* **Architecture:** Modern `src/` layout (Prevents import hell).
* **Workflow:** Pre-configured Husky, Commitlint, and Semantic Versioning.
* **Tooling:** `Black` (Format), `Isort` (Import), and `Pytest` ready to go.
* **Build:** Includes templates for PyInstaller (`.spec`) and Inno Setup (`.iss`).

### 🚀 Usage

Generate a new project with a single command:

```bash
# If cookiecutter is not installed: pip install cookiecutter

cookiecutter https://github.com/DeponesLabs/depones-python-template
# Or from local: cookiecutter D:/Tools/depones-python-template

```

### ⚠️ Naming Logic (Automated)

The template automatically handles the naming convention difference between the Repo and the Python Package:

* **Project Name:** If you enter `Turbo Skryer`;
* **Repo/Folder:** becomes `turbo-skryer` (Hyphenated).
* **Python Package:** becomes `src/turbo_skryer` (Underscored).
* *No manual renaming required.*

### Post-Install

To "hydrate" the project after creation:

```bash
cd project-name
git init                # Required for Husky
python -m venv venv     # Create virtual env
pip install -e .        # Install in editable mode (Crucial for src layout)
npm install             # Install Husky hooks

```