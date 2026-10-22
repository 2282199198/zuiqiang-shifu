# 安装说明

这份是写给 AI 看的，人照着做也行。用户把这个仓库的链接或者压缩包交给你，意思就是：把最强师傅装成**一个** Skill。

## 先弄清楚三件事

1. 整个文件夹就是一个 Skill，入口是根目录的 `SKILL.md`。全包只有这一个 `SKILL.md`。
2. 各子目录里的 `MODULE.md` 是这个 Skill 自己的模块，由根 `SKILL.md` 按需去读。不要把它们拆出来单独装，也不要改回 `SKILL.md`，不然会被认成十几个互不相干的 Skill，总路由、去 AI 味终检和真人润色都会被绕过去。
3. 文件夹名必须是 `zuiqiang-shifu-v3`，跟 `SKILL.md` 里的 `name` 一样。GitHub 上点 Download ZIP 下来的压缩包，解开是 `zuiqiang-shifu-v3-main`，要把 `-main` 去掉。

## 装

**第 1 步：拿到文件。**

- 有 git：`git clone <仓库链接> <技能目录>/zuiqiang-shifu-v3`
- 没有 git：下载压缩包、解压，外层文件夹改名成 `zuiqiang-shifu-v3`，整个放进技能目录

**第 2 步：放对地方。** 下面是个人级目录，放这里所有项目都能用：

| 工具 | 技能目录 |
|---|---|
| Claude Code | `~/.claude/skills/` |
| Codex | `~/.agents/skills/` |
| Cursor | `~/.cursor/skills/` 或 `~/.agents/skills/` |
| GitHub Copilot（VS Code、Visual Studio、Copilot CLI） | `~/.copilot/skills/` 或 `~/.agents/skills/` |
| Gemini CLI | `~/.gemini/skills/` |
| OpenCode | `~/.config/opencode/skills/` 或 `~/.agents/skills/` |
| 别的工具 | 先查它自己的文档；不少工具都认 `~/.agents/skills/` |

Windows 上 `~` 就是 `%USERPROFILE%`，一般是 `C:\Users\用户名`。只想在某一个项目里用，就放到项目根目录下对应的 `.claude/skills/`、`.agents/skills/` 这类目录。

这张表是 2026 年各家文档里的写法，以后可能会变。对不上的时候，以你这个工具的官方文档为准。

**第 3 步：旧版先删。** 技能目录里已经有旧版，比如 `zuiqiang-shifu-v2` 或者更早的 `zuiqiang-shifu`，先把旧文件夹整个删掉，再放新的。直接覆盖会把新旧文件混在一块，旧版留下的 `SKILL.md` 也还在。以前装在 `~/.codex/skills/` 下的，也一起删掉。

**第 4 步：只装一处。** Cursor、Copilot、OpenCode 会同时读 `~/.claude/skills/` 和 `~/.agents/skills/`，两处都放，列表里就会出现两个最强师傅。

**第 5 步：检查。**

- `<技能目录>/zuiqiang-shifu-v3/SKILL.md` 在，而且没套两层。`zuiqiang-shifu-v3/zuiqiang-shifu-v3/SKILL.md` 是错的。
- 整个文件夹里只找得到一个 `SKILL.md`（macOS / Linux：`find <技能目录>/zuiqiang-shifu-v3 -name SKILL.md`）。
- 想核对文件齐不齐，在文件夹里跑 `sha256sum -c MANIFEST.sha256`（macOS 用 `shasum -a 256 -c MANIFEST.sha256`）。Windows 上可以跳过。

**第 6 步：跟用户说一声**装在哪了，让他新开一个会话或者重启工具。已经开着的会话不一定读得到新装的 Skill。

装了 Node.js 的话，也可以直接 `npx skills add <GitHub 用户名>/<仓库名>`，照它的提示选你用的工具。装完照样做第 5 步。

## 工具没有 Skill 功能

网页版聊天这类没有技能目录的，把整个压缩包或者解压后的整个文件夹传进对话或项目，先读根目录的 `SKILL.md` 和 `WORKFLOW_PROTOCOL.md`，之后每次按 `SKILL.md` 的路由去读对应的 `MODULE.md`。只传一个 `SKILL.md` 用不全，模块和规则都在别的文件里。

有些网页版能在设置里上传 Skill 压缩包。这时候用解开后外层就是 `zuiqiang-shifu-v3` 的那种压缩包；GitHub 自动打的包外层带 `-main`，要先改名再重新压。

## 装好了试一下

- 问“最强师傅现在是哪个版本”，应该答 V3.0。
- 让它出选题，应该出 3–5 个、标一个推荐，不会分“离线”“联网”两组。
- 打开工具的技能列表（比如 Codex 里输入 `/skills`），只该看到一个 `zuiqiang-shifu-v3`。看到 topic-engine、viral-factory 这些模块名，说明还有旧版没删干净，回到第 3 步。
