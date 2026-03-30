# Gitignore Auto Gen

`Gitignore Auto Gen` 是一个简单的 Python 命令行工具，用于在目标目录中快速生成一份预置的 `.gitignore` 文件。

当前内置模板主要面向 Python 项目，覆盖了常见的缓存文件、虚拟环境、构建产物、测试产物、编辑器配置以及部分 AI 编码工具相关目录。

## Features

- Generate a ready-to-use `.gitignore` file for Python projects
- Support writing to the current directory or a custom target path
- Ask before overwriting an existing `.gitignore`
- Include common ignores for tooling, environments, logs, and editor files

## Project Structure

```text
.
├── gitignore_auto_gen.py
├── LICENSE
└── README.md
```

## Requirements

- Python 3.8+

## Quick Start

在当前目录生成 `.gitignore`：

```bash
python gitignore_auto_gen.py
```

在指定目录生成 `.gitignore`：

```bash
python gitignore_auto_gen.py --path /path/to/your/project
```

如果目标目录中已经存在 `.gitignore`，程序会提示是否覆盖：

```text
Do you want to overwrite the existing file? (y/n):
```

## What Is Included

当前模板主要包含以下类别：

- Python cache and compiled files
- Build and packaging artifacts
- Virtual environments
- Test and coverage outputs
- Jupyter and IPython files
- Type checker and linter caches
- IDE and editor files such as VS Code
- Local logs and OS-generated files
- AI coding assistant related files such as `AGENTS.md`, `.claude`, `.omx`, `.omc`, and `.codex*`

## Example Workflow

进入你的项目目录后运行：

```bash
python /path/to/gitignore_auto_gen.py
```

或者在任意位置为某个项目目录生成：

```bash
python gitignore_auto_gen.py --path ./my_project
```

生成完成后，对应目录下会得到一个 `.gitignore` 文件。

## Notes

- 当前模板是内置在脚本中的固定内容，不是交互式按语言或框架动态选择
- 模板更适合 Python 项目；如果你的项目包含其他语言或特殊构建工具，建议按需补充
- 脚本只负责生成 `.gitignore`，不会初始化 Git 仓库

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
