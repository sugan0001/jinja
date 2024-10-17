# Jinja2 Version Control

A simple bash script to manage different versions of your Jinja2 templates using Git tags. This tool helps you create, update, switch between versions, list all versions, and delete specific versions of your templates.

## 📋 Prerequisites

- Git must be installed and initialized in your project
- Templates should be stored in the `prompts` directory
- Bash environment to run the script

## 🚀 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/jinja2-version-control.git
cd jinja2-version-control
```

2. Make the script executable:
```bash
chmod +x script.sh
```

## 📁 Directory Structure

```
your-project/
├── script.sh
└── prompts/
    └── your-templates-here
```

## 🛠️ Usage

### 1. Create a Version
Create a new version of your template and save it with a Git tag.

```bash
./script.sh create <templateName> <version>

# Example
./script.sh create joke v1
```

### 2. Update the Latest Version
Update the most recent version of your template with new changes.

```bash
./script.sh update <templateName>

# Example
./script.sh update joke
```

### 3. Switch Versions
Switch to a specific version of your template.

```bash
./script.sh switch <templateName> <version>

# Example
./script.sh switch joke v1
```

### 4. List All Versions
Display all available versions for a template.

```bash
./script.sh list <templateName>

# Example
./script.sh list joke-template
```

### 5. Delete a Version
Remove a specific version of your template.

```bash
./script.sh delete <templateName> <version>

# Example
./script.sh delete joke-template v1
```

## ⚠️ Important Notes

- The update function uses `-f` with `git tag` to force-update tags to the latest commit
- When switching versions, ensure all changes are committed or stashed to avoid conflicts
- All templates must be stored in the `prompts` directory
- The script expects your project to be a Git repository

## 📝 Example Workflow

1. Create your first template version:
```bash
./script.sh create my-template v1
```

2. Make changes to your template and update it:
```bash
./script.sh update my-template
```

3. Switch between versions as needed:
```bash
./script.sh switch my-template v1
```

4. Check available versions:
```bash
./script.sh list my-template
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
