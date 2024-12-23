# WPF.Xlog

## 简介
WPF.Xlog 是一个基于 .NET 6.0 的 WPF 应用程序，用于记录和管理日志信息。它支持多种日志级别，并能够将日志信息保存在结构化的文件系统中。

## 主要功能
- **日志记录**：支持不同级别的日志记录，包括调试、信息、警告、错误和致命错误。
- **日志管理**：自动管理日志文件的创建和轮转，保证日志文件的大小和数量符合预设的限制。
- **用户操作日志**：记录用户的操作行为，便于审计和回溯。

## 安装
1. 确保你的系统已安装 .NET 6.0 SDK。
2. 克隆仓库到本地：
   ```bash
   git clone https://github.com/xioa-cn/WPF.Xlog.git
   ```
3. 进入项目目录，并构建项目：
   ```bash
   cd WPF.Xlog
   dotnet build
   ```

## 使用方法
要启动日志服务，请在你的应用程序启动时调用 `LogService.CreateLoggerInstance()` 方法。之后，你可以通过 `LogService.Instance` 获取日志服务的实例，并调用相应的方法来记录日志。

例如，记录一个错误信息：
 ## csharp
`LogService.Instance.LogError("这是一个错误信息");`
