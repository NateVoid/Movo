# 🚗 Movo - 出行服务平台

> 基于 Go + Kubernetes 的分布式出行平台，支持司机管理、行程规划和支付处理

![Go](https://img.shields.io/badge/Go-1.26+-00ADD8?style=flat-square&logo=go)
![Kubernetes](https://img.shields.io/badge/Kubernetes-v1.28+-326CE5?style=flat-square&logo=kubernetes)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-3.12+-FF6600?style=flat-square&logo=rabbitmq)
![Next.js](https://img.shields.io/badge/Next.js-14+-000000?style=flat-square&logo=next.js)

## 📋 项目概述

Movo 是一个现代化的出行服务平台，采用微服务架构，主要功能包括：

- 🚕 **司机服务** - 司机位置管理、状态追踪
- 🗺️ **行程服务** - 路径规划、实时行程追踪
- 💳 **支付服务** - 集成 Stripe 支付
- 🌐 **API 网关** - 统一入口、负载均衡

## 🛠️ 技术栈

| 组件     | 技术                            |
| -------- | ------------------------------- |
| 后端     | Go 1.26+                        |
| 前端     | Next.js 14 + React + TypeScript |
| 数据库   | gRPC + Protocol Buffers         |
| 消息队列 | RabbitMQ                        |
| 追踪     | Jaeger                          |
| 容器化   | Docker                          |
| 编排     | Kubernetes                      |
| 本地开发 | Tilt                            |

## 🚀 快速开始

### 环境要求

- Docker
- Go
- Tilt
- Kubernetes

## ▶️ 启动项目

```bash
tilt up
```

## 📊 监控

查看 Pod 状态：

```bash
kubectl get pods
```

或打开 Kubernetes Dashboard：

```bash
minikube dashboard
```

## 📁 项目结构

```
Movo/
├── services/
│   ├── api-gateway/        # API 网关服务
│   ├── driver-service/     # 司机管理服务
│   ├── trip-service/       # 行程服务
│   └── payment-service/    # 支付服务
├── web/                    # 前端
├── shared/                 # 共享库
│   ├── proto/              # Protocol Buffer 定义
│   ├── messaging/          # 消息队列封装
│   ├── tracing/            # 分布式追踪
│   └── retry/              # 重试机制
├── proto/                  # Proto 文件定义
├── deployment
│   ├── development/        # 开发环境配置
│   └── production/         # 生产环境配置
│       ├── docker/         # Docker 镜像构建
│       └── k8s/            # Kubernetes 部署清单
└── docs/
    └── architecture/       # 架构文档
```

## 📚 相关文档

- [行程创建流程 (v1)](docs/architecture/trip-creation-flow-v1.md)
- [RabbitMQ 消息流程 (v1)](docs/architecture/rabbitmq-flow-v1.md)

## 📄 许可证

本项目采用 [MIT](https://opensource.org/licenses/MIT) 许可证。
