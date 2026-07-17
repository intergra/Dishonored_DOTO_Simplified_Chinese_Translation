<div align="center">

# 《耻辱：界外魔之死》简体中文翻译

### Simplified Chinese Translation for Dishonored: Death of the Outsider

**高质量简体中文本地化，覆盖菜单、界面、任务、书信、日志、对白字幕与中文字体。**

</div>

## Download / 下载

> [!IMPORTANT]
> 当前尚未创建正式 Release，也没有可供玩家安装的公开 ZIP。请不要把 GitHub 自动生成的
> `Source code (zip)` 或 `Source code (tar.gz)` 当作 MOD 安装包。

`v1.0` 的全文本审校、全量测试、完整构建、独立回读与首次安装沙箱验证已经完成。
当前尚未创建正式 Release；正式安装包将发布到本仓库的
[Releases](https://github.com/intergra/Dishonored_DOTO_Simplified_Chinese_Translation/releases) 页面，
文件名固定为：

```text
Dishonored_DOTO_Simplified_Chinese.zip
```

## Overview / 简介

本 MOD 为《Dishonored: Death of the Outsider / 耻辱：界外魔之死》制作完整简体中文
翻译，目标覆盖主菜单、HUD、任务目标、教程、技能与物品说明、书信、日志、环境文本、
剧情对白和游戏内字幕。

翻译以**官方英文原文为最高依据**，官方繁体中文仅作为参考。项目不是把繁体机械转换
为简体，而是结合剧情语境、人物身份、组织性质、时代气质和简体中文的自然表达与阅读习惯，
逐条处理误译、漏译、港台用语、术语不统一和不自然表达。

项目已完成全部主文本和对白的逐条审校。共有译文在复用后也与 DOTO 专属文本一同按
英文原文、剧情语境和游戏内用法复核：

- 主文本 8,261 条。
- 对白 5,431 个可编辑字幕文本槽。

全部主文本和对白都以稳定身份单独保存，不受官方繁体字数和语序限制。译者可以任意
调整单条译文的字数、语序和句式，而不必重建整份对白声明。

本 MOD 同时重建游戏的中文字体资源。全部可绘制 CJK 槽统一使用 **Noto Sans SC /
思源黑体简体 600** 字重，并校正字面大小、笔画轮廓和垂直基线，避免简繁字形混排、
缺字、碎笔、灰影和大量 `~` 的问题。

当前技术方案由两部分组成：

- **Void 静态资源层：** 安装主语言表、中文字体和 17 个确有必要直接替换的对白资源，
  保证菜单、界面、字体与安全底座正常加载。
- **运行时完整对白层：** 从 Steam 启动游戏时加载逐条译文，在保留游戏原版地图、角色、
  存档、检查点、音频和语音声明生命周期的前提下修改既有字幕文本槽。

## Important Notes / 重要说明

1. 当前技术基线只支持经项目验证的 **Windows x64 Steam 版
   `Dishonored_DO.exe 1.145.0.0`**。
2. 安装静态资源需要前置工具
   [Void Installer](https://www.nexusmods.com/dishonored2/mods/31)（作者：FCH823）。
   请从该页面单独下载并解压；本 MOD 不包含 Void Installer。
3. 完整对白翻译需要设置一次 **Steam 启动选项**。只安装 Void 静态资源而不设置启动
   选项，无法获得运行时逐条对白译文。
4. 请在 Steam 中把游戏语言设置为 **中文（繁体）**。本 MOD 使用游戏原有中文槽位，
   不会新增独立的“简体中文”语言选项。
5. 解压后的 MOD 文件夹必须长期保留。Steam 启动选项会从该目录加载运行时组件。
6. 玩家始终从 Steam 的“开始游戏”按钮启动，不需要也不建议到游戏目录双击
   `Dishonored_DO.exe`。
7. 不要叠加安装旧版、测试包或其他修改中文文本、中文字体和 localized speech 的 MOD。
8. 本 MOD 不包含游戏本体。使用前必须拥有并安装正版游戏。

## Main Features / 主要内容

### 1. 简体中文菜单、界面与主文本

项目审计官方英文和官方中文主语言表的 8,259 个文本键，并补入 2 条官方英文存在、但
官方繁体缺失的可用文本，最终主语言表共 8,261 条。

覆盖内容包括但不限于：

- 主菜单、暂停菜单、保存与载入界面
- HUD、互动提示、警告和系统消息
- 任务目标、任务日志和剧情摘要
- 教程、能力、技能与升级说明
- 物品、武器、护符和骨符说明
- 书信、日志、公告、报纸和世界观文本
- 视频、画质、声音、操作和辅助设置

图形质量等级使用“非常高”和“极致”，避免同一菜单中出现两个含义不清的“极高”。

### 2. 可逐条精修的游戏内对白与字幕

项目从 DOTO 官方资源中提取并建立稳定目录：

- 922 个唯一 localized speech 资源
- 5,829 个语音行
- 5,430 个非空文本集合
- 5,431 个可编辑字幕文本槽

运行时目录为每个字幕槽保存独立译文，支持自由调整语序、增删字和重写句子。声明名称、
行数、顺序、角色、音频关联、分支结构和所有非文本字段保持不变。

翻译 DLL 不重建整份语音声明，也不接管地图、存档、死亡回档、音频或事件系统。它只在
引擎完成原版声明加载后调用引擎自身的字符串赋值逻辑，修改当前进程内既有的字幕槽。

### 3. 完整简体中文字形支持

中文字体采用 **Noto Sans SC / 思源黑体简体 600**，统一重绘 3,938 个可绘制 CJK
字形槽：

- 保持原版字体 4,217 个字符和原版码点表不变
- 覆盖独立中文字体及实际 UI 加载使用的 17 个字体目标
- 统一中文字面大小、笔画粗细和垂直基线
- 修复复杂汉字交叠轮廓造成的碎笔、缺口和灰影
- 主语言表、静态对白和运行时完整译文统一参与缺字审计
- 编码缺字和视觉简体回译错误均为 0

字体依据 SIL Open Font License 1.1 使用，许可证文件随正式包提供。

### 4. 翻译原则

1. 英文原文是判断含义的最高依据。
2. 结合世界观、剧情流程、人物关系、身份和说话场景。
3. 使用符合简体中文语境和游戏行业约定的表达。
4. 人物、地点、组织、能力、技能和物品译名按上下文保持一致。
5. 任务目标、教程、技能和 UI 优先保证清晰，不为文采牺牲玩法信息。
6. 对白、书信和日志保持克制，不添加原文没有的梗、情绪或剧情信息。
7. 保留变量、占位符、标签、转义、换行语义和所有技术控制结构。

### 5. 安全构建与验证

- 从官方资源只读提取并重新构建，不在旧 MOD 成品上叠加修改。
- 构建时使用一次性原版源镜像，真实游戏目录写入为 0。
- 逐项验证语言表、字体、对白目录、Void 索引和压缩元数据。
- 使用原始 `master.index` 执行首次安装沙箱测试。
- 回读全部 35 个 Void 补丁目标。
- 启动器验证游戏 EXE 的 SHA-256、PE/PDB 身份和关键机器码，版本不符时拒绝加载。
- 发布目录与确定性 ZIP 逐文件验证大小和 SHA-256 一致。

## Package Contents / 文件内容

`v1.0` 完整包固定包含 11 个文件：

```text
Dishonored_DOTO_Simplified_Chinese/
├─ ModInfo.xml
├─ package-manifest.json
├─ licenses/
│  ├─ NotoSansSC-COPYRIGHT.txt
│  └─ OFL.txt
├─ Resources/
│  ├─ game1.voidIndex
│  ├─ game1.voidRessources
│  ├─ game2.voidIndex
│  └─ game2.voidRessources
└─ Runtime/
   ├─ DOTORuntimeLauncher.exe
   ├─ DOTORuntimeTranslation.dll
   └─ speech-translations.bin
```

正式包不包含游戏本体、Void Installer、开发检查脚本、研究探针、调试 DLL、构建脚本、
机器路径配置或运行日志。

## Recommended Environment / 推荐环境

- 操作系统：Windows x64
- 游戏版本：Steam 版 Death of the Outsider，`Dishonored_DO.exe 1.145.0.0`
- 静态资源安装工具：[Void Installer](https://www.nexusmods.com/dishonored2/mods/31)
- Steam 游戏语言：中文（繁体）
- 推荐安装前状态：未安装其他中文文本、字幕或中文字体 MOD

玩家端**不需要**安装 Python、.NET SDK、CMake、Visual Studio 或额外 VC++ 运行库。
正式启动器和 DLL 使用静态 C/C++ 运行库构建。

## Prerequisite Tool / 前置工具

安装本 MOD 的静态资源必须使用
[Void Installer](https://www.nexusmods.com/dishonored2/mods/31)。请在其 Nexus Mods
页面的 **Files** 栏下载并解压，然后运行 `VoidInstaller.exe`。Void Installer 由
FCH823 制作，不包含在本 MOD 正式包中，也不属于本项目。

Void Installer 当前需要 **Microsoft .NET 6 Desktop Runtime x64**。如果
`VoidInstaller.exe` 可以正常打开，无需重复安装；如果系统提示缺少 .NET 运行环境，
请从 [Microsoft 官方 .NET 6 下载页面](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
安装 Windows x64 的 **.NET Desktop Runtime 6.0**。该运行环境仅供 Void Installer
使用，本 MOD 自带的运行时组件不依赖 .NET。

## Installation / 安装方法

> [!NOTE]
> 下列流程适用于正式 Release 发布后的完整包。当前仓库还没有可安装的公开附件。

1. 从本仓库的
   [Releases](https://github.com/intergra/Dishonored_DOTO_Simplified_Chinese_Translation/releases)
   页面下载 `Dishonored_DOTO_Simplified_Chinese.zip`。
2. 把 ZIP 解压到一个长期保留的目录。解压后应得到
   `Dishonored_DOTO_Simplified_Chinese` 文件夹，第一层可以直接看到 `ModInfo.xml`、
   `Resources` 和 `Runtime`，不会再套一层同名文件夹。
3. 打开已单独下载并解压的
   [Void Installer](https://www.nexusmods.com/dishonored2/mods/31)。
4. **Game folder** 选择包含 `Dishonored_DO.exe` 和 `base` 的游戏根目录。
5. **Mod folder** 选择包含 `ModInfo.xml` 的
   `Dishonored_DOTO_Simplified_Chinese` 文件夹，然后安装。
6. 在 Steam 中把《Dishonored: Death of the Outsider》的语言设置为“中文（繁体）”。
7. 打开 Steam 的“属性 → 通用 → 启动选项”，填写下方的一整行命令，并把路径替换为
   自己的实际解压路径：

```text
"你的MOD目录\Runtime\DOTORuntimeLauncher.exe" --steam-command %command%
```

例如，把文件夹放在 `D:\Dishonored_DOTO_Simplified_Chinese` 时填写：

```text
"D:\Dishonored_DOTO_Simplified_Chinese\Runtime\DOTORuntimeLauncher.exe" --steam-command %command%
```

“你的MOD目录”必须替换为包含盘符的完整绝对路径。命令保持为一整行，路径两侧使用英文
半角双引号。以后仍然只从 Steam 正常点击“开始游戏”，不需要填写游戏 EXE 的路径。

Steam 会先短暂运行 `DOTORuntimeLauncher.exe`。启动器验证游戏和翻译文件、挂起创建
游戏、加载 `DOTORuntimeTranslation.dll`、等待 DLL 就绪并恢复游戏主线程；可靠交接
完成后启动器立即退出，因此启动时看到黑色窗口一闪而过属于正常现象。翻译 DLL 会留在
游戏进程中继续工作，退出游戏后自动释放。

## Updating / 更新方法

1. 关闭游戏。
2. 使用 Void Installer 卸载旧版同名 MOD。
3. 清空旧的 Steam 启动选项，或准备在安装后更新其中的路径。
4. 旧版卸载完成后，再删除旧的解压目录。
5. 下载并解压新版 ZIP。
6. 使用 Void Installer 安装新版 MOD 文件夹。
7. 重新填写指向新版 `DOTORuntimeLauncher.exe` 的 Steam 启动选项。

不要把新版直接覆盖到仍处于安装状态的旧目录，也不要混用不同版本的启动器、DLL 和
翻译目录。

## Uninstallation / 卸载方法

1. 关闭游戏。
2. 打开 Void Installer，在已安装 MOD 列表中卸载本 MOD 的静态资源。
3. 打开 Steam 游戏属性，清空本 MOD 的启动选项。
4. 确认以上两步完成后，删除解压的 `Dishonored_DOTO_Simplified_Chinese` 文件夹。
5. 从 Steam 正常启动游戏，确认已经恢复原版状态。

> [!WARNING]
> Void Installer 只管理静态资源，不会自动清理 Steam 启动选项。卸载时必须完成以上
> 两个部分。

## Compatibility / 兼容性说明

- 当前只支持 Windows x64 Steam 版 `Dishonored_DO.exe 1.145.0.0`。
- 与其他修改 `strings/chinese_m.lang`、中文 Iggy 字体、界面字体依赖或中文
  localized speech 的 MOD 冲突。
- 不建议与旧汉化包、字体替换包或其他中文本地化 MOD 同时安装。
- 本 MOD 不修改关卡流程、敌人 AI、能力数值、武器数值、音频内容或存档格式。
- 游戏更新后如果 EXE 哈希或关键机器码发生变化，启动器会拒绝加载，需要等待兼容性
  更新。
- 《耻辱2》的启动器、DLL、Steam 启动命令和管理器安装状态不能用于本项目。

## Technical Safety / 技术安全说明

- 不替换、不修改磁盘上的 `Dishonored_DO.exe`。
- 不直接修改游戏 `base` 原始归档；静态 MOD 资源由 Void Installer 管理和卸载。
- 运行时组件只在启动阶段验证并加载到游戏进程，不向游戏目录或 MOD 目录写入文件。
- 启动器在翻译 DLL 完成初始化并恢复游戏主线程后立即退出，不会一直驻留后台。
- 翻译 DLL 只修改当前进程内的既有字幕字符串，不重建声明，不保存跨地图对象指针。
- 运行时目录、声明身份、文本槽拓扑、UTF-8 边界和 SHA-256 均经过严格验证。
- 版本、签名、目录或结构验证失败时会停止加载，不在未知游戏版本上继续执行。

## Known Notes / 已知说明

- 游戏语言菜单仍显示“中文（繁体）”，这是因为本 MOD 使用官方中文槽位。
- 只完成 Void Installer 安装、但没有设置 Steam 启动选项时，主界面和字体可以生效，
  但无法获得全部运行时逐条对白译文。
- 从 Steam 启动时会短暂出现一个黑色命令行窗口，随后自动关闭；这不是闪退，也不需要
  手动关闭。
- 运行时启动器不是常驻程序；游戏启动后在任务管理器中看不到它继续运行属于正常现象。
- 当前正式 Release 尚未发布；正式安装包发布后会在本页顶部和 Releases 页面说明。

## Credits / 制作信息

**作者：** NoWindNoMoon / 此情无关风月

**简体中文字形：** Noto Sans SC / Source Han Sans SC

字体依据 SIL Open Font License 1.1 使用。第三方版权与许可详情见
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)，完整字体版权声明和许可证位于正式包的
`licenses/` 目录。

游戏名称、原始文本、图像、音频和其他资产归其各自权利人所有。本 MOD 是非官方、
非商业的玩家制作项目，与 Arkane Studios、Bethesda Softworks 或 ZeniMax Media
没有隶属或认可关系。使用本 MOD 必须拥有通过合法渠道取得的游戏副本。

本仓库采用[自定义使用许可](LICENSE.md)。玩家可以下载、安装并用于个人、非商业的正常
游戏用途，也可以分享本仓库或 Release 页面的原始链接；未经许可不得重新上传、镜像
分发、公开发布修改版或进行商业利用。明确标注的第三方内容继续遵循其各自许可证。

## Troubleshooting / 故障排查

### 安装后仍有繁体对白

- 确认 Steam 游戏语言已经设置为“中文（繁体）”。
- 确认 Void Installer 中已经安装本 MOD。
- 确认 Steam 启动选项仍然存在，并准确指向当前保留目录中的
  `DOTORuntimeLauncher.exe`。
- 确认没有从游戏目录中的 EXE 或其他快捷方式绕过 Steam 启动。

### Steam 点击启动后立即报错或退出

- 检查启动选项路径是否使用英文半角双引号包围，并保持为一整行。
- 确认解压目录没有被移动、改名或删除。
- 确认游戏 EXE 为受支持的 1.145.0.0 版本。
- 确认没有误用《耻辱2》的 `D2RuntimeLauncher.exe` 或 DLL。
- 查看 `%LOCALAPPDATA%\NoWindNoMoon\DishonoredDOTO_SC\runtime.log` 和同目录的
  `runtime.error.txt` 中记录的明确错误原因。

### Void Installer 无法安装或卸载

- 关闭游戏后再操作 Void Installer。
- 确认 Game folder 选择的是包含 `Dishonored_DO.exe` 和 `base` 的 DOTO 游戏目录。
- 确认 Mod folder 第一层直接包含 `ModInfo.xml`，没有多选或少选一层目录。
- 不要手动删除仍处于安装状态的 MOD 资源。
- 如果安装过其他会修改相同资源的 MOD，先卸载冲突 MOD；必要时通过 Steam 验证游戏
  文件完整性后重新安装。

### 字幕换行或文字长度不自然

- 游戏会根据当前界面宽度自动换行，不同分辨率和 UI 缩放可能产生不同断行。
- 请在 Issue 中提供具体界面、任务、角色、分辨率和截图。项目会优先调整单条译文的
  语序和长度，不会修改游戏的 UI 布局或强行接管自动换行。

## Feedback / 反馈

发现问题时，请在
[GitHub Issues](https://github.com/intergra/Dishonored_DOTO_Simplified_Chinese_Translation/issues)
提交反馈，并尽量提供出现位置、当前任务、角色、截图和 `runtime.log`：

- 繁体残留或英文残留
- 字幕缺失、错位或显示时间异常
- 文本溢出、换行不自然或字符显示异常
- 人物、地点、组织、能力、技能或物品译名不一致
- 译文不符合英文原意、剧情语境或人物性格
- 启动、载入、检查点回档、安装、更新或卸载异常

感谢每一位参与审校、测试和反馈问题的玩家。
