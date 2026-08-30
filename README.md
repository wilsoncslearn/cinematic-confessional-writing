

# 通过这个skill，我们也能写出孙哥这种文笔的文章

一个把“瓜”拆成写作技法的 Codex Skill。

最近，孙宇晨与景甜相关的争议文本在网上引发了大量讨论。有人关注其中的情节，有人讨论真假，也有人注意到：这篇文章的行文、节奏和细节组织，确实很会制造阅读推动力。

这个项目关心的不是替事件下结论，而是把文本里的表达方法拆出来，变成任何人都可以使用的写作工具。

> 重要说明：本项目只分析公开流传文本的叙事技法，不对涉及真人的关系、金额、私生活或争议指控作事实认定。使用 Skill 时，未经核实的内容必须保留归因和不确定性。

## 能做什么

`cinematic-confessional-writing` 会帮助 Agent：

* 梳理事件时间线和叙事主线；
* 从材料中寻找适合开篇的具体冲突；
* 用动作、环境、物件和对白代替直接情绪表达；
* 使用核心物件、重复意象和前后呼应增强叙事；
* 控制信息释放和第一人称叙事节奏；
* 在真实事件中区分事实、陈述和未经核实的信息；
* 在虚构故事中补充符合人物设定和前后连续性的细节。

核心原则是：

> 少解释情绪，多让动作、细节和留白承担情绪。

---

## 安装

### Codex

```bash
git clone https://github.com/5ysy/cinematic-confessional-writing.git \
  ~/.agents/skills/cinematic-confessional-writing
```

然后重新启动 Codex。

调用：

```text
$cinematic-confessional-writing

请把下面的材料改写成克制、电影感、细节驱动的中文第一人称叙事。
```

---

### Claude Code

```bash
git clone https://github.com/5ysy/cinematic-confessional-writing.git \
  ~/.claude/skills/cinematic-confessional-writing
```

然后重新启动 Claude Code。

调用：

```text
/cinematic-confessional-writing

请把下面的材料改写成克制、电影感、细节驱动的中文第一人称叙事。
```

也可以直接描述写作需求，让 Agent 根据 Skill 的 `description` 自动判断是否使用。

---

## 使用示例

输入：

```text
人物：我和一位合伙人

时间线：
合作三年；
融资后我逐渐被移出核心决策；
最后一次见面是在便利店。

关键物件：
办公室钥匙

希望的结尾：
回到“没有拿走钥匙”这个动作。
```

然后调用：

```text
$cinematic-confessional-writing
```

或：

```text
/cinematic-confessional-writing
```

Skill 会先整理时间线、人物关系、核心冲突和关键意象，再完成正文。

---

## 写作特点

这个 Skill 重点使用以下叙事方法：

* 具体数字与尺度反差；
* 场景和物件写人；
* 克制的第一人称；
* 短对白；
* 情绪留白；
* 核心物件反复出现；
* 重复意象的意义变化；
* 首尾呼应；
* 秩序建立 → 秩序破坏 → 回望。

它不会为了制造“电影感”而随意补充不存在的酒店、品牌、航班、转账、天气、对白或心理活动。

---

## 真实事件与虚构事件

对于真实人物或真实事件，Skill 会尽量区分：

* 已知事实；
* 当事人陈述；
* 第三方说法；
* 未经核实的信息；
* 准确引语；
* 普通转述。

文学化表达不能代替事实核查。

对于明确的虚构作品，可以在既有设定内补充场景、动作、对白和细节，但需要保持人物、时间线和故事连续性。

---

## 文件结构

```text
cinematic-confessional-writing/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── style-guide.md
    └── rewrite-workflow.md
```

* `SKILL.md`：Skill 入口、触发条件和核心规则
* `style-guide.md`：叙事风格与写作方法
* `rewrite-workflow.md`：从原始材料到最终文本的改写流程
* `openai.yaml`：OpenAI / Codex 相关元数据

---

## 更新

如果已经安装：

```bash
cd ~/.agents/skills/cinematic-confessional-writing
git pull
```

Claude Code：

```bash
cd ~/.claude/skills/cinematic-confessional-writing
git pull
```

---

## License

本项目基于 [MIT License](LICENSE) 开源。

你可以自由使用、复制、修改、合并、发布、分发、再授权或销售本项目的副本，包括用于商业用途，但需要保留原始版权声明和许可证声明。
