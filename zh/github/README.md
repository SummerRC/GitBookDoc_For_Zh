# GitHub Integration

GitBook 可以完美地集成 [GitHub](https://github.com) 并用后者托管你的书籍文件.

## 连接你的账号/权限

在连接你的书籍与 GitHub 之前, 你需要授权 GitBook 访问你的 GitHub 账户.

在你的 [账户设置](https://www.gitbook.com/settings), 连接你的 GitHub 账户需要正确的权限:

- **Default permissions**: 只允许你在登录的时候访问 only access your GitHub account to authenticate you during login
- **Access to webhook**: access your GitHub account to create a webhook on your specified repository (See [webhooks](#webhooks)).
- **Access to public repositories**: access your GitHub repository from the webeditor so that you can edit your book easily from GitBook (only public repositories)
- **Access to private repositories**: same as above but with access to private repositories

## 从 GitHub 导入一本书籍

当你创建一本新的书籍时, 通过 `GitHub` 选项卡你可以选择要导入的 GitHub 仓库.

The newly created book will be setup with your repository's content, and a webhook will be automatically added.

## Webhooks

Webhooks notify GitBook when your GitHub repository changes.

If your GitHub changes are not available on GitBook, the main source of the problem is the webhook. You can check the state of your webhook in your repository's settings.


## Link a book and a GitHub repository

When your GitHub account is correctly linked to your GitBook account, linking a book to a repository is easy.

**Caution:** When you specify a GitHub repository in your book's settings, it will take priority over GitBook's git repository, this means that the editor will directly edit content on GitHub.

**The sync is unidirectional**, only changes made on GitHub will trigger builds on GitBook, GitBook **will not** update your GitHub repository with any content written before.

1. Open the GitHub section in your book settings
2. Enter your repository id (such as: `YourGitHubUserName/RepoName`)
3. Save your settings
4. Click on the button **Add a deployment webhook**

You can now edit your GitHub repository from the web editor (if you have authorized the correct permissions), and your commit on GitHub will trigger builds on GitBook

## Common Errors:

##### My Book is not being updated / I can't see any builds

If you linked your GitHub repository to a GitBook but editing content doesn't trigger any build.
Verify that the webhook has been correctly added to your GitHub repository (in your GitHub repository settings -> Webhook). If the webhook is not present or invalid, add it back from your book's settings.

##### Change of book name/owner

If you transferred your book to a new owner, the webhook is now invalid, you need to add it back.
