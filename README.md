# Anya & Miku Codex Pets

非官方同人桌面宠物包：Anya Forger 与 Q 版初音未来 Miku，可安装到 Codex 的本地宠物目录。

每个角色只维护一个 **v2** 包：透明精灵图为 `1536 × 2288`，包含 9 组标准动画和 16 个注视方向，共 73 帧。Anya 保留原 v2 的全部 73 个有效帧，清理了未使用格中的遗留静止帧，安装包目录已改为 `anya/`。旧 v1 停止分发，历史版本仍可通过 Git 历史查看。

## 宠物包

| 角色 | 安装包目录 | 动画预览 | 完整精灵图预览 |
| --- | --- | --- | --- |
| Anya | [`anya/`](anya/) | [播放预览](preview/anya.gif) | [全部 73 帧](preview/anya-contact-sheet.png) |
| Miku | [`miku/`](miku/) | [播放预览](preview/miku.gif) · [16 个注视方向](preview/miku-look.gif) | [全部 73 帧](preview/miku-contact-sheet.png) |

| Anya | Miku |
| :---: | :---: |
| ![Anya 动画预览](preview/anya.gif) | ![Miku 动画预览](preview/miku.gif) |

```text
anya-codex-pet/
├── anya/
│   ├── pet.json
│   └── spritesheet.webp
├── miku/
│   ├── pet.json
│   └── spritesheet.webp
├── preview/
└── qa/
    ├── anya-validation.json
    └── miku-validation.json
```

`anya/` 和 `miku/` 都是独立的完整安装包，保留目录中的两个文件即可使用。Miku 的 WebP 由已校验的最终 PNG 无损转换，解码后的 RGBA 像素完全一致。

## 本地安装

下载仓库 ZIP 并解压，或运行：

```bash
git clone https://github.com/boltguo/anya-codex-pet.git
cd anya-codex-pet
```

在仓库根目录运行以下命令，同时安装两个角色。已有同名包会更新为本仓库中的版本。

```bash
mkdir -p ~/.codex/pets/anya ~/.codex/pets/miku
cp anya/pet.json anya/spritesheet.webp ~/.codex/pets/anya/
cp miku/pet.json miku/spritesheet.webp ~/.codex/pets/miku/
```

如果只需要一个角色，仅执行对应的 `mkdir` 和 `cp` 命令。使用自定义 `CODEX_HOME` 时，将 `~/.codex` 替换为该目录。

安装后重新打开 Codex 宠物选择器，选择 **Anya** 或 **Miku**；列表未刷新时重启 Codex。

## 校验

两份最终 WebP 均按 v2 图集契约重新校验，结果见 [`qa/`](qa/)：

- `pet.json` 的 `spriteVersionNumber` 为 `2`，图片路径指向同目录的 `spritesheet.webp`。
- 图集为 `8 × 11` 格，每格 `192 × 208` 像素。
- 73 个必需帧均非空，15 个未使用格完全透明。
- 编码、尺寸、透明度和色键残留检查通过。
- 报告记录最终图片的 SHA-256，便于核对下载的文件。

## Disclaimer

This is an unofficial fan-made project and is not affiliated with or endorsed by OpenAI, SPY×FAMILY, Crypton Future Media, or any related rights holder. Anya Forger, Hatsune Miku, and related character rights belong to their respective owners. This repository does not grant a license to the underlying characters or franchises. Review applicable platform rules and rights requirements before public redistribution or commercial use.

