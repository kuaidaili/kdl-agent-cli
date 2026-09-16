# 0.1.0 发行范围与验收记录

2026-09-16，发布负责人张阔确认：公司 CLI 软件包先发行，生产服务随后按既有审批流程上线。`business-e2e`、`production-operations`、`public-entry` 保留为服务上线检查，当前为 `deferred-to-service-rollout`，不标为 passed。该首发安排仅适用于 0.1.0。

## 软件发行检查

发行流水线仍强制 Go/npm 回归、固定候选五平台运行烟测、HTTPS/SHA256/源码校验、GitHub Release 审批与 npm-production 审批，并通过公司 Trusted Publisher 发行。最终结果见本 tag 的 GitHub Actions；本记录不提前声明流水线或 OIDC 已成功。

源码准备时 npm 40 项回归通过；新增发行顺序回归要求没有明确决定、缺证据、缺项或挪用到其他版本时拒绝。官网安装固定 `@kuaidaili/kdl-agent@0.1.0`，公开文档指向 `www.kuaidaili.com`；Gateway API 仍为 `agent-gateway.kdlapi.com`。

macOS 程序暂未签名/公证；不关闭系统安全设置，不宣称最低系统兼容已实测。

## 服务上线检查（待完成）

| 检查 | 待完成内容 |
| --- | --- |
| business-e2e | 当前服务组合的授权负例、限定写与幂等、审计链路 |
| production-operations | 运行版本、留存及告警、恢复点与恢复验证 |
| public-entry | 正式官网/会员中心/安装指南/Skill 部署后回读、首次登录与查询 |

这些检查由发布负责人协调研发、测试与运维完成，结果归档到生产交接记录。软件发行不代表服务上线或上述验收通过，不改变运行时鉴权、租户隔离、限流及审计要求。
