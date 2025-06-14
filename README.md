# VsCode-CodeRunner-Setting-for-Rust
This configuration allows you to run Rust projects or individual .rs files directly in Visual Studio Code using the Code Runner extension.

📌 功能简介 | Features

✅ 自动识别 Cargo 项目
如果当前目录包含 Cargo.toml，将自动使用 cargo run 运行整个项目。
This ensures that full Rust projects are executed correctly with proper build and dependency management.
✅ 支持单个 .rs 文件运行
如果没有 Cargo.toml，则使用 rustc 编译并运行单个 .rs 文件。
Ideal for quick tests, small programs, or learning Rust without a full project setup.
✅ 在终端中运行
所有 Rust code runs inside the terminal (not just output).
Allows for interactive input/output, debugging, and better visibility of program behavior.
✅ 自动保存所有文件
Ensures that any unsaved changes are saved before execution starts.

⚙️ 配置内容 | Configuration Details:
![first](https://github.com/user-attachments/assets/41d50bdb-6f9f-4fc7-bedc-8aa0b4010834)



![second](https://github.com/user-attachments/assets/46275589-403d-4880-a1b0-d4718c9967e1)


"""Add this"""

{
  "code-runner.executorMapByFileExtension": {
          ".rs": "if (Test-Path Cargo.toml) { cargo run } else { rustc $fileName && .\\$fileNameWithoutExt }",
  }
  "code-runner.runInTerminal": true,
  "code-runner.saveAllFilesBeforeRun": true,
}

"""like this:"""
![Screenshot 2025-06-14 111841](https://github.com/user-attachments/assets/0f052c79-09dd-4ee9-96f3-c2a79e4faead)

![Screenshot 2025-06-14 111850](https://github.com/user-attachments/assets/d7bbf15d-d8f1-496e-bc58-2251282add06)


📌 Enjoy coding Rust smoothly in VSCode!
