# QMF 当前资源维护目录

## 初始化记录

- 日期：2026-10-04（Asia/Shanghai）。
- 本目录：`D:/Quenching/QM/Latest`。
- 初始来源：`D:/Quenching/QM/3.5/QMF3.5`。原目录保留，作为本次复制来源。
- 资源仓库：`https://github.com/UIZorrot/Quenching-Assets.git`。
- 工作分支：`main`。
- 旧远程起点：`8cc45d7a39040a082f48345caf365d486dd5b5b4`（2024-11-25）。按维护者要求，`main` 重新建立以当前 QMF 资源为起点的历史，不继承旧 2.x 提交。
- 复制范围：全部 23 个资源目录及根目录 `Mac.txt`、`reg.reg`；共 9,025 个来源文件，7,637,721,693 字节。
- 根目录成品 ZIP、构建及上传日志没有复制。历史仓库的 `LICENSE` 和 `README.md` 单独保留。
- 原 `_patch/keep.que` 和官方 3.5 快照原样复制；本次初始化不产生新的发布版本。

## 日常维护

这里保存可编辑的完整 MOD 资源树。相对目录直接对应游戏分支中的资源路径；不要在这里创建 `_retail_` 或 `_ptr_` 外层。

为避免 GitHub 单次推送 2 GiB 的限制，初始化资源按批次提交到 `main`；最终提交包含完整资源树。Git 中直接保存资源文件，未启用 Git LFS。二进制资源保留原字节，只有维护文档采用 LF 换行。

客户端资源源目录是 `D:/Quenching/QM/MOD/QuenChing-Electron-Client/assets/quenching`。按资源职责把确认后的客户端资源复制到本目录，不移动源 assets，不把整个客户端 assets 目录直接覆盖进来。

2026-10-04 初始化时，下列着色器按文件路径及 SHA-256 对比，均与客户端源一致：

| 本目录目标 | 客户端着色器来源 |
| --- | --- |
| `shaders/vs` | `shaders/shaders-300-hd/vs` |
| `shaders/ps` | `shaders/shaders-300-hd/ps/standard` |
| `_manual/_20/shaders` | `shaders/shaders203` |
| `_manual/_30/shaders-hd` | `shaders/shaders-300-hd` |
| `_manual/_30/shaders-de` | `shaders/shaders-300-de` |

PTR 的独立着色器留在客户端 `shaders-ptr-hd`、`shaders-ptr-de` 中，不能混入完整包默认 HD 3.0 布局。初始化没有引入旧仓库的 `scripts` 目录。

## 发布前

本目录是维护树，不等于已发布的新资源包。资源变更后，需要确定新的资源版本和 sequence，再重建 `_patch` 中的官方文件清单；不要把原 3.5 清单当作变更后的清单。

打包输出放到独立产物目录，排除 `.git`、本维护说明和生成日志。A/B 包必须是两份可独立解压的普通 ZIP。制作、上传与更新线上清单时，遵循客户端仓库的 `.agents/skills/quenching-release/SKILL.md`。
