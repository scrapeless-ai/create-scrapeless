# 🧰 create-scrapeless

> A command-line tool to quickly scaffold [Scrapeless](https://github.com/scrapeless-ai/create-scrapeless) actor templates using Golang or Node.js.

---

## ✨ Features

- ⚡ Instant project scaffolding
- 🤖 Built-in templates: Golang & Node.js
- 🎯 Interactive CLI like `npm init`
- 🔧 Extendable template system

---

## 📦 Installation

### Using the install script (recommended)
You can quickly install the latest release via our bash install script (Linux/macOS/Windows Git Bash):
```bash
bash <(curl -fsSL https://raw.githubusercontent.com/scrapeless-ai/create-scrapeless/main/install-create-scrapeless.sh)
```
This script will:
- Automatically detect your OS and architecture
- Download the latest create-scrapeless release
- Extract the binary and install it to ~/.local/bin
- Add ~/.local/bin to your PATH if it’s not already set (for Linux/macOS)
- Show instructions on how to add to PATH manually on Windows

### From source (requires Go 1.24+)

```bash
go install github.com/scrapeless-ai/create-scrapeless@latest
```

## 🚀 Usage

### 📌 1. Interactive Mode

Just run:

```bash
create-scrapeless --create
```

You’ll be guided to:

- Select a template (e.g. start_with_golang, start_with_node)
- Input a project folder name

**Useful when you're unsure about flags or want a guided experience.**

### 📌 2. Non-interactive Mode

Fully automate project generation with flags:

```bash
create-scrapeless --tmpl start_with_golang --name my-actor
```

Creates a folder **my-actor** using the Golang actor template.
Run your actor:
```bash
cd my-actor
create-scrapeless --run
```

### 📌 3. Show Version

```bash
create-scrapeless --version
```

## 🧩 Flags

| Flag        | Short | Description                                                |
|-------------|-------|------------------------------------------------------------|
| `--create`  | `-c`  | Launch interactive template selection and naming           |
| `--tmpl`    | `-t`  | Choose a template (`start_with_golang`, `start_with_node`) |
| `--name`    | `-n`  | Set the project folder name (default: `my-actor`)          |
| `--version` | `-v`  | Print the version number of `create-scrapeless`               |
| `--run`     | `-r`  | Quickly launch your actor                                  |

## 📸 Example

```
create-scrapeless --create
# ? Select a template  [Use arrows to move, type to filter, ? for more help]
# > start_with_golang
#   start_with_node_js
#   start_with_ts
# ？Enter the name of the template [? for help] (my-actor)
#
# ? Enter the name of the template my-actor


# Output:
# Template Source: https://github.com/scrapeless-ai/actor-template-go.git
# Template generated in your_work_base\my-actor

cd my-actor
create-scrapeless --run
# Output:
# Launch my-actor logs...
```
