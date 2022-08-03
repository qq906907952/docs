---
title: DeepFlow 产品
permalink: /about/editions
---

# 社区版（Community Edition）

DeepFlow 社区版是一个开源版本，是一个高度自动化的可观测性`数据平台`。
它的核心采用 Apache 2.0 许可证，前端页面完全基于 Grafana 因此采用 AGPL 许可证。
它具备高效建设可观测性所需要的的所有功能，包括：

- AutoMetrics：基于 eBPF/BPF，自动采集应用、网络全栈性能指标
- AutoTracing：基于 eBPF/BPF，自动追踪微服务分布式调用链
- AutoLogging：基于 eBPF/BPF，自动采集 TCP/UDP 流日志、HTTP/MySQL/Redis 等应用的访问日志
- Integration：集成 Prometheus/Telegraf 等指标数据，解决数据孤岛和高基数问题
- Integration：集成 OpenTelemetry/SkyWalking 等追踪数据，实现无盲点分布式追踪
- Integration：集成 Fluentd 等外部日志数据源，解决日志存储的高资源消耗问题
- AutoTagging：支持同步公有云资源标签，并自动注入所有观测数据
- AutoTagging：支持同步容器资源标签和自定义 Label，并自动注入所有观测数据
- AutoTagging：支持 SmartEncoding 高性能数据标签存储
- 支持使用 Grafana 展示指标、追踪、日志数据
- 支持统一监控多个 K8s 集群及非容器服务器
- 采集 Agent 支持运行于 K8s 节点、Linux Host 环境中
- 支持在 X86、ARM 体系架构下部署

# 企业版（Enterprise Edition）

DeepFlow 企业版是一个高度自动化的一站式可观测性平台，
它拥有企业级的可视化及管理界面、具备完整的数据分析和增强的数据治理能力。
除社区版所有功能之外，它还有如下功能：

- 支持 Serverless 多租户网络隔离容器环境下的 AutoMetrics、AutoTracing、AutoLogging
- 支持 Kata 等安全沙箱（runv）容器环境下的 AutoMetrics、AutoTracing、AutoLogging
- 支持 Windows 服务器、HyperV 宿主机、ESXi 宿主机环境下的 AutoMetrics、AutoTracing、AutoLogging
- AutoMetrics 及 AutoLogging：支持零侵扰采集整个 KVM 宿主机上所有虚机、Pod 的数据，包括使用 DPDK 数据面的环境
- AutoMetrics 及 AutoLogging：支持采集专有云 NFV 四七层网关的数据，包括使用 DPDK 数据面的环境
- AutoMetrics 及 AutoLogging：支持采集物理网络设备的 Packet、NetFlow、sFlow 并生成指标数据
- AutoTracing：除进程、Pod、虚拟机以外，支持覆盖宿主机、NFV 网关、物理防火墙负载均衡的分布式调用链追踪
- AutoTracing：除 Pod、虚拟机以外，支持覆盖宿主机、NFV 网关、物理防火墙负载均衡的全栈智能 NAT 追踪
- AutoLogging：支持高性能的全网包头存储能力，支持与流日志关联查询、展示 TCP 通信逐包时序图
- AutoLogging：支持按需配置流量过滤策略，存储原始流量以供回溯取证
- AutoTagging：与专有云产品深度适配，包括阿里、腾讯、华为等主流云平台
- 支持按需配置流量过滤策略，向安全、网络、审计等流量消费工具分发流量
- 支持指标、追踪、日志数据的关联查询、自动跳转
- 支持一站式的告警、报表、SLO 等多团队协同功能
- 支持为多租户提供服务，支持数据权限隔离
- 支持 Agent 与 Server 之间的加密数据传输
- 支持统一监控多个 Region 的专有云、公有云、容器资源
- 提供完善的金融、能源、运营商（IT、5GC）、车联网等行业的云原生可观测性建设解决方案
- 提供企业级的售后支持服务，包括故障排查、性能调优、版本升级、可观测性最佳实践落地等

# 云服务（Cloud Edition）

DeepFlow 云服务版是一个完全托管的一站式可观测性平台，
它拥有与企业版一致的功能，目前处于测试试用阶段。