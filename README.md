# 小霸王游戏机 Docker版

基于 JSNES 的网页版 NES 模拟器，支持在浏览器中直接玩 FC/魂斗罗等游戏。

## 快速部署

```bash
# 克隆仓库
git clone https://github.com/liangminmx/bawang-nes.git
cd bawang-nes

# 添加游戏ROM
# 将 .nes 文件放到 roms/ 目录

# 构建并运行
docker-compose up -d
```

## 访问

打开浏览器访问: http://localhost:8080

## 添加游戏

将 NES 格式的 ROM 文件放入 `roms/` 目录，然后刷新页面即可看到新游戏。

## 控制器

- **方向键**: 上/下/左/右
- **A/B 键**: 攻击
- **Select**: 选择游戏
- **Start**: 开始/暂停
