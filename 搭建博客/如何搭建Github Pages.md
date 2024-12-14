GitHub Pages 是通过 GitHub 托管和发布的公共网页。
# 创建仓库
1. 首先登陆了github之后，点击新建存储库：
![!\[\[Pasted image 20241214155411.png\]\]](assets/image17.png)
2. 输入`username.github.io`作为存储库的名称，username替换成你自己想命名的名称。同时可以选择可见性，选择添加README文件，.gitignore文件选择Github Pages的模板
![!\[\[Pasted image 20241214160017.png\]\]](assets/image18.png)
3. 创建完成：
![!\[\[Pasted image 20241214160208.png\]\]](assets/image19.png)
进入设置，选择Github Pages从哪个分支来构建，我这里默认选择main分支的根文件
![!\[\[Pasted image 20241214160658.png\]\]](assets/image20.png)
保存完成之后，项目就创建完成，然后会自动部署，部署完成之后，这里会显示：
![!\[\[Pasted image 20241214162849.png\]\]](assets/image21.png)
点进去之后，你可以看到部署的记录和网站的链接：
![!\[\[Pasted image 20241214162924.png\]\]](assets/image22.png)
# 提交文档
1. （可选）你可以对你的默认main分支进行保护，防止有人随意在上面进行提交：
![!\[\[Pasted image 20241214162155.png\]\]](assets/image23.png)
在Rules里面的Rulesets里面新建一条，因为我已经建好了，所以里面有一个，
在这里面，我创建的规则是，对于默认的Default分支，限制了以下的规则，你可以根据自己情况来选择
![!\[\[Pasted image 20241214162254.png\]\]](assets/image24.png)
以下是Gemini AI对于配置的方法描述：
> 在 GitHub 上，限制直接向 main（或 master）分支提交代码是一种常见的最佳实践，它可以有效地维护代码库的稳定性和质量。通过强制使用 Pull Request（PR）流程，可以确保所有更改都经过代码审查和测试，然后再合并到主分支。以下是如何在 GitHub 上设置这种限制的几种方法：
> 
> **1. 使用分支保护规则：**
> 
> 这是最常用的方法，它允许你配置各种规则来保护你的分支。以下是如何操作：
> 
> - **进入仓库设置：** 在你的 GitHub 仓库页面，点击 “Settings”（设置）。
> - **导航到分支设置：** 在左侧边栏的 “Code and automation”（代码和自动化）部分，点击 “Branches”（分支）。
> - **添加分支保护规则：** 在 “Branch protection rules”（分支保护规则）部分，点击 “Add rule”（添加规则）。
> - **指定要保护的分支：** 在 “Branch name pattern”（分支名称模式）下，输入 `main`（或 `master`，取决于你的主分支名称）。
> - **配置规则：**
>     - **Require pull requests before merging（合并前需要拉取请求）：** 勾选此项以强制使用 PR 流程。你可以设置需要的最少审查人数。
>     - **Require status checks to pass before merging（合并前需要通过状态检查）：** 如果你使用了 CI/CD（持续集成/持续交付）工具，勾选此项以确保所有测试都通过。
>     - **Require conversation resolution before merging（合并前需要解决所有对话）：** 勾选此项以确保所有代码审查的评论都已解决。
>     - 其他选项，如 “Include administrators”（包含管理员）和 “Allow force pushes”（允许强制推送），根据你的需要进行配置。通常不建议允许强制推送到受保护的分支。
> - **保存更改：** 点击 “Save changes”（保存更改）。

2. 接下来创建一个分支（有很多种办法），然后本地clone了之后，在新分支上提交文档，最终在Pull request里面提交合并的请求即可