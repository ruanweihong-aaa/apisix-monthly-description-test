---
title: "2026 社区月报 (10.01 - 10.31)"
keywords: ["Apache APISIX", "API 网关", "社区月报", "贡献者"]
description: "本期月报聚焦流量可观测性与服务发现：Stream Prometheus 指标支持按服务区分，Kubernetes 服务发现可跨集群组合节点；同时支持将 OpenID Connect 验证后的声明传递至上游请求头。"
tags: [Community]
---

本月，我们围绕“看清流量、找到服务、传递可信身份”三个方向完善 Apache APISIX。下面通过几个具体场景介绍相关进展。

<!--truncate-->

## 监控：按服务查看流量

Stream Prometheus 指标增加了服务标签。多个服务共用端口时，也能按服务区分指标，方便定位流量异常。

相关改动：[PR #13992](https://github.com/apache/apisix/pull/13992)。

## 服务发现：按需选择多个集群

Kubernetes 服务发现支持通过 `discovery_args.cluster_ids` 指定多个集群。APISIX 会合并并去重所选集群的节点，便于为同一个上游组合服务实例。

相关改动：[PR #13991](https://github.com/apache/apisix/pull/13991)。

## 认证：向上游传递可信身份

OpenID Connect 支持将验证后的声明映射到上游请求头。业务服务可以读取经过网关验证的身份信息，减少重复处理。

相关改动：[PR #14030](https://github.com/apache/apisix/pull/14030)。

## 社区小记

感谢参与讨论、反馈问题和提交代码的社区成员。欢迎大家试用这些功能，并分享实际使用中的体验。
