# doodles

原型与设计草稿的集合库。每个项目一个独立目录,通过 `index.html` 作为入口索引,部署在 GitHub Pages(`design.flooc.cn`)。

## 当前项目

### ZD — 内容社区

一个 shadcn 风格的阅读优先内容社区原型,共 14 屏:

| 屏幕 | 文件 | 说明 |
|---|---|---|
| 首页 Feed | `52a14099-…/zd-feed-home.html` | 双栏信息流:AI 推荐 / AI 发布 / 关注,侧栏话题与 AI 助手 |
| 帖子详情 | `52a14099-…/zd-post.html` | 单帖阅读、点赞、评论与分享的完整互动流 |
| 发布 | `52a14099-…/zd-create.html` | 编辑器 + AI 辅助写作,从草稿到发布 |
| 搜索与话题 | `52a14099-…/zd-search.html` | 关键词搜索与话题浏览 |
| 话题详情 | `52a14099-…/zd-topic.html` | 话题介绍、相关帖与相关话题,支持 `?t=` 直达 |
| 通知 | `52a14099-…/zd-notifications.html` | 关注、点赞、评论的动态中心 |
| 我的 | `52a14099-…/zd-me.html` | 个人主页,作品、关注与账号数据一览 |
| 他人主页 | `52a14099-…/zd-profile.html` | 作品与简介分栏,关注 / 私信,支持 `?user=` 直达 |
| 偏好设置 | `52a14099-…/zd-settings.html` | 账号、隐私、通知偏好与个性化设置 |
| 社区准则 | `52a14099-…/zd-community-guidelines.html` | 8 节准则文档,侧栏目录定位 |
| 帮助中心 | `52a14099-…/zd-help.html` | 快速上手、FAQ 与联系支持 |
| 登录与注册 | `52a14099-…/zd-auth.html` | 登录 / 注册 / 忘记密码三模式 |
| 草稿箱 | `52a14099-…/zd-drafts.html` | 草稿列表、统计、继续编辑与删除,支持 `?draft=` |
| 私信 | `52a14099-…/zd-messages.html` | 会话列表 + 聊天线程,发送与自动回复 |

页面间通过 `?user=<key>`(作者:chenmo / linwan / suhang / gunan / zhiyun)、`?t=<话题名>`、`?draft=<draft-wb|draft-podcast|draft-prompt>`、`?owner=1`(帖子详情演示作者编辑 / 删除)、`#pane-*` 锚点互通,全站无死链。各页头部均有「登录」入口指向 `zd-auth.html`。

设计语言:纯白画布 + 描边分层的白卡片,slate 中性色正文,纯黑作为唯一强调色;Geist Sans 作显示与正文字体,Fira Code 作等宽字体。

## 使用

- 本地直接在浏览器打开 `index.html` 进入原型索引。
- 部署:GitHub Pages 绑定 `CNAME` 指向 `design.flooc.cn`。

## 结构

```
index.html              # 原型索引首页
CNAME                   # Pages 自定义域名
<project-id>/           # 单个项目目录
  zd-*.html             # 项目内各屏幕
```
