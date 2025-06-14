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

![Screenshot 2025-06-14 111044](https://github.com/user-attachments/assets/800022b1-2d24-4b47-8dc5-13f79b600617)
![Screenshot 2025-06-14 111255](https://github.com/user-attachments/assets/b0939fde-a953-4e0c-a3a9-91b75d45f2ce)

"""Add this"""

{
  "code-runner.executorMapByFileExtension": {
          ".rs": "if (Test-Path Cargo.toml) { cargo run } else { rustc $fileName && .\\$fileNameWithoutExt }",
  }
  "code-runner.runInTerminal": true,
  "code-runner.saveAllFilesBeforeRun": true,
}

"""like this:"""
![Screenshot 2025-06-14 111841](https://github.com/user-attachments/assets/f9883fd0-cf61-4c80-909b-d67909f893a4)

![Screenshot 2025-06-14 111850](https://github.com/user-attachments/assets/2c375418-4120-4c3c-a471-402752192a9e)

📌 Enjoy coding Rust smoothly in VSCode!
