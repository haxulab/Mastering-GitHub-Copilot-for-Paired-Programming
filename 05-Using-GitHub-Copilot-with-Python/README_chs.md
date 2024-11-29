<header>

# 使用GitHub Copilot与Python

GitHub Copilot是世界上第一款大规模AI开发者工具，它通过在您工作时提供类似自动完成的建议来显著加速代码编写。在本模块中，我们将重点使用GitHub Copilot的力量来提高您的Python编码效率。

作为开发人员，您的目标是提高生产力并加快编码过程。GitHub Copilot充当您的AI配对程序员，根据上下文和代码模式提供建议。在本模块中，您将使用GitHub Copilot与Codespaces一起有效生成和实施代码建议。

准备好进入一个真实的场景吧！您将使用GitHub Copilot修改一个Python仓库，以创建一个交互式HTML表单和一个API端点。这个项目将为您提供开发一个提供HTTP API的Python网络应用的宝贵经验，该应用生成用于识别目的的伪随机令牌。

</header>


- **适合对象**: 开发人员，DevOps工程师，软件开发经理，测试人员。
- **您将学到什么**: 使用GitHub Copilot创建代码并为您的工作添加注释。
- **您将构建什么**: 将由Copilot AI生成代码和注释建议的Python文件。
- **先决条件**: 要使用GitHub Copilot，您必须拥有一个活跃的GitHub Copilot订阅。报名享受30天免费试用 [Copilot](https://github.com/settings/copilot)。
- **时间**: 本模块可在一小时内完成。

在本模块结束时，您将学会：

- 编写提示以从GitHub Copilot生成建议
- 应用GitHub Copilot改进您的项目

## 必读资料:
- [GitHub Copilot提示工程简介](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [使用GitHub Copilot与Python](https://learn.microsoft.com/en-us/training/modules/introduction-copilot-python/?WT.mc_id=academic-113596-abartolo)

## 要求

1. 启用您的[GitHub Copilot服务](https://github.com/github-copilot/signup)
1. 使用Codespaces打开[此仓库](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

## 💪🏽 练习

**右键单击以下Codespaces按钮以在新标签页中打开您的Codespace**
 
[![在GitHub Codespaces中打开](https://github.com/codespaces/badge.svg)](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

API已经有一个生成令牌的单一端点。让我们通过添加一个新端点来接受文本并返回一个令牌列表来更新API。

### 🛠 第1步：添加Pydantic模型

转到`main.py`文件，导航到提供的代码底部，选择**Ctrl + I（PC）**或**Cmd + I（Mac）**，然后将以下内容复制到提供的GitHub Copilot聊天框中，让其为您生成一个`Pydantic`模型：

```
创建一个Pydantic模型，以便我可以在一个新路由中使用它，该路由将接受带有text为键并接受字符串的JSON。
```

生成的模型应如下所示：

```python
    class TextData(BaseModel):
        text: str
```

> [!NOTE]
> 您可能会在编辑器中看到一些标识为红色虚线的代码检查警告，可以忽略。这些包括长行或不需要的新行。尽管如此，这些不应影响您的应用程序正常运行。

### 🔎 第2步：生成一个新端点

接下来，通过在`main.py`文件的最后一个路由下方添加注释，使用GitHub Copilot生成一个新端点。

```python
# 创建一个接受带有名为"text"的单个字段包含JSON主体并返回文本校验和的FastAPI端点
```

您可能会收到一个使用未导入的模块或库的建议。如果是这样，您可以选择生成的代码并使用Command + I（Apple）或Control + I（Windows）并添加一个提示来帮助您导入正确的模块。这种小弹出窗口称为内联聊天，是与GitHub Copilot交互的另一种方式。

### 🐍 第3步：解释代码

`generate()`路由使用单行代码创建伪随机令牌ID，可能难以完全理解。选择整个函数，然后右键点击选择，选择Copilot菜单项，然后选择“解释此”选项。GitHub Copilot聊天界面将打开左侧，并提供一个有用的解释，您可以用它来互动更多问题。

最后，通过访问`/docs`端点并确认该端点显示来验证新端点是否工作。

🚀 恭喜，通过此练习，您不仅使用Copilot生成代码，还以一种互动和有趣的方式完成了它！您可以使用GitHub Copilot不仅生成代码，还可以编写文档，测试您的应用程序等。

### 💡 第4步：使用斜杠命令

既然您已经使用GitHub Copilot生成并解释了代码，您还可以探索一些其他替代方法来执行开发者任务。这些额外的挑战将帮助您深入了解其他GitHub Copilot功能，除了您已经知道的功能。这些额外挑战中，您将使用聊天界面。如果您尚未打开它，请单击左侧栏上的GitHub Copilot聊天图标。

**生成文档**
 
在`main.py`打开的情况下，使用聊天界面输入以下文本：

```
/docs 我需要为这些API路由编写文档。帮助我生成可以放入此项目的README.md文件中的文档
```

提示的`/docs`部分称为“斜杠命令”，它是GitHub Copilot的一个特定功能，允许您编写文档。如果结果看起来不错，请将它们添加到README.md文件的新部分中。

**生成测试**
 
当前代码没有任何测试。对于此挑战，您将使用`/tests`斜杠命令。在`main.py`打开的情况下，使用聊天界面输入以下提示：

```
/tests 帮助我使用FastAPI测试客户端和Pytest框架为generate()路由编写测试。帮助我了解应将测试文件放在哪里，如何将Pytest依赖项添加到我的项目中，以及如何运行测试
```

`/tests`斜杠命令将引导您编写路由的新测试，并为您提供所需的一切，以便您可以验证工作。

**工作区挑战**
 
最后，您将有机会使用一个代理。代理是GitHub Copilot在Visual Studio Code中的一个特殊功能，允许与GitHub Copilot共享特定上下文。对于最终挑战，您将使用`@workspace`代理，其中包括来自当前工作区的文件以提供更多上下文。您将解决一个与如何运行整个应用程序有关的问题。在这种情况下，您将增强README.md，以更详细地说明多个文件。使用`@workspace`有助于在无需打开许多文件的情况下提供更多上下文。

对于最终挑战，不需要打开任何文件。在GitHub Copilot聊天窗口中使用以下提示：

```
@workspace 我想提供使用uvicorn web服务器运行此应用程序的说明，还需要提供正确安装依赖项的说明以及FastAPI框架的一些特点。我将使用此内容改进README.md文件
```

结果应该是一份关于FastAPI的很好说明，如何运行应用程序以及如何安装依赖项。在响应的最顶部可能会包括所有参考资料，用于确定需要使用哪些文件以提供适当的GitHub Copilot上下文。

## 法律声明

Microsoft和任何贡献者授予您对本存储库中Microsoft文档和其他内容的许可
根据[创作共用 署名4.0国际公共许可协议](https://creativecommons.org/licenses/by/4.0/legalcode)，
请参阅[LICENSE](LICENSE)文件，并授予您对存储库中的任何代码的许可根据[MIT许可证](https://opensource.org/licenses/MIT)，请参阅
[LICENSE-CODE](LICENSE-CODE)文件。

Microsoft、Windows、Microsoft Azure和/或文档中提到的其他Microsoft产品和服务
可能是Microsoft在美国和/或其他国家/地区的商标或注册商标。
本项目的许可不授予您使用任何Microsoft名称、徽标或商标的权利。
Microsoft的一般商标指南可以在http://go.microsoft.com/fwlink/?LinkID=254653找到。

隐私信息可以在https://privacy.microsoft.com/en-us/找到

Microsoft和任何贡献者保留所有其他权利，无论是根据各自的版权、专利，
或商标，是否通过暗示、禁止反言或其他方式取得。