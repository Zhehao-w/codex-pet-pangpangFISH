# 蓝色大肥鱼 Codex Pets

> 我是吃白饭的蓝色大肥鱼！

女仆装与冬装两只大肥鱼，可以分别安装，也可以同时保留。

| 目录 | 桌宠名称 | 设定 |
|---|---|---|
| `deepseek/` | DeepSeek | 女仆装；捧碗待机、叉腰挺胸、奔跑、吃白饭、趴睡，以及任务完成时侧躺托腮拍肚子 |
| `deepseek-winter/` | 冬装蓝色大肥鱼 | 鲸鱼毛绒帽、蓝白围巾和冬衣；空手待机、叉腰挺胸、端碗奔跑、吃白饭、冬装趴睡，以及任务完成时侧躺托腮拍肚子 |

两只都包含 16 个视线方向，会跟着鼠标看过去。

## v1.1.2 更新

下载 [v1.1.2](https://github.com/Zhehao-w/codex-pet-pangpangFISH/releases/tag/v1.1.2)，完整说明见 [发布说明](./RELEASE_NOTES.md)。

- **女仆装**：统一各动作的蓝色调，修正 waiting 和挺胸 hover 偏灰；除吃饭和趴睡外，头身比对齐吃饭动画，待机饭碗也统一为吃饭同款。
- **奔跑修复**：去除女仆装部分帧的多余手和绿色杂物，保留原来的八帧动作、手脚姿势与顺序。
- **冬装**：统一各动作配色，为趴睡增加随呼吸变化的鼻尖睡泡，保留帽子鲸鱼勋章。
- **任务完成动画**：两个版本都改为吃饱后侧躺托腮、轻拍肚子的动作，配合自然睁眼、小幅微笑和短暂眨眼；分别保留各自的身材、服装和头发。冬装修正大衣侧边和托腮袖子的形状、角度，缩小帽尾，并让身体尾巴轻摆。

### 任务完成动画只闪一下？

任务完成动画位于 `review` 状态，对应完成后等待查看。聊天被标记为已读后，应用可能立即切回待机，中断尚未播完的动作；一直停留在当前聊天时尤其容易出现。可以切到其他聊天，让任务在后台完成后观察。

播放时长和状态切换由应用控制，宠物图片及 `pet.json` 无法强制延长停留时间。预览 GIF 的循环时长也不会作为播放设置写入宠物。

## 鱼图预览

### 女仆装 · DeepSeek

<p align="center">
  <img src="./deepseek/spritesheet.webp" alt="女仆装蓝色大肥鱼 V2 鱼图" width="512">
</p>

### 冬装 · 冬装蓝色大肥鱼

<p align="center">
  <img src="./deepseek-winter/spritesheet.webp" alt="冬装蓝色大肥鱼 V2 鱼图" width="512">
</p>

## 安装

从 [最新 Release](https://github.com/Zhehao-w/codex-pet-pangpangFISH/releases/latest) 下载需要的安装包：

- [deepseek.zip](https://github.com/Zhehao-w/codex-pet-pangpangFISH/releases/latest/download/deepseek.zip)：女仆装。
- [deepseek-winter.zip](https://github.com/Zhehao-w/codex-pet-pangpangFISH/releases/latest/download/deepseek-winter.zip)：冬装。
- [SHA256SUMS](https://github.com/Zhehao-w/codex-pet-pangpangFISH/releases/latest/download/SHA256SUMS)：两个 ZIP 的 SHA256 校验值。

将 ZIP 内的宠物文件夹解压到 `~/.codex/pets/`。也可以克隆本仓库，将 `deepseek/` 和 `deepseek-winter/` 文件夹复制过去。

```text
~/.codex/pets/
├── deepseek/
│   ├── pet.json
│   └── spritesheet.webp
└── deepseek-winter/
    ├── pet.json
    └── spritesheet.webp
```

完全退出并重新打开 Codex，在宠物选择器中选择 **DeepSeek** 或 **冬装蓝色大肥鱼**。更新同 ID 的旧版本时，替换对应目录中的两个文件后重启 Codex。

下载两个 ZIP 和 `SHA256SUMS` 后，可在下载目录执行：

```bash
shasum -a 256 -c SHA256SUMS
```

## 仓库结构与文件

```text
.
├── README.md
├── RELEASE_NOTES.md
├── deepseek/
│   ├── pet.json
│   └── spritesheet.webp
└── deepseek-winter/
    ├── pet.json
    └── spritesheet.webp
```

每个宠物目录只包含两个文件：`pet.json` 保存名称、描述和 V2 配置；`spritesheet.webp` 是包含全部动画帧和观察方向的透明鱼图。

两只均采用 Codex Hatch Pet V2：1536 × 2288 像素、8 列 × 11 行、单格 192 × 208 像素，`spriteVersionNumber: 2`。

## 同人作品声明

本项目是非官方、非商业的同人桌宠，仅用于个人桌面定制与技术学习。本项目与 DeepSeek、OpenAI 或 Codex 无隶属或授权关系，名称、标识及相关形象的权利归各自权利人所有。
