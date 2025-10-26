# Contributing to Tufte-Style Typst Template

感谢你对本项目的关注！ | Thank you for your interest in this project!

## 如何贡献 | How to Contribute

### 报告问题 | Reporting Issues

如果你发现了 bug 或有功能建议：| If you found a bug or have a feature request:

1. 查看 [Issues](https://github.com/exusiaiwei/template-typst-tufte/issues) 确认问题是否已被报告
2. 创建新的 Issue，包含：
   - 清晰的标题
   - 详细的描述
   - 复现步骤（如果是 bug）
   - 期望的行为
   - 实际的行为
   - 环境信息（Typst 版本等）

### 提交代码 | Submitting Code

1. **Fork 本仓库** | Fork this repository
2. **创建特性分支** | Create a feature branch
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **进行修改** | Make your changes
   - 保持代码风格一致
   - 添加注释说明复杂逻辑
   - 测试你的修改
4. **提交修改** | Commit your changes
   ```bash
   git commit -m "feat: add your feature description"
   ```
5. **推送到你的 Fork** | Push to your fork
   ```bash
   git push origin feature/your-feature-name
   ```
6. **创建 Pull Request** | Create a Pull Request

### 提交信息规范 | Commit Message Convention

使用 [Conventional Commits](https://www.conventionalcommits.org/) 格式：

- `feat:` 新功能
- `fix:` Bug 修复
- `docs:` 文档修改
- `style:` 代码格式修改（不影响功能）
- `refactor:` 重构（既不是新功能也不是修复）
- `test:` 测试相关
- `chore:` 构建过程或辅助工具的变动

例如 | Examples:
```
feat: add custom callout color support
fix: resolve sidenote overlap issue
docs: update README with new examples
```

## 代码风格 | Code Style

### Typst 代码

- 使用 2 空格缩进
- 函数名使用 kebab-case（如 `my-function`）
- 变量名使用 kebab-case（如 `theme-color`）
- 添加必要的注释，特别是复杂逻辑

### 文档

- 中英文混排时，中英文之间添加空格
- 使用 Markdown 标准格式
- 代码块指定语言

## 测试 | Testing

提交 PR 前请确保：

1. 模板可以正常编译
2. 所有示例章节渲染正确
3. 新功能有相应的示例
4. 文档已更新

## 需要帮助？ | Need Help?

- 查看 [README](README.md)
- 查看现有的 [Issues](https://github.com/exusiaiwei/template-typst-tufte/issues)
- 提问时请提供详细信息

## 行为准则 | Code of Conduct

请保持友好和尊重。我们致力于为每个人提供一个开放和友好的环境。

---

再次感谢你的贡献！🎉 | Thank you for your contribution! 🎉
