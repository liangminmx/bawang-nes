# 小霸王游戏机 Docker 版

基于 JSNES 的网页版 NES 模拟器，在浏览器中即可玩 FC/魂斗罗等经典游戏。

> 此项目是根据 [echeverra.cn/bawang](https://echeverra.cn/bawang) 改造的 Docker 镜像

![Docker Image Size](https://img.shields.io/docker/image-size/jzbdc/bawangnes?style=flat)
![Docker Pulls](https://img.shields.io/docker/pulls/jzbdc/bawangnes?style=flat)

## 特性

- 🎮 支持 644 个 NES 游戏（魂斗罗、超级玛丽、忍者龙剑传等）
- 🖥️ 支持 PC 和手机浏览器
- 📱 支持触屏控制
- 🐳 Docker 容器化部署
- ☁️ GitHub Packages 自动构建

## 快速开始

### 使用 Docker Compose（推荐）

```bash
# 克隆仓库
git clone https://github.com/liangminmx/bawang-nes.git
cd bawang-nes

# 启动服务
docker-compose up -d

# 访问游戏
# http://localhost:8080
```

### 使用 Docker

```bash
# 拉取镜像
docker pull jzbdc/bawangnes:latest

# 运行容器
docker run -d -p 8080:80 --name bawang-nes jzbdc/bawangnes:latest

# 访问游戏
# http://localhost:8080
```

### 使用 Docker Run

```bash
docker run -d \
  --name bawang-nes \
  -p 8080:80 \
  jzbdc/bawangnes:latest
```

## 控制说明

### 键盘控制

| 按键 | 功能 |
|------|------|
| 方向键 | 上下左右 |
| Z | A 键 |
| X | B 键 |
| Enter | Start |
| Shift | Select |

### 触屏控制

手机浏览器访问时显示虚拟手柄，支持触屏操作。

## 添加更多游戏

将 `.nes` 格式的 ROM 文件放入 `roms/` 目录，然后重启容器即可。

```bash
# 复制新的 ROM 文件
cp your_game.nes roms/

# 重启容器
docker-compose restart
```

## 技术栈

- 前端：JSNES (JavaScript NES 模拟器)
- Web 服务器：Nginx (Alpine)
- 容器化：Docker

## 许可证

仅供学习交流使用，请尊重游戏版权。

## 致谢

感谢原作者及资源收集者的辛苦付出！

## 相关链接

- [JSNES 官方](https://github.com/bfirsh/jsnes)
- [GitHub Packages](https://github.com/liangminmx/bawang-nes/pkgs/container/bawang-nes)
