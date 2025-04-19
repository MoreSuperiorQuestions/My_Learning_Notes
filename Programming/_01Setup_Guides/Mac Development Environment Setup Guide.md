This note records how I set up my Python + Machine Learning development environment from scratch on a brand-new Mac.
It includes tools, commands, and my understanding of each step.

## Tool List Overview

| Tool          | Purpose                                |
| ------------- | -------------------------------------- |
| Homebrew      | Package manager for macOS              |
| Git           | Version control                        |
| Python        | Programming language                   |
| Anaconda      | Python environment and package manager |
| VS Code       | Code editor                            |
| Powerlevel10k | Terminal theme + Git prompt            |

---

## Step-by-Step Setup Process

### 1. 安装 Homebrew

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew --version
```

**为什么要安装Homebrew**: 使用它安装和管理后面的软件更简单，它会自动处理软件之间的依赖关系和更新.

---

### 2. 安装Python

```
brew install python
python3 --version
```

**Why**: Python 是机器学习和数据分析中最常用的编程语言，许多深度学习框架依赖于 Python.

---

### 3. Install Python

```
brew install python
python3 --version
```

**Why**: Base requirement for coding and running scripts.

---

### 4. Install Anaconda

```
bash Anaconda3-2024.10-1-MacOSX-x86_64.sh
conda init zsh
source ~/.zshrc
conda --version
```

**Why**: For creating isolated environments and managing ML/data science packages.

---

### 5. Install VS Code

```
brew install --cask visual-studio-code
```

- Open VS Code and install extensions:
    
    - Python
        
    - GitLens
        
    - Jupyter (if needed)
        

**Why**: My main code editor with built-in terminal, Git integration, and Python support.

---

### 6. Setup Powerlevel10k

```
brew install zsh
brew install romkatv/powerlevel10k/powerlevel10k
```

Then in `~/.zshrc`:

```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Also:

- Install MesloLGS NF fonts
    
- Set terminal font to MesloLGS NF
    

**Why**: Nothing else, just for cool.For a better terminal experience (Git status, path, syntax coloring).

---

### 7. Generate and Connect SSH Key for GitHub

```
ssh-keygen -t rsa -b 4096 -C "your.email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub
```

- Add the public key to your GitHub account → **Settings > SSH and GPG Keys**
    
- Test connection:
    

```
ssh -T git@github.com
```

**Why**: Securely connect and push code to GitHub.

---

## 📦 Optional but Recommended

- `conda install jupyterlab` → for interactive notebooks
    
- `conda install scikit-learn pandas matplotlib` → data tools
    
- `conda install tensorflow pytorch` → deep learning frameworks
    

---

## 🧠 My Key Takeaways

- Tools like `conda`, `git`, and `zsh` are more than "just install and use" — they each solve real developer pain points.
    
- Automating this setup into a script or repeatable guide increases reproducibility.
    
- Knowing "why" gives me more confidence when things break.
    

---

## 🔗 Related Notes

[[Anaconda]] [[Git]] [[Interpreter_vs_Compiler]] [[Tool_Usage]] [[VSCode]]