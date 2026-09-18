# AMS-PPT

Advanced Materials Science 课程资料，包含课件、作业、课堂录音和对应的 TXT 转写文本。录音及转写文本位于各课程的 `Recording/日期/` 目录。

GitHub 仓库：[EchoJonhson/AMS-PPT](https://github.com/EchoJonhson/AMS-PPT)。原 [GitCode 仓库](https://gitcode.com/GPR/AMS-PPT) 保留此前版本；两处仓库不会自动同步。GitHub 版本包含 4 份原始 WAV，以及 9 月 8 日录音的无损 FLAC 副本。

## 音频文件限制与保存方式

GitHub 普通 Git 文件限制见[官方说明](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github)。此前 GitCode 的上传情况记录于 **2026 年 9 月 16 日**；GitHub 版本于 **2026 年 9 月 18 日**补充原始 WAV 并更新下载说明。

- **普通 Git 上传的单文件上限为 100 MiB，即 104,857,600 字节。** 超过这个大小的原始 WAV 会被本仓库服务器拒绝；拆成多次提交也不会改变单文件限制。100 MiB 约等于十进制的 104.9 MB。
- **Git LFS 用于保存较大的 WAV。** Git 仓库中记录的是小型指针文件，实际音频存放在 LFS 服务中。下载时需要取得音频实体，只有指针无法播放。本仓库已配置 `*.wav` 使用 LFS；LFS 仍受平台自身的存储、流量及网络条件约束。
- **9 月 8 日录音同时提供原始 WAV 和无损 FLAC。** 原 WAV 为 192,291,868 字节，在 GitHub 通过 LFS 保存；无损压缩后的 FLAC 为 100,481,063 字节（约 95.8 MiB），通过普通 Git 保存。完整解码后的音频样本与原 WAV 完全一致，保留 16,000 Hz、16 位、单声道。
- **全部 4 份原始 WAV 均使用 LFS。** 此前 GitCode 上传 9 月 8 日 WAV 多次中断，因此旧版仅提供同名 FLAC；GitHub 版本已取消该 WAV 的忽略规则。MP3、FLAC 和 TXT 通过普通 Git 保存。

FLAC 是可以直接播放的无损音频格式，无需像 ZIP 一样解压。它改变文件封装和存储体积，不丢失音频样本。详见 [FLAC 官方介绍](https://xiph.org/flac/)和 [9 月 8 日音频说明](<AMSC5720_Advanced Materials Synthesis/Recording/9.8/音频说明.md>)。

## 录音与转写文本索引

表中的大小为完整音频实体的大小，单位为 MiB；点击链接进入相应文件页面。

| 课程 | 日期 | 音频文件 | 大小 | 保存方式 | 转写文本 |
| --- | --- | --- | ---: | --- | --- |
| AMSC5710 材料表征 | 9 月 7 日 | [1788755850655.wav](<AMSC5710_Advanced Materials Characterization/Recording/9.7/1788755850655.wav>) | 231.4 MiB | Git LFS | [TXT](<AMSC5710_Advanced Materials Characterization/Recording/9.7/基础同传-1.txt>) |
| AMSC5710 材料表征 | 9 月 14 日 | [1789360274975.wav](<AMSC5710_Advanced Materials Characterization/Recording/9.14/1789360274975.wav>) | 218.3 MiB | Git LFS | [TXT](<AMSC5710_Advanced Materials Characterization/Recording/9.14/基础同传-1(3).txt>) |
| AMSC5720 材料合成 | 9 月 8 日 | [1788863889187.flac](<AMSC5720_Advanced Materials Synthesis/Recording/9.8/1788863889187.flac>) | 95.8 MiB | 普通 Git；无损 FLAC | [TXT](<AMSC5720_Advanced Materials Synthesis/Recording/9.8/基础同传-1(1).txt>) |
| AMSC5720 材料合成 | 9 月 8 日 | [1788863889187.wav](<AMSC5720_Advanced Materials Synthesis/Recording/9.8/1788863889187.wav>) | 183.4 MiB | Git LFS；原始 WAV | [TXT](<AMSC5720_Advanced Materials Synthesis/Recording/9.8/基础同传-1(1).txt>) |
| AMSC5720 材料合成 | 9 月 16 日 | [9.16.mp3](<AMSC5720_Advanced Materials Synthesis/Recording/9.16/9.16.mp3>) | 16.8 MiB | 普通 Git | [TXT](<AMSC5720_Advanced Materials Synthesis/Recording/9.16/9.16.txt>) |
| AMSC5730 前沿材料 | 9 月 10 日 | [1789037676212.wav](<AMSC5730_Frontiers in Advanced Materials/Recording/9.10/1789037676212.wav>) | 180.4 MiB | Git LFS | [TXT](<AMSC5730_Frontiers in Advanced Materials/Recording/9.10/基础同传-1(2).txt>) |
| AMSC5730 前沿材料 | 9 月 17 日 | [录音_2026-09-17T14-53-45.mp3](<AMSC5730_Frontiers in Advanced Materials/Recording/9.17/录音_2026-09-17T14-53-45.mp3>) | 37.2 MiB | 普通 Git | [当日两份 TXT](<AMSC5730_Frontiers in Advanced Materials/Recording/9.17/>) |
| AMSC5730 前沿材料 | 9 月 17 日 | [录音_2026-09-17T14-54-06.mp3](<AMSC5730_Frontiers in Advanced Materials/Recording/9.17/录音_2026-09-17T14-54-06.mp3>) | 23.1 MiB | 普通 Git | [当日两份 TXT](<AMSC5730_Frontiers in Advanced Materials/Recording/9.17/>) |

## 如何下载

### 下载全部资料和完整录音

先安装 [Git](https://git-scm.com/downloads) 和 [Git LFS](https://git-lfs.com/)。安装完成后打开终端，依次执行以下命令；Windows PowerShell、macOS 和 Linux 均可使用：

```sh
git lfs version
git lfs install
git clone https://github.com/EchoJonhson/AMS-PPT.git
cd AMS-PPT
git lfs pull
```

`git lfs version` 用于检查 LFS 程序是否已安装；`git lfs install` 配置 Git 所需的过滤器和钩子，本身不负责下载安装程序。正常情况下，克隆时会自动下载 LFS 音频；最后的 `git lfs pull` 用于补齐当前版本需要的 LFS 文件。

下载结束后，在上表对应的 `Recording` 子目录中打开音频。若平台提示登录，请使用具有仓库访问权限的 GitHub 账号完成认证。

### 已经克隆过仓库，补齐录音或更新资料

在本地 `AMS-PPT` 仓库目录内执行：

```sh
git pull --ff-only
git lfs pull
```

如果只需补拉某一份 LFS 录音，可指定文件路径，例如 9 月 7 日录音：

```sh
git lfs pull --include="AMSC5710_Advanced Materials Characterization/Recording/9.7/1788755850655.wav" --exclude=""
```

这里的 `--include` 只筛选 LFS 文件。FLAC、MP3 和 TXT 是普通 Git 文件，随 `git clone` 或 `git pull` 获取。

### 通过网页下载

只需要某份录音或 TXT 时，可以先点击上表链接，在文件页面使用平台提供的文件下载入口。对于 WAV，需确认下载的是完整的 LFS 音频实体；如果页面只展示指针或未提供音频实体下载，请使用上面的 Git LFS 方法。

**不要仅凭“下载 ZIP”完成，就认定所有 WAV 已下载。** 仓库压缩包是否包含 LFS 实体取决于平台的实现与设置。下载后请检查 WAV 大小：本仓库的 4 份 WAV 均有约 180–231 MiB。若文件仅约 130 字节，或用文本编辑器打开后以这一行开头，取得的是 LFS 指针：

```text
version https://git-lfs.github.com/spec/v1
```

指针不能通过修改扩展名变成音频。已有 Git 克隆目录时，进入该目录执行 `git lfs pull`；只有 ZIP 解压目录时，请按“下载全部资料和完整录音”的步骤重新克隆。

## 下载后如何使用

### 收听录音和查看转写

1. 将下载完成的 `.wav`、`.flac` 或 `.mp3` 文件用支持相应格式的音频播放器打开。若系统默认播放器不支持 FLAC，可使用 [VLC](https://www.videolan.org/vlc/) 等支持 FLAC 的播放器。
2. 同时打开同一日期目录下的 TXT，配合录音查阅内容。TXT 可用记事本、VS Code 等文本编辑器查看；如果中文乱码，请尝试按 UTF-8 编码打开。
3. 网页没有音频预览不等于文件损坏，下载到本地后再播放。FLAC 可以直接收听，无需先转成 WAV。

### 软件只接受 WAV 时，将 9 月 8 日 FLAC 解码为 WAV

先安装 [FFmpeg](https://ffmpeg.org/download.html)。从本地仓库根目录进入 9 月 8 日录音目录，再执行：

```sh
cd "AMSC5720_Advanced Materials Synthesis/Recording/9.8"
ffmpeg -n -i "1788863889187.flac" -c:a pcm_s16le "1788863889187-decoded.wav"
```

生成的 `1788863889187-decoded.wav` 可供只接受 WAV 的播放器、转写工具或音频分析软件使用。此命令将本录音无损解码为 16 位 PCM，保留原采样率和声道数，不覆盖原有文件。

解码后的 WAV 会恢复到约 192 MB，仍超过本仓库普通 Git 的 100 MiB 限制。转换得到的 WAV 与原始 WAV 可以具有不同的文件头及文件哈希；音频样本一致才是无损校验的依据。请勿仅将 `.flac` 扩展名改成 `.wav`，也无需为了收听而另转有损 MP3。

## 下载失败或无法播放时

| 现象 | 处理方法 |
| --- | --- |
| 提示 `git: 'lfs' is not a git command` | 安装 Git LFS，重新打开终端，执行 `git lfs version` 检查。 |
| WAV 文件很小，内容是三行指针文本 | 在 Git 克隆目录内执行 `git lfs pull`，下载音频实体。 |
| LFS 下载中断、连接超时 | 网络恢复后重试 `git lfs pull`；也可用上面的 `--include` 命令逐份下载。 |
| FLAC 无法被默认播放器打开 | 换用支持 FLAC 的播放器，或按上述命令解码为 WAV。 |
| 找不到 9 月 8 日的原始 WAV | 从本页列出的 GitHub 仓库更新并执行 `git lfs pull`；旧 GitCode 版本仅提供同名无损 FLAC。 |
| 网页显示大文件无法预览 | 使用文件下载入口或 Git／Git LFS 下载，再在本地打开。 |

9 月 8 日 FLAC 的 SHA-256 为：

```text
e55407762770ec52e605c29295c61dc4c8021d1c0fc68e57451e3a8da6965a29
```

如需检查下载是否完整，可在仓库根目录使用 Windows PowerShell 执行：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath "AMSC5720_Advanced Materials Synthesis/Recording/9.8/1788863889187.flac"
```

输出的哈希应与上面一致，字母大小写不影响比较。该 FLAC 及先前的 3 份 LFS WAV 已在 2026 年 9 月 16 日完成 GitCode 远端完整下载与 SHA-256 校验；此记录不代表后续平台的校验结果。

参考：[Git LFS 官方说明](https://git-lfs.com/)、[git lfs pull 官方文档](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-pull.adoc)、[FLAC 格式说明](https://xiph.org/flac/)、[FFmpeg 命令文档](https://ffmpeg.org/ffmpeg.html)。
