<header>

# 使用 GitHub Copilot 高级功能

GitHub Copilot 不仅仅是代码建议。作为一名软件工程师，你经常会试图理解现有代码，并通过文档、测试和自动化来增强它。

在本模块中，你将使用 GitHub Copilot 的高级功能，这些功能将允许你与代码进行互动，并有效地应用建议和知识。

你将使用基于 Python 的现有 HTTP API 进行更改、修复错误、编写文档和测试你将实现的新端点。

</header>


- **适合人群**: 开发人员，DevOps 工程师，软件开发经理，测试人员。
- **你将学到**: 使用 GitHub Copilot 的高级功能进行测试、文档编写和代码工作。
- **你将构建**: 新的 HTTP API 路由，以及文档和测试以验证其正确性。
- **前提条件**: 要使用 GitHub Copilot，你必须拥有一个有效的 GitHub Copilot 订阅。注册获取30天免费 [Copilot](https://github.com/settings/copilot)。
- **时间**: 本模块可以在一小时内完成。

在本模块结束时，你将掌握以下技能:

- 使用 GitHub Copilot 的高级功能，如内联聊天、斜杠命令和代理。
- 与 GitHub Copilot 互动，深入了解你的项目并对其提问。

## 必读内容:
- [GitHub Copilot 提示工程介绍](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [使用 GitHub Copilot 的高级功能](https://learn.microsoft.com/training/modules/advanced-github-copilot/?WT.mc_id=academic-113596-abartolo)

## 要求

1. 启用你的 [GitHub Copilot 服务](https://github.com/github-copilot/signup)
1. 使用 Codespaces 打开 [此库](https://codespaces.new/MicrosoftDocs/mslearn-advanced-copilot)

## 💪🏽 练习

**右键单击以下 Codespaces 按钮以在新标签中打开你的 Codespace**
 
[![在 GitHub Codespaces 中打开](https://github.com/codespaces/badge.svg)](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

当前的 API 未公开 country/{country}，需要实现以列出城市。该路由应仅允许 GET HTTP 请求，并使用 JSON 响应提供该国家、城市和给定月份的历史高低数据。

与任何实现一样，此添加应该包括至少一个测试函数，以与 pytest 运行器和测试框架一起使用。

### 🛠 第一步: 添加新路由
在我们的第一个练习中，我们将在 API 中创建一个新路由。转到 main.py 文件，并使用 `ctrl` + `i`（在 Windows 上）或 `cmd` + `i`（在 Mac 上）的内联聊天，要求 GitHub Copilot 帮助你创建一个显示国家城市的新 API。

在内联聊天中使用以下提示:

```
创建一个公开国家城市的新路由。
```

这个提示应该为你提供类似如下的内容:

```python
# 创建一个公开国家城市的新路由:
@app.get('/countries/{country}')
def cities(country: str):
    return list(data[country].keys())
```

> [!注意]
> 试用你新的路由并调整你的提示，直到结果符合预期。

### 🔎 第二步: 创建测试
现在，你已经创建了一个新路由，让我们使用 Copilot Chat 为此路由创建一个测试，使用西班牙作为国家。记得选择你的代码，并要求 Copilot Chat 帮助你创建我们刚刚创建的这个特定 API 的测试。

使用以下提示与 GitHub Copilot Chat 进行互动:

```
/tests 帮我为这个路由创建一个新的测试，使用西班牙作为国家。
```

![Copilot Chat 图像示例](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-advanced-copilot/main/images/ideascopilot.png)

一旦 Copilot 帮助你创建了测试，请测试它。如果它不像预期的那样工作，请随时在聊天中与 Copilot 分享这些细节。例如:

```
这个测试不太对，它没有包括不存在的城市。只有塞维利亚是 API 的一部分。
```

它应该给你另一个解决方案。继续尝试，直到达到预期的结果。

### 🐍 第三步: 使用代理编写项目
在此步骤中，我们将使用代理（工作区）来编写有关如何运行此项目的项目文档。在 GitHub Copilot Chat 中，我们将尝试以下提示:

`> @workspace 帮我使用代理编写有关如何运行此项目的项目文档。`

最后，通过访问 `/docs` 端点并确认该端点显示，以验证新端点是否正常工作。

### 💡 第四步: 使用斜杠命令

现在你已经使用 GitHub Copilot 生成并解释了代码，你还可以探索一些其他替代方法来执行开发人员任务。这些额外的挑战将帮助你深入了解除了你已经知道的功能以外的其他 GitHub Copilot 功能。对于这些额外的挑战，你将使用聊天界面。如果尚未打开，请单击左侧边栏中的 GitHub Copilot Chat 图标。

🚀 恭喜你，通过练习，你已经使用了许多不同的 GitHub Copilot 功能，使你能够更好地处理不同的项目。你互动地使用了一些功能来编写测试、文档，并了解现有代码的更多信息。

## 法律声明

Microsoft 和任何贡献者授予你对本存储库中 Microsoft 文档和其他内容的使用权，依照 [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode)，详见 [LICENSE](LICENSE) 文件，并授予你对存储库中的任何代码的使用权，依照 [MIT License](https://opensource.org/licenses/MIT)，详见 [LICENSE-CODE](LICENSE-CODE) 文件。

Microsoft、Windows、Microsoft Azure 和/或文档中提到的其他 Microsoft 产品和服务可能是美国和/或其他国家的 Microsoft 商标或注册商标。
本项目的许可不授予你使用任何 Microsoft 名称、标志或商标的权利。
Microsoft 的一般商标指南可以在 http://go.microsoft.com/fwlink/?LinkID=254653 中找到。

隐私信息请访问 https://privacy.microsoft.com/zh-cn/

Microsoft 和任何贡献者保留所有其他权利，无论是根据各自的版权、专利或商标，以及通过默示、禁止反言或其他方式。