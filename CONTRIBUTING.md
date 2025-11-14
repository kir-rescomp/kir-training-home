# Contributing to KIR Training Catalogue

Thank you for contributing to the KIR Research Computing Training Catalogue! This guide will help you quickly create new training modules.

## Branching Strategy

All contributions should be made on a personal development branch following the naming convention: `<username>-dev`

**Examples:**
- `jacky-dev`
- `alice-dev`
- `bob-dev`

**Workflow:**
```bash
# Create and switch to your dev branch
git checkout -b <your-name>-dev

# Make your changes
# Commit regularly
git add .
git commit -m "Your commit message"

# Push to your dev branch
git push -u origin <your-name>-dev

# When ready, create a Pull Request to merge into main
```

## Quick Start: Create a New Training Module

### 1. Use the Template Repository

Create a new repository from the template on GitHub:

1. Go to [https://github.com/kir-rescomp/training-template](https://github.com/kir-rescomp/training-template)
2. Click the green **"Use this template"** button
3. Select **"Create a new repository"**
4. Name your repository following the pattern: `training-[topic-name]`
   - Example: `training-intro-to-tmux`
5. Set the repository as **Public**
6. Click **"Create repository"**

### 2. Clone Your New Repository

```bash
# Clone your newly created repository
git clone https://github.com/kir-rescomp/training-[your-topic].git
cd training-[your-topic]

# Create your personal dev branch
git checkout -b <your-name>-dev
```

**Example:**
```bash
git clone https://github.com/kir-rescomp/training-intro-to-tmux.git
cd training-intro-to-tmux
git checkout -b jacky-dev
```

### 3. Configure Your Module

Edit `mkdocs.yml` and replace placeholders:

- `[YOUR TRAINING MODULE NAME]` → Your module title (e.g., "Introduction to tmux")
- `[YOUR-REPO-NAME]` → Repository name (e.g., "training-intro-to-tmux")

**Example changes in mkdocs.yml:**
```yaml
site_name: Introduction to tmux
site_url: "https://kir-rescomp.github.io/training-intro-to-tmux/"
repo_name: kir-rescomp/training-intro-to-tmux
repo_url: https://github.com/kir-rescomp/training-intro-to-tmux
```

### 4. Create Your Content

**Edit `docs/index.md`:**
- Add module description
- List your sections with links

**Create content files:**
```bash
cd docs/
touch 1.getting-started.md
touch 2.essential-commands.md
touch 3.practical-examples.md
```

**Add images:**
- Place logos and screenshots in `docs/images/`

### 5. Test Locally

**Option A: Using pip (traditional)**
```bash
# Install dependencies
pip install -r requirements.txt

# Run local server
mkdocs serve
```

**Option B: Using pixi (modern, recommended)**
```bash
# Install dependencies from pixi.toml (first time only)
pixi install

# Run local server
pixi run serve
```

Or use the shorthand:
```bash
pixi run serve
```
(pixi will automatically install dependencies if needed)

Visit http://127.0.0.1:8000 to preview your module.

### 6. Commit and Push Your Changes

```bash
# Add your changes
git add .
git commit -m "Configure module: [Your Module Name]"

# Push to your dev branch
git push -u origin <your-name>-dev
```

### 7. Enable GitHub Pages

1. Go to your repository on GitHub
2. Navigate to **Settings → Pages**
3. Configure:
   - **Source:** Deploy from branch
   - **Branch:** `gh-pages` (will be created automatically by CI)
   - Click **Save**

The GitHub Actions workflow (`.github/workflows/ci.yml`) will automatically build and deploy your site when you push to `main`.

### 8. Add to Main Catalogue

**Important:** Work on your `<username>-dev` branch, then create a PR to `main`.

Edit `kir-training-home/docs/index.md` and add a card for your module:

```markdown
-   <a href="https://kir-rescomp.github.io/training-intro-to-tmux/" style="text-decoration: none; color: inherit; display: block;">
    <center>![tmux](./images/tmux_logo.png){ width="220" }</center>

    __Introduction to tmux__

    ---
    <span style="font-size: 0.7rem;">
    Terminal multiplexer for managing persistent sessions on HPC clusters. Learn to create detachable sessions, split terminals into panes, and maintain long-running processes even when disconnected from SSH.
    </span></a><br>

    [Start :octicons-arrow-right-24:](https://kir-rescomp.github.io/training-intro-to-tmux/){ .md-button }
```

**Note:** Add your card in the appropriate position based on learning progression (see `plan/master-plan.md` for suggested ordering).

## Writing Guidelines

### Target Audience
Researchers using HPC/cluster environments at various skill levels.

### Content Guidelines
- **5-minute read time** per module - keep it focused and practical
- **Use numbered files** for sequential content (e.g., `1.topic.md`, `2.topic.md`)
- **Include code examples** - practical, copy-pasteable code
- **Focus on HPC/cluster use cases** where relevant
- **Keep examples generic** - avoid institution-specific details
- **Use admonitions** for tips, warnings, and key takeaways

### Example Admonition (Key Takeaways Box)
```markdown
!!! success "Key Takeaways"
    - First key point
    - Second key point
    - Third key point
```

### Code Blocks
Use syntax highlighting:
````markdown
```bash
# Bash command example
srun --partition=interactive --cpus-per-task=4 bash
```

```python
# Python code example
import numpy as np
print("Hello, HPC!")
```
````

## Template Repository

For detailed template documentation, see [https://github.com/kir-rescomp/training-template](https://github.com/kir-rescomp/training-template)
