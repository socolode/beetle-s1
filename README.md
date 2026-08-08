# 独角仙S1 · 官方资源仓库 | Beetle S1 Official Repository

[官方网站](https://socolode.com) · [文档中心](https://docs.socolode.com)

> 本仓库集中存放 **独角仙S1 灯光控制器** 的所有官方与社区资源，包括：应用（App）脚本、固件、3D 打印文件、电路板设计、接线参考等。持续更新，欢迎贡献。

---

## 仓库目录结构

```
beetle-s1/
├── apps/                # 应用脚本（无需编程，下载即用）
├── firmware/            # 设备固件（.uf2 / .bin 刷机文件）
│   ├── stable/          # 稳定版固件
│   └── beta/            # 测试版固件
├── hardware/            # 硬件设计文件
│   ├── pcb/             # 电路板 Gerber / 原理图（KiCad）
│   ├── schematic/       # 接线示意图
│   └── bom/             # 物料清单 BOM
├── 3d-models/           # 3D 打印模型（STL / STEP）
│   ├── case/            # 主机外壳
│   ├── accessories/     # 配件：夹具、手柄、支架
│   └── ...
└── docs/                # 补充说明文档
```

---

## 快速开始

### 1. 安装应用（App）

适合普通用户，**无需编程**：

1. 打开下方 [应用列表](#应用列表-apps)，挑选你喜欢的应用
2. 点击对应行的「下载」获取压缩包，解压到本地
3. 把解压后的文件夹复制到独角仙S1 U 盘的 `/apps` 目录中
4. 编辑 `apps/config.json`，在 `apps` 数组中加入新应用信息（参考下方模板）
5. 重启设备，拨动左右键切换到该应用，单击中键启动

> 完整图文安装步骤见文档 [**独角仙S1 · 应用安装**](https://docs.socolode.com/zh-CN/light-painting-controller/beetle-s1/effects-projects/effect-list-install)

### config.json 填写模板

```json
{
  "apps": [
    {
      "name": "应用名称",
      "folder": "应用文件夹名",
      "enabled": true
    }
  ]
}
```

### 2. 升级固件

1. 进入 `firmware/` 目录，下载对应版本的固件文件（`.uf2`）
2. 独角仙S1 关机状态下**按住功能键**接入电脑进入刷机模式，电脑会出现一个名为 `BEETLE-S1` 的 U 盘
3. 把 `.uf2` 文件拖入 U 盘根目录，设备会自动重启完成升级

> 详细说明见文档：[固件升级教程](https://docs.socolode.com/zh-CN/light-painting-controller/beetle-s1)

### 3. 3D 打印外壳 / 配件

1. 进入 `3d-models/` 目录，选择需要的模型文件（`.stl` / `.step`）
2. 使用切片软件（Cura、PrusaSlicer 等）导入并调整参数
3. 推荐打印材料：PLA（外壳）、PETG（受力配件）

### 4. 硬件自制 / 维修

- `hardware/pcb/`：电路板 Gerber 生产文件与 KiCad 原理图（自制或维修参考）
- `hardware/bom/`：物料清单（各元件型号、参数、采购建议）
- `hardware/schematic/`：WS2812 / SK6812 / 灯环 / 矩阵的接线参考图

---

## 应用列表（Apps）

| 应用名称 | 说明 | 适用场景 | 作者 | 下载 |
|---------|------|---------|------|------|
| （待上传） | 即将开放 | - | socolode | 稍后开放 |

> 更多应用正在陆续上传中。若应用库暂无你需要的应用，欢迎到社区反馈需求，或参考进阶开发章节自行编写。

### 每个应用的推荐目录结构

```
my-app/
├── main.py            # 应用入口脚本（必选）
├── config.json        # 应用默认参数（可选）
├── assets/            # 图片、字体、BMP 素材（可选）
│   └── logo.bmp
├── README.md          # 应用说明（接线、参数、效果展示，推荐）
└── preview.png        # 效果预览图，用于应用库展示（推荐）
```

---

## 贡献你的资源（PR 欢迎）

本仓库欢迎社区开发者提交应用、固件、3D 模型、硬件设计等资源。

### 贡献应用（App）

1. **Fork** 本仓库
2. 在 `apps/` 目录下创建一个以你的应用名称命名的文件夹，按上述结构放置文件
3. 编辑上方的「应用列表」表格，添加一行说明
4. 发起 **Pull Request**，等待审核合并

### 贡献 3D 模型 / 硬件文件

1. **Fork** 本仓库
2. 在对应目录（`3d-models/` 或 `hardware/`）下新建目录
3. 附上 `README.md` 说明：适用型号、打印参数（3D）、版本信息（硬件）等
4. 发起 **Pull Request**

### 贡献建议

- 应用 README.md 中必须包含：接线说明、参数说明、效果展示（图片或视频链接）
- 3D 模型建议同时提供 `.stl`（通用切片）和 `.step`（源文件可编辑）
- 如使用第三方素材，确保版权允许分发
- 推荐在说明里附上设备与灯材型号，方便他人复现

### 进阶开发

- 搭建开发环境、编写第一个应用、打包与分享教程：
  👉 [独角仙S1 · 进阶开发](https://docs.socolode.com/zh-CN/light-painting-controller/app-development/setup-environment)

---

## 相关链接

- 产品官网：[socolode.com](https://socolode.com)
- 文档中心：[docs.socolode.com](https://docs.socolode.com)
- 主仓库（文档与网站源码）：[socolode/docs](https://github.com/socolode/docs)
- 提交 Bug / 功能建议：[Issues](https://github.com/socolode/beetle-s1/issues)

---

## License

- 本仓库中的代码、应用脚本、固件、硬件设计文件按 **MIT License** 发布（见 [LICENSE](./LICENSE)）
- 第三方素材版权归其原作者所有，详见各目录中的说明
