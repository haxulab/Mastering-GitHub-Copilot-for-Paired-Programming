<header>

# 使用 GitHub Copilot 与 JavaScript

在本模块中，我们将继续深入了解 GitHub Copilot 的功能，学习如何使用它来增强编码体验。想象一下，更快、更轻松地编写代码——GitHub Copilot 通过根据你的评论和代码的上下文无缝生成建议，使这一切成为现实。

作为一个寻求提高生产力的开发者，你将开启一段掌握 GitHub Copilot 功能的旅程，重点是它在 JavaScript 中的应用。在模块结束时，你将掌握编写提示，以便利用 GitHub Copilot 扩展在 Visual Studio Code 中生成有价值的建议。提升你的编码技能，使用 GitHub Copilot 来增强 JavaScript 项目，亲身体验这种 AI 编程助手如何通过自动完成式的建议改变你的开发工作流程。

通过掌握 GitHub Copilot，你不仅能够在 Codespaces 中配置存储库，还能高效地利用这个 AI 工具来改进你的编码项目。准备好在这次动态学习冒险中革新你的编码体验，并提高你的生产力吧！

</header>


- **适用于**: 开发人员、DevOps 工程师、软件开发经理、测试人员。
- **你将学到的内容**: 利用 GitHub Copilot 创建代码并为你的工作添加注释。
- **你将构建的项目**: JavaScript 文件，将由 Copilot AI 生成代码和注释建议。
- **先决条件**: 使用 GitHub Copilot 你必须订阅一个有效的 GitHub Copilot 订阅。免费注册30天 [Copilot](https://github.com/settings/copilot)。
- **时长**: 本模块可以在一小时内完成。


在本模块结束时，你将掌握以下技能:

- 编写提示以从 GitHub Copilot 生成建议
- 应用 GitHub Copilot 来改进你的项目。


## 先决条件阅读:
- [使用 GitHub Copilot 进行提示工程介绍](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [使用 GitHub Copilot 与 JavaScript](https://learn.microsoft.com/training/modules/introduction-copilot-javascript/?WT.mc_id=academic-113596-abartolo)


## 要求

1. 启用你的 [GitHub Copilot 服务](https://github.com/github-copilot/signup)
1. 使用 Codespaces 打开 [这个存储库](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-javascript?quickstart=1)



## 💪🏽 练习

**右键点击以下 Codespaces 按钮，在新标签页中打开你的 Codespaces**

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526682619)

在这个模板组合中，我们有一个基于 React 的 web 应用程序，您可以轻松个性化和部署，只使用您的 web 浏览器。

**注意**: 请忽略 GitHub Codespace 内给出的说明。对于本实验，一定要遵循这里的说明。


### 🛠 第 1 步: 自定义 web 应用

使用你自己的链接来自定义组合。转到 `src/App.jsx` 并用你的信息更新 `siteProps`。`siteProps` 变量是一个 JavaScript 对象，包含用于自定义站点的键值对，它应该是这样的：

```javascript
const siteProps = {
  name: "Alexandrie Grenier",
  title: "Web Designer & Content Creator",
  email: "alex@example.com",
  gitHub: "microsoft",
  instagram: "microsoft",
  linkedIn: "satyanadella",
  medium: "",
  twitter: "microsoft",
  youTube: "Code",
};
```
### 📖 第 2 步: 解释代码

现在，让我们使用斜杠命令来解释代码的某部分的作用。高亮以下代码：

```javascript
};

const primaryColor = "#4E567E";
const secondaryColor = "#D2F1E4";

const App = () => {
  return (
    <div id="main">
      <Header />
      <Home name={siteProps.name} title={siteProps.title} />
      <About />
      <Portfolio />
      <Footer {...siteProps} primaryColor={primaryColor} secondaryColor={secondaryColor} />
    </div>
  );
};
```
高亮后，按 Ctrl + I (Windows) 或 Cmd + I (Mac) 并输入 **/explain**。你应该在 Copilot 聊天窗口中收到类似这样的响应：

```
这段 JavaScript 代码是用 React 编写的，React 是一个流行的构建用户界面的库。代码定义了一个名为 App 的函数组件。App 组件是你应用程序的根组件。它是所有其他组件（Header, Home, About, Portfolio, Footer）被调用和渲染的地方。App 组件返回一个 JSX（JavaScript XML）结构，看起来类似于 HTML。这个 JSX 结构定义了 App 组件应在屏幕上渲染的内容。在 JSX 中，有一个 id 为 "main" 的 div。在这个 div 内，几个组件被渲染：Header, Home, About, Portfolio 和 Footer。Home 组件被传递了两个 props：name 和 title，它们都是 siteProps 对象的属性。Footer 组件被传递了几个 props。...siteProps 语法使用 JavaScript 的展开操作符将 siteProps 的所有属性作为单独的 props 传递。除了 siteProps，还有两个常量被传递：primaryColor 和 secondaryColor。这些常量在文件顶部定义。请记住，React 中的 props（属性的缩写）是组件之间通信的方式。如果你将组件视为函数，那么 props 就是这些函数的参数。它们从父组件（在本例中是 App）传递到子组件（Header, Home, About, Portfolio, Footer）。
```

让我们深入一点。注意到 Copilot 聊天现在提供了一个后续问题建议供你提问。点击 GitHub Copilot 在窗口底部建议的通常以 "What is the purpose..." 开头的问题，并查看提供的答案。例如，如果 GitHub Copilot 提供的问题如下：

What is the purpose of using props in React components? 

你应该得到类似这样的答案：

```
在 React 中，props（属性的缩写）用于将数据从一个组件传递到另一个组件，就像函数参数一样。它们是只读的，有助于使组件可重用和动态化。例如，在你的代码中，Home 组件被传递了 name 和 title 作为 props。这意味着 Home 组件可以使用这些值来显示动态内容。Footer 组件也被传递了几个 props，包括 siteProps 的所有属性以及 primaryColor 和 secondaryColor 常量。这里有一个比喻：将组件看作一个自定义的 HTML 元素，而 props 则是该元素的属性。就像你可以传递不同的属性给 HTML 元素（比如 <img src="image.jpg" alt="An image">），你也可以传递不同的 props 给 React 组件（比如 <Home name="John" title="Developer" />）。这使你的组件更灵活和可重用。例如，你可以使用相同的 Home 组件，通过不同的 props 来显示不同的内容。
```

你是否注意到，当你点击 Copilot 聊天窗口中的建议问题时，它使用了类似以下的命令来提问：

```
@workspace /explain What is the purpose of using props in React components?
```

@workspace 代理，如 Copilot，会填补遗漏的细节，帮助人类忽略或未完全描述的一切。在被提示时，与其立即回应，Copilot 先查看工作环境中的文件和文件夹：

1. 它检查文件/文件夹的名称，看哪些可能相关。
2. 它读取文件内容，有时是全部内容，有时是部分内容，取决于内存限制。
3. 它从收集的信息中创建上下文。
4. 它使用提示的上下文和收集的信息进行回应。


### 🔎 第 3 步: 使用提示为社交媒体图标添加动画

动画可以使社交媒体部分更吸引人。请 Copilot 帮忙为图标添加动画。跳到文件末尾，并在 `src/styles.css` 文件中编写以下提示：

```css
/* 为社交图标添加一个惊人的动画 */
```

Copilot 的建议应该类似于以下内容：

```css
img.socialIcon:hover {
  animation: bounce 0.5s;
  animation-iteration-count: infinite;
}

@keyframes bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
```

### 🚀 第 4 步: 了解如何运行应用程序
点击左侧边栏上的聊天图标打开 GitHub Copilot 聊天，并使用输入部分提问：

```
@workspace 我想了解如何运行这个 React 应用程序
```

这个提示使用了 `@workspace`，它是 GitHub Copilot 聊天的一个特殊功能，允许你包含更多上下文以获得更完整的答案。尝试使用聊天室面板进行其他查询，以获取更互动的工作流程。

### 结论
你的站点应该已经在你的 Codespace 中运行，且更改会自动重新加载到页面上。要查看效果，悬停在页脚的一个社交媒体图标上，看看魔法发生！

**注意**: 如果悬停效果不起作用，请刷新 Codespace 浏览器窗口。

恭喜！通过练习，你已经使用 GitHub Copilot 生成代码，并且以一种互动和有趣的方式完成了它！你可以使用 GitHub Copilot 来不仅生成代码，还可以撰写文档，测试你的应用程序等等。