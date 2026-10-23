# 公子教代码做事 · 速查卡

【速查卡】一次性列出 ponytail 全部模式、技能和命令的一句话说明， 以及如何切换强度、如何关闭、如何更新。忘了怎么用就说 ponytail help。 触发词：/ponytail-help、ponytail 怎么用、ponytail 有哪些命令。

## 📺 看看效果

![ponytail-help](screenshots/hero.png)

> 把 `screenshots/hero.png` 换成真实效果图（建议 1200px 宽、不超过 400KB）

## What This Does

【速查卡】一次性列出 ponytail 全部模式、技能和命令的一句话说明， 以及如何切换强度、如何关闭、如何更新。忘了怎么用就说 ponytail help。 触发词：/ponytail-help、ponytail 怎么用、ponytail 有哪些命令。

### Key Features

- Levels
- Skills
- Deactivate
- Configure Default Mode
- Update
- More

## Installation

### WorkBuddy

```bash
git clone https://github.com/<you>/ponytail-help.git ~/.workbuddy-ai/skills/ponytail-help
pip install -r ~/.workbuddy-ai/skills/ponytail-help/requirements.txt
```

### Claude Code / 其他 Agent

```bash
mkdir -p ~/.claude/skills/ponytail-help
cp -R SKILL.md README.md requirements.txt scripts references \
      ~/.claude/skills/ponytail-help/
```

把仓库链接丢给 agent，它会按 `SKILL.md` 加载所需文件。

## Usage

触发词：**/ponytail-help、ponytail 怎么用、ponytail 有哪些命令**

```bash
export PONYTAIL_DEFAULT_MODE=ultra
```

## Architecture

| 文件 | 作用 |
|---|---|
| `SKILL.md` | 触发条件与流程 |

## Requirements

- Python 3.9+
- `pip install -r requirements.txt`

## Credits

基于 [Ponytail](https://github.com/DietrichGebert/ponytail)（MIT，作者 DietrichGebert）改写 · 中文版维护 [@chengangrun-ai](https://github.com/chengangrun-ai)

Created by 公子 · [@你的GitHub](https://github.com/).

## License

MIT — Use it, modify it, share it.
