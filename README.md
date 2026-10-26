中文 | [English](README.en.md)

# 公子教代码做事 · 速查卡

一个 agent 技能，一次性列出这套东西的**全部模式、技能和命令**，以及怎么切强度、怎么关、怎么更新。

忘了怎么用的时候说一句 `ponytail help` 就行。

## 为什么有它

这套东西一共 6 个技能、3 档强度、一堆命令。用过两次之后就忘了 `/ponytail-audit` 和 `/ponytail-debt` 到底差在哪。

所以留一张卡，一张就够，看完关掉。

## 它长什么样

**三档强度**

| 强度 | 怎么开 | 变化 |
|---|---|---|
| **Lite** | `/ponytail lite` | 照做，但顺手提一句更省事的做法 |
| **Full** | `/ponytail` | 六步阶梯强制执行，默认档 |
| **Ultra** | `/ponytail ultra` | YAGNI 极端派，先质疑需求，再谈实现 |

强度一直有效，直到你改它或会话结束。

**六个技能**

| 技能 | 命令 | 干什么 |
|---|---|---|
| **ponytail** | `/ponytail` | 懒人模式本体，能用的最简方案 |
| **review** | `/ponytail-review` | 改动审查：`L42: yagni: 工厂只有一个产品。内联。` |
| **audit** | `/ponytail-audit` | 整仓审计：按能砍多少排名的删除清单 |
| **debt** | `/ponytail-debt` | 把 `ponytail:` 注释收成技术债账本 |
| **gain** | `/ponytail-gain` | 基准数据记分板：更少代码、更低成本、更快 |
| **help** | `/ponytail-help` | 这张卡 |

Codex 用 `@ponytail`、`@ponytail-review`、`@ponytail-help`；Claude Code 和 OpenCode 用上面的斜杠命令。

## 关闭

说「正常模式」或 `stop ponytail`。随时用 `/ponytail` 回来。`/ponytail off` 也行。

## 改默认档

默认是 `full`，每次会话自动生效。想换：

**环境变量**（优先级最高）

```bash
export PONYTAIL_DEFAULT_MODE=ultra
```

**配置文件**（`~/.config/ponytail/config.json`，Windows 是 `%APPDATA%\ponytail\config.json`）

```json
{ "defaultMode": "lite" }
```

填 `"off"` 就是不自动开启，需要时手动 `/ponytail`。

优先级：环境变量 > 配置文件 > `full`。

## 更新

在 Claude Code 里打开 `/plugin` → Marketplaces → 选 ponytail → 开启自动更新。之后每次启动自动拉新版本（提示时执行 `/reload-plugins`）。

手动刷新：`/plugin marketplace update ponytail`，然后 `/reload-plugins`。

`/plugin` 不认？说明 Claude Code 太旧了，更新一下（`npm install -g @anthropic-ai/claude-code@latest` 或 `brew upgrade claude-code`）再重启。其他宿主用自己的更新流程。

## 安装

```bash
git clone https://github.com/chengangrun-ai/gongzi-teaches-code-help.git \
  ~/.workbuddy-ai/skills/gongzi-teaches-code-help
```

没有依赖，不用 pip install。

## 用法

```
/ponytail-help
```

或者直接问「ponytail 怎么用」「有哪些命令」。

## 边界

- 一次性展示，不改模式、不写文件、不留痕迹。
- 想退出：说「正常模式」或 `stop ponytail`。

## 致谢

基于 [Ponytail](https://github.com/DietrichGebert/ponytail)（MIT，作者 DietrichGebert）改写，保留了原作者的版权声明（见 `LICENSE`）。

## License

MIT. See [LICENSE](LICENSE).

Made by [公子](https://github.com/chengangrun-ai).
