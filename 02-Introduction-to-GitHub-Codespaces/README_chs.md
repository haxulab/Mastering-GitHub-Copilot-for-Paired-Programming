<header>

# GitHub Codespaces简介

欢迎来到 GitHub Codespaces 的精彩世界，这是您基于云的编码资源。在这个模块中，我们将深入了解即时的、基于云的开发环境，革新您对编码的看法。GitHub Codespaces 提供了无缝集成的体验，提供了一个配备了开发所需的基本语言、工具和实用程序的容器。

在整个学习过程中，我们将探索 Codespaces 的生命周期和过程。发现根据您的独特偏好和需求定制您的 Codespace 设置的力量。为了巩固您的理解，我们将在模块结束时进行一个动手练习，允许您在 GitHub Codespaces 环境中展示您的编码才能。

想象一下，一个完全配置的开发环境触手可及，可以从任何有互联网连接的计算机访问。GitHub Codespaces 为协作和灵活的编码打开了大门。让我们深入探索，解锁 GitHub Codespaces 基于云开发的全部潜力！

</header>


- **适用于**: 开发人员、DevOps 工程师、工程经理、产品经理。
- **您将学到**: 如何创建 codespace，从 codespace 推送代码，选择自定义镜像，以及自定义 codespace。
- **您将构建**: 一个带有 devcontainer.json 文件、自定义和个性化设置的 codespace。
- **先决条件**: 您需要了解以下内容:
  - 使用 Visual Studio Code，[Visual Studio Code 文档](https://code.visualstudio.com/docs)。
  - 了解 GitHub 的使用或完成上一模块 [GitHub 简介](https://github.com/WirelessLife/Mastering-GitHub-Copilot-for-Paired-Programming/blob/main/01-Introduction-to-GitHub/README.md?WT.mc_id=academic-113596-abartolo)。
- **时间**: 本课程可以在一小时内完成。

在本模块结束时，您将能够:

1. 描述 GitHub Codespaces。
2. 解释 GitHub Codespace 的生命周期以及如何执行每个步骤。
3. 定义可以用 GitHub Codespaces 个性化的不同自定义内容。


## 预备阅读: 

- [使用 GitHub Codespaces 进行编码](https://learn.microsoft.com/training/modules/code-with-github-codespaces/?WT.mc_id=academic-113596-abartolo)
- 什么是 GitHub Codespaces? (下面的视频播放列表)
- [![什么是 Codespaces](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://www.youtube.com/watch?v=ozuDPmcC1io&list=PLmsFUfdnGr3wTl-NCblzcrEv2lFSX975-)



### 如何开始本课程

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'skills',
  template_name: 'code-with-codespaces',
  owner: '@me',
  name: 'skills-code-with-codespaces',
  description: 'My clone repository',
  visibility: 'public',
}).toString()
-->

[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=code-with-codespaces&owner=%40me&name=skills-code-with-codespaces&description=My+clone+repository&visibility=public)

1. 右键点击 **开始课程** 并在新标签页中打开链接。
2. 在新标签页中，大部分提示将自动为您填写。
   - 对于所有者，选择您的个人账户或托管仓库的组织。
   - 我们建议创建一个公共仓库，因为私有仓库将[使用 Actions 分钟](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions?WT.mc_id=academic-113596-abartolo)。
   - 向下滚动并点击表单底部的 **创建仓库** 按钮。
3. 创建新仓库后，等待约20秒，然后刷新页面。按照新仓库中 README 的分步说明进行操作。

<footer>

<!--
  <<< 作者提示: 页脚 >>>
  添加支持链接，GitHub 状态页面，行为守则，许可链接。
-->

---

获取帮助: [在我们的讨论板上发帖](https://github.com/orgs/skills/discussions/categories/introduction-to-github) &bull; [查看 GitHub 状态页面](https://www.githubstatus.com/)