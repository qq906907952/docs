---
title: DeepFlow 路标
permalink: /about/milestone
---

DeepFlow 开源之前已经迭代到了 v6.1.0，2022 年 7 月计划发布的 v6.1.1 将会是首个可下载使用的社区版，届时将具备如下特性：
- AutoMetrics
  - [x] 基于 BPF+AF\_PACKET 的 TCP 网络性能指标
  - [x] 基于 BPF+AF\_PACKET 的 HTTP1/2、Dubbo、MySQL、PostgreSQL、Redis、Kafka、MQTT、DNS 应用协议解析能力
  - [x] 基于 eBPF tracepoint/kprobe 的 HTTP1/2、Dubbo、MySQL、PostgreSQL、Redis、Kafka、MQTT、DNS 应用协议解析能力
  - [x] 基于 eBPF USDT/uprobe 的 Golang/openssl 应用 HTTPS 协议解析能力
- AutoTracing
  - [x] 基于 eBPF 的 AutoTracing 分布式链路追踪能力
  - [x] 支持对所有同步阻塞调用（BIO，Blocking IO）场景下任意服务组成的分布式调用链进行追踪
  - [x] 支持对部分同步非阻塞调用（NIO，Non-blocking IO）场景下任意服务组成的分布式调用链进行追踪
  - [x] 支持内核线程调度（[kernel-level threading](https://en.wikipedia.org/wiki/Thread_(computing))）场景
  - [x] 支持解析请求中的 X-Request-ID 等字段对采用 NIO 模式的网关（如 Envoy）前后的调用链进行追踪
  - [x] 集成 OpenTelemetry 追踪，并与 eBPF/cBPF 追踪数据关联，实现无盲点的分布式追踪
- AutoTagging & SmartEncoding
  - [x] 自动注入 K8s 资源标签、自定义 Label 标签
  - [x] 自动注入公有云资源标签
  - [x] 高性能的 SmartEncoding 标签存储查询能力
- Agent Integration
  - [x] 集成 Prometheus 和 Telegraf 的指标数据
  - [x] 集成 OpenTelemetry 和 SkyWalking 的追踪数据
- Server Integration
  - [x] 提供 SQL API，作为 Grafana 的 DataSource
  - [x] 使用 ClickHouse 作为存储引擎

DeepFlow未来还有很多激动人心的特性等待我们和社区一起开发，包括：
- AutoTracing
  - [ ] 支持更多同步非阻塞调用（NIO，Non-blocking IO）场景
  - [ ] 支持异步调用（AIO，Asynchronous IO）场景
  - [ ] 支持协程调度（hybrid threading）场景
  - [ ] 增强和 OpenTelemetry 的集成能力，通过 eBPF 插入 OTel Tracer API
- AutoTagging & SmartEncoding
  - [ ] 同步服务注册中心，自动注入服务和 API 属性信息
  - [ ] 非容器环境下自动同步并注入进程标签信息
- Active Probe
  - [ ] 支持 Agent 发起主动拨测获取 Metrics
- Continuous Profiler
  - [ ] 支持使用 eBPF 采集 On/Off CPU 火焰图，提供零侵扰的 Continue Profile 能力
- Agent Programmability
  - [ ] 支持 WASM 的可编程应用协议解析能力
- Agent Adaptability
  - [ ] 支持 Agent 以 Sidecar 形式运行于 Serverless Pod 中
  - [ ] 支持运行于 Andriod 操作系统中（智能汽车场景）
- Agent Integration
  - [ ] 集成 Sentry RUM 数据源
  - [ ] 集成 Promtail/Loki 日志数据源
  - [ ] 支持将数据输出至日志文件中，通过日志采集服务 iLogTail 进行采集
- Server Integration
  - [ ] 支持将分布式追踪数据展示在 Grafana Tempo 中
  - [ ] 支持将日志数据展示在 Grafana Loki GUI 中
  - [ ] 支持 PromQL 作为查询 API
  - [ ] 支持作为 Prometheus Exporter 输出 BPF/eBPF 指标数据
  - [ ] 支持将数据输出至 OpenTelemetry Collector
  - [ ] 支持将数据输出至 Kafka
  - [ ] 支持将数据写入至公有云日志存储服务中
