# Anya & Miku Codex Pets

非官方同人桌面宠物包：Anya Forger 与 Q 版初音未来 Miku，可安装到 Codex 的本地宠物目录。

## 宠物包

| 角色 | 安装包目录 | 动画预览 |
| --- | --- | --- |
| Anya | [`anya/`](anya/) | [播放预览](preview/anya.gif) |
| Miku | [`miku/`](miku/) | [播放预览](preview/miku.gif) |

| Anya | Miku |
| :---: | :---: |
| ![Anya 动画预览](preview/anya.gif) | ![Miku 动画预览](preview/miku.gif) |

```text
codex-pet/
├── anya/
│   ├── pet.json
│   └── spritesheet.webp
├── miku/
│   ├── pet.json
│   └── spritesheet.webp
└── preview/
    ├── anya.gif
    └── miku.gif
```

`anya/` 和 `miku/` 可以分别安装，保留对应目录中的两个文件即可。

## 本地安装

下载仓库 ZIP 并解压，或运行：

```bash
git clone https://github.com/boltguo/codex-pet.git
cd codex-pet
```

在仓库根目录运行以下命令，同时安装两个角色。已有同名包会更新为本仓库中的版本。

```bash
mkdir -p ~/.codex/pets/anya ~/.codex/pets/miku
cp anya/pet.json anya/spritesheet.webp ~/.codex/pets/anya/
cp miku/pet.json miku/spritesheet.webp ~/.codex/pets/miku/
```

如果只需要一个角色，仅执行对应的 `mkdir` 和 `cp` 命令。使用自定义 `CODEX_HOME` 时，将 `~/.codex` 替换为该目录。

安装后重新打开 Codex 宠物选择器，选择 **Anya** 或 **Miku**；列表未刷新时重启 Codex。

## Disclaimer

This is an unofficial fan-made project and is not affiliated with or endorsed by OpenAI, SPY×FAMILY, Crypton Future Media, or any related rights holder. Anya Forger, Hatsune Miku, and related character rights belong to their respective owners. This repository does not grant a license to the underlying characters or franchises. Review applicable platform rules and rights requirements before public redistribution or commercial use.

