# 从第一次 Fork，到第一份 PR 🌱

准备一台电脑、浏览器和 GitHub 账号即可。你可以慢慢来，每完成一步就停下来看看。

我们会用到几个英文按钮，下面保留按钮原文，并解释它们的意思。

| 页面上的词 | 在这里的意思 |
| --- | --- |
| Repository / Repo | 仓库，一个存放文件的项目空间 |
| Fork | 把项目复制到你的账号，得到自己的副本 |
| Markdown / `.md` | 用普通文字加简单符号排版的文件 |
| Commit changes | 保存一次改动，并留下说明 |
| Branch | 分支，让这次改动有自己的位置 |
| Pull Request / PR | 请原项目接收你的改动 |
| Issue | 公开提问或讨论的帖子 |

## 0. 注册并登录

打开 [GitHub](https://github.com)，点击 **Sign up** 注册，按页面提示完成邮箱验证，然后登录。用户名会出现在仓库地址和你的宣言文件名里；昵称就可以。

这是一个公开项目。宣言、PR 和 Issue 都可以被别人看到，提交历史也可能保留旧内容。只写愿意公开的文字。若希望隐藏提交邮箱，可先到 **Settings → Emails** 开启 **Keep my email addresses private**，保存文件时使用 GitHub 提供的 no-reply 邮箱。

## 1. Fork：得到自己的副本

1. 打开 [一颗种子原仓库](https://github.com/Hertz-chat/seed)。
2. 点击右上角 **Fork**。
3. 在 **Owner** 选择你自己的账号。仓库名保持 `seed` 即可；只复制默认分支的选项可以保持勾选。
4. 点击 **Create fork**。

**停下来检查：** 页面顶部应该变成 `你的用户名 / seed`，下面有 `forked from Hertz-chat/seed`。接下来在这个副本里操作。

如果已经 Fork 过，直接打开自己的副本即可，不用重复创建。

## 2. 新建你的宣言

先看 [示例](seeds/example.md)，读完后回到自己的副本首页。

1. 在副本首页，点击文件列表上方的 **Add file → Create new file**。窗口窄时按钮可能收进菜单，试着放大窗口。
2. 在文件名输入框填写 `seeds/你的GitHub用户名.md`。把「你的GitHub用户名」替换成真实用户名。
   - 假设用户名是 `little-sprout`，就写 `seeds/little-sprout.md`。
   - 这里从仓库首页创建，`seeds/` 会指定文件所在目录。不要修改 `example.md`。
3. 在正文里写下你的宣言。下面这段可以复制，也可以随意改写：

```markdown
# 我的第一颗种子

你可以叫我小芽。

我一直想尝试……

今天，我决定从这里开始。
```

`# `（井号后加一个空格）会把一行变成标题。两段文字之间空一行就可以了。即使只写普通文字，也是一份有效的 Markdown 文件。

4. 点击 **Preview** 看看排版，再回到编辑视图继续修改。
5. 点击 **Commit changes…**，在 **Commit message** 写「种下我的第一颗种子」。
6. 选择 **Create a new branch for this commit and start a pull request**，给新分支起名 `my-first-seed`。如果页面没有这个选项，先回到副本首页，通过文件列表上方的分支菜单输入 `my-first-seed` 并创建分支，再在该分支新建文件。
7. 点击 **Propose changes** 或 **Commit changes**，以页面实际显示为准。

**停下来检查：** 在副本的 `my-first-seed` 分支里，能看到 `seeds/你的用户名.md` 和刚才写的文字。这一步是保存，下一步才是把协作邀请送出去。

## 3. 把 PR 发回原仓库

保存后可能自动进入比较页面。无论从哪里进入，都先检查目标仓库。

一个固定入口：打开 [原仓库的 Pull requests](https://github.com/Hertz-chat/seed/pulls)，点击 **New pull request**，再点击 **compare across forks**。

按下面选择：

| 字段 | 选择 |
| --- | --- |
| base repository（接收改动的仓库） | `Hertz-chat/seed` |
| base（接收改动的分支） | `main` |
| head repository / head fork（你的副本） | `你的用户名/seed` |
| compare（有你的宣言的分支） | `my-first-seed` |

**这一步的方向：你的副本 → Hertz-chat/seed。**

查看下方的文件差异：应该只新增你的宣言文件，没有更改示例或其他人的文字。

点击 **Create pull request**，填写：

- 标题：`种下我的第一颗种子：你的用户名`
- 说明：`这是我的第一份宣言，也是我的第一次 PR。请帮我看看。`

再次点击 **Create pull request** 提交，使用普通 PR 即可。

**完成检查：** 地址应该以 `https://github.com/Hertz-chat/seed/pull/` 开头，页面状态是 **Open**。恭喜，你已经送出了第一次协作邀请！

维护者会查看并合并。看到 **Merged** 后，你的宣言就进入原仓库了。你不需要自己点击 Merge。

## 4. 如果卡住了

| 看到的情况 | 可以这样做 |
| --- | --- |
| 找不到 Fork / 新建按钮 | 确认已登录，并回到仓库 Code 页；放大浏览器窗口 |
| 显示没有差异 / nothing to compare | 检查保存是否完成，compare 是否选了 `my-first-seed`，base 是否是原仓库的 `main` |
| PR 发到了自己的副本 | 在原仓库重新打开 New pull request，按上表选择；原先误开的 PR 可以关闭 |
| 文件名已存在 | 如果是自己的旧宣言，打开它点击编辑按钮，在新分支修改；不要覆盖别人的文件 |
| 提交后发现错字 | 打开副本的 `my-first-seed` 分支，编辑同一个文件并保存到该分支；已有的 PR 会更新，不用重发 |
| 提示有冲突 | 不用急着解决，在 PR 评论里告诉维护者「我需要帮助」 |

也可以在 [原仓库 Issues](https://github.com/Hertz-chat/seed/issues/new/choose) 提问。你没有义务第一次就熟悉这些按钮。

## 5. 可选：说说你希望种子长成什么

在原仓库点击 **Issues → New issue**，选择「让种子生长，或问一个问题」，如果出现 **Get started** 就点击它。填一个标题和你想说的话，再点击 **Submit new issue**。

比如：「我想学做一个读书记录页面，能不能一起试试？」

做到这里，已经足够。下一次探索可以等你想出发的时候再开始。

---

按钮位置可能随 GitHub 更新变化。核对参考（2026-10-10）：[Fork 官方说明](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/fork-a-repo?tool=webui)、[网页新建文件](https://docs.github.com/en/repositories/working-with-files/managing-files/creating-new-files)、[从 Fork 提交 PR](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork)。
