# Precision Fashion Lookbook Collage

一个可复用的 Codex skill：把用户提供的白底服装模特图转换为 9:16 极简高级时装 Lookbook 拼贴图，同时严格保留人物、服装、配色和固定版式比例。

## 安装

在 Codex 中调用 `$skill-installer`，并要求它从以下 GitHub 仓库安装：

```text
https://github.com/madwitchcloud/precision-fashion-lookbook-collage
```

也可以手动克隆到用户级 skill 目录：

```powershell
New-Item -ItemType Directory -Force "$HOME\.agents\skills"
git clone https://github.com/madwitchcloud/precision-fashion-lookbook-collage "$HOME\.agents\skills\precision-fashion-lookbook-collage"
```

若 skill 没有立即出现在列表中，请重启 Codex。

## 调用

上传一张白底服装模特图，然后输入：

```text
使用 $precision-fashion-lookbook-collage 制作 9:16 Lookbook 拼贴图。
```

运行环境需要具备能够引用输入图片的图像生成或编辑能力。

## 仓库结构

```text
precision-fashion-lookbook-collage/
├── README.md
├── SKILL.md
└── agents/
    └── openai.yaml
```

`SKILL.md` 是技能入口；`agents/openai.yaml` 提供 Codex 界面显示信息和默认调用提示。
