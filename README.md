# XueXI 学习系统

XueXI 是一个基于 Spring Boot 构建的轻量级学习系统后端服务，提供 RESTful API 接口，支持用户管理、学习资源等核心功能。

## 技术栈

| 技术 | 版本 |
|------|------|
| Java | 1.8 |
| Spring Boot | 2.7.18 |
| Maven | 3.x |
| Spring Data REST | - |
| Spring HATEOAS | - |

## 功能特性

- RESTful API 设计，遵循 HATEOAS 规范
- 标准化项目结构，便于扩展
- 简洁的依赖设计，启动快速
- 支持用户服务管理（开发中）
- 可扩展的模块化架构

## 快速开始

### 环境要求

- JDK 1.8 或更高版本
- Maven 3.x

### 安装

```bash
# 克隆项目
git clone https://github.com/thx19981/XueXI.git

# 进入项目目录
cd XueXI
```

### 运行

```bash
# 方式一：直接运行
mvn spring-boot:run

# 方式二：打包后运行
mvn clean package
java -jar target/xuexi-1.0.0.jar
```

服务启动后，访问 `http://localhost:8085`

## 使用示例

### 健康检查

```bash
curl http://localhost:8085/
```

## 配置说明

配置文件位于 `src/main/resources/application.yml`：

```yaml
server:
  port: 8085

spring:
  application:
    name: xuexi
```

### 配置项说明

| 配置项 | 说明 | 默认值 |
|--------|------|--------|
| server.port | 服务端口 | 8085 |
| spring.application.name | 应用名称 | xuexi |

## 项目结构

```
XueXI/
├── src/main/
│   ├── java/com/xuexi/xuexi/
│   │   ├── XuexiApplication.java    # 启动类
│   │   └── service/
│   │       └── UserService.java     # 用户服务
│   └── resources/
│       └── application.yml          # 应用配置
├── pom.xml                          # Maven 配置
└── README.md                        # 项目文档
```

## 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/your-feature`)
3. 提交更改 (`git commit -m 'Add some feature'`)
4. 推送分支 (`git push origin feature/your-feature`)
5. 创建 Pull Request

## 许可证

MIT License