<header>

# 使用 GitHub Copilot 创建迷你游戏

本模块的重点是利用 GitHub Copilot 创建经典的石头、剪刀、布迷你游戏。这种实践经验不仅能提升您的编程技能，还能增强您在 Python 中开发控制台应用程序的能力。最棒的是？我们将利用 GitHub Codespaces，免去配置开发环境的烦恼。借助 GitHub Copilot 作为您的 AI 配对编程助手，您可以专注于应用程序开发，同时与您的代码助手无缝协作。

</header>


- **适合谁**: 开发人员、DevOps 工程师、软件开发经理、测试人员。
- **您将学到什么**: 利用 GitHub Copilot 创建代码并为您的工作添加注释。
- **您将构建什么**: 由 Copilot AI 生成代码和注释建议的 Python 文件。
- **先决条件**: 要使用 GitHub Copilot，您必须有一个有效的 GitHub Copilot 订阅。注册 30 天免费 [Copilot](https://github.com/settings/copilot) 体验。
- **时长**: 本课程可以在一小时内完成。

在本模块结束时，您将掌握以下技能：

- 体验 GitHub Codespaces 作为开发环境。
- 在 Python 控制台应用程序中开发输入和输出例程。
- 使用 GitHub Copilot 作为助手。

## 预备阅读：
- [使用 GitHub Copilot 的提示工程介绍](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [挑战项目 - 使用 GitHub Copilot 和 Python 构建迷你游戏](https://learn.microsoft.com/training/modules/challenge-project-create-mini-game-with-copilot/?WT.mc_id=academic-113596-abartolo)
- 学习直播：使用 GitHub Copilot 构建迷你游戏控制台应用程序（视频如下）
- [![学习直播：使用 GitHub Copilot 构建迷你游戏控制台应用程序](https://mediusimg.event.microsoft.com/video-53275/b508053c0b/thumbnail.jpg?sv=2018-03-28&sr=c&sig=k6NthrPwnvBfDPNAEBQaYaVzlJavZ8pnWuP6OcKm4Bs%3D&se=2028-11-18T05%3A23%3A52Z&sp=r)](https://ignite.microsoft.com/sessions/aeaf1e85-65e2-497d-aaf5-724d85213aa1?WT.mc_id=academic-113596-abartolo)
  

## 要求

- 启用您的 [GitHub Copilot 服务](https://github.com/github-copilot/signup)

## 💪🏽 练习

**右键点击“开始课程”按钮以在新标签页中打开 Codespace**
 
[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=copilot-codespaces-vscode&owner=%40me&name=skills-copilot-codespaces-vscode&description=My+clone+repository&visibility=public)

您已经了解了一些关于 GitHub Codespaces 和 GitHub Copilot 及其工作原理的信息。在这个挑战练习中，您的目标是使用 GitHub Copilot 来开发一个 Python 迷你游戏。

#### 测试您的 GitHub Codespace

1. 访问您的 Codespaces 并在 Visual Studio Code 中创建一个名为 *app.py* 的新文件。

   **注意**: 如果尚未安装，您可能需要在 Visual Studio Code 中安装 Python 扩展。

2. 输入以下注释：

   ```python
   # 将 'hello world' 输出到控制台
   ```
      
3. GitHub Copilot 应该会为您完成代码并提供以下结果：

   ```python
   # 将 'hello world' 输出到控制台
   print('hello world')
   ```

4. 在终端中运行 *python app.py* 命令，检查结果是否类似于以下控制台消息：

   ```bash
   hello world
   ```
   
### 创建游戏逻辑

现在您已验证 Codespaces 与 GitHub Copilot 一起工作，下一步是在 GitHub Copilot 的帮助下，根据以下规格开发 Python 迷你游戏的逻辑：

游戏的获胜者由三个简单规则决定：

- **石头** 胜 剪刀。
- **剪刀** 胜 纸。
- **纸** 胜 石头。

#### 游戏交互考虑

计算机会是您的对手，并可以随机选择一个元素（**石头**、**纸**或**剪刀**）。您的游戏交互将通过控制台（终端）进行。

- 玩家可以选择三个选项之一，石头、纸或剪刀，如果他们输入无效选项应有所提示。
- 每回合，玩家必须输入列表中的一个选项，并被告知他们是赢了，输了还是与对手打成平局。
- 每回合结束后，玩家可以选择是否继续游戏。
- 在游戏结束时显示玩家的得分。
- 迷你游戏必须处理用户输入，将其转换为小写字母，并在选项无效时通知用户。

在您的 GitHub Codespaces 中，按照给定的指示设置提示，以便 GitHub Copilot 能够理解并帮助您构建迷你游戏。请记住，GitHub Copilot 依赖注释来掌握上下文，并在您项目时为您提供有用的建议。

#### 验证您的工作

1. 在控制台中使用 *python app.py* 命令运行迷你游戏。
2. 在提示中输入游戏选项之一：*rock*、*paper* 或 *scissors*。
3. 迷你游戏应告知玩家是否赢了、输了或与对手打成平局。
4. 选择继续游戏。
5. 在提示中输入 *screen*。
6. 迷你游戏应告知玩家输入的选项是否无效。
7. 重复步骤 2 和 4，玩几轮并选择不继续游戏。
8. 检查迷你游戏是否终止并显示您的得分，告知您获胜次数和回合数。

祝贺您完成了这一挑战练习！您已使用 GitHub Copilot 创建了一个 Python 控制台迷你游戏。