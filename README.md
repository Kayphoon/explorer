# explorer

本地代码库只读探查 skill：仓库结构陌生、需要跨层跨目录找实现、或要少量只读 git 历史取证时，把多角度检索委派给原生只读子代理，返回带路径的结论。

这是自包含分发单元：根目录 `SKILL.md` 是入口，`references/role.md` 是委派时逐字嵌入的行为正文。

## 安装

```bash
# 公开 skills 协议
npx skills add Kayphoon/explorer

# 本仓库自带安装器（零依赖，默认装到 ~/.agents/skills）
# 跟随最新的 1.x 发布：自动解析到匹配的最高 tag
npx github:Kayphoon/explorer#semver:^1.0.0
npx github:Kayphoon/explorer#semver:^1.0.0 --target codex
npx github:Kayphoon/explorer#semver:^1.0.0 --project ./my-repo
```

`#semver:^1.0.0` 每次都会解析到最新的 1.x tag，适合日常使用；想锁死具体版本就写 `#v1.0.2`，或者直接写 commit SHA。省略 ref 写 `npx github:Kayphoon/explorer` 则跟随默认分支 HEAD，可能包含还没发版的提交；替换已装副本加 `--force`。

装好后新开一次会话让运行时重新发现 skill。

## 许可与来源

本 skill 的行为文本是 [oh-my-openagent](https://github.com/code-yeongyu/oh-my-openagent) 中 MIT 许可 agent 提示词的改编版，不是上游原文件，也未获上游作者背书。上游署名与许可全文随本仓库分发：见 [NOTICE.md](NOTICE.md) 与 [LICENSE.txt](LICENSE.txt)。
