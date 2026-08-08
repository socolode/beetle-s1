# apps · 应用目录

存放独角仙S1 的灯光应用脚本（无需编程，下载即用）。

## 目录结构

```
apps/
├── <应用名>/   # 每个应用一个文件夹
│   ├── main.py       # 应用入口脚本（必选）
│   ├── config.json   # 应用默认参数（可选）
│   ├── assets/       # 图片、字体、BMP 素材（可选）
│   └── README.md     # 应用说明（接线、参数、效果展示）
└── config.json       # 应用注册表（启用/关闭应用）
```

## 安装应用

1. 将应用文件夹复制到独角仙S1 U 盘的 `/apps` 目录中
2. 编辑 `apps/config.json`，在 `apps` 数组中添加新应用信息
3. 重启设备，拨动左右键切换到该应用，单击中键启动

> 应用即将上传，敬请期待。详细安装教程见 [独角仙S1 · 应用安装](https://docs.socolode.com/zh-CN/light-painting-controller/beetle-s1/effects-projects/effect-list-install)。
