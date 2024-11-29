<header>

# 介绍GitHub Copilot

在这一学习模块中，我们将深入探讨由GitHub Copilot带来的AI配对编程革命性领域，这款首个大规模AI开发者工具旨在提升您的编码体验。

GitHub Copilot通过分析文件和注释的上下文以及从其交互式聊天中输入的信息来提供自动填充式建议，使您能够更快、更轻松地编写代码。当您深入研究此模块时，您将揭开GitHub Copilot的复杂性，探索其在VS Code和Codespaces中的功能。

我们的学习目标既雄心勃勃又可实现。到模块结束时，您不仅能够清楚地说明GitHub Copilot是什么及其优势，而且还能够理解它对个人和企业的可用性。深入了解GitHub Copilot的未来，并通过实践练习掌握其在Visual Studio Code中的使用。

研究表明，GitHub Copilot使开发人员能够更快地编写代码，专注于解决重大问题，保持更长的工作效率，并在他们的工作中获得更大的满足感。

注意：尽管本模块使用[Codespaces](https://github.com/codespaces)，您也可以在包括本地Visual Studio Code在内的多种环境中使用GitHub Copilot。

</header>

- **适用对象**：开发人员、DevOps工程师、软件开发经理、测试人员。
- **学习内容**：如何将Copilot安装到Codespace中，接受来自代码的建议，接受来自注释的建议。
- **构建内容**：JavaScript文件将由Copilot AI生成代码和注释建议。
- **先决条件**：要使用GitHub Copilot，您必须拥有有效的GitHub Copilot订阅。注册30天免费[Copilot](https://github.com/settings/copilot)。
- **时间**：本课程可在一小时内完成。

在本模块结束时，您将能够：

- 解释什么是GitHub Copilot及其提供的优势。
- 了解GitHub Copilot对个人和企业的可用性。
- 讨论GitHub Copilot的未来。
- 学习如何开始使用GitHub Copilot及一些常见的配置。
- 通过动手练习使用GitHub Copilot在Visual Studio Code中开发。

## 先决阅读：
- [GitHub Copilot简介](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/?WT.mc_id=academic-113596-abartolo)
- 什么是GitHub Copilot？（下方视频播放列表）
- [![What is GitHub Copilot](https://img.youtube.com/vi/QG1E0SCqqW8/0.jpg)](https://learn.microsoft.com/shows/introduction-to-github-copilot/what-is-github-copilot-1-of-6/?WT.mc_id=academic-113596-abartolo)

### 如何开始本课程

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'skills',
  template_name: 'copilot-codespaces-vscode',
  owner: '@me',
  name: 'skills-copilot-codespaces-vscode',
  description: 'My clone repository',
  visibility: 'public',
}).toString()
-->

[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=copilot-codespaces-vscode&owner=%40me&name=skills-copilot-codespaces-vscode&description=My+clone+repository&visibility=public)

1. 右键点击**开始课程**并在新标签页中打开链接。
2. 在新标签页中，大部分提示将自动为您填写。
   - 对于所有者，选择您的个人账户或托管存储库的组织。
   - 我们建议创建一个公开存储库，因为私人存储库会[使用Actions分钟](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions)。
   - 向下滚动并点击表单底部的**创建存储库**按钮。
3. 在创建新存储库后，等待约20秒，然后刷新页面。按照新存储库的README中的分步说明进行操作。

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

寻求帮助：[在我们的讨论板中发布](https://github.com/orgs/skills/discussions/categories/code-with-copilot) &bull; [查看GitHub状态页面](https://www.githubstatus.com/)
