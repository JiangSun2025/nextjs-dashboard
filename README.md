## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## Next.js 学习课程示例项目，采用 App Router

## 分支命名规范

项目采用 GitHub 分支命名规范

| 前缀 | 用途 | 示例 |
|------|------|------|
| `feature/` | 新功能开发 | `feature/email-notifications` |
| `bugfix/` | 错误修复 | `bugfix/login-redirect-loop` |
| `hotfix/` | 紧急修复 | `hotfix/security-vulnerability` |
| `release/` | 版本发布 | `release/v2.1.0` |
| `chore/` | 维护任务 | `chore/update-dependencies` |
| `docs/` | 文档更新 | `docs/api-documentation` |
| `refactor/` | 代码重构 | `refactor/user-service` |
| `test/` | 测试相关 | `test/integration-tests` |

## 分支工作流

```mermaid
gitgraph
    commit id: "初始提交"
    branch develop
    checkout develop
    commit id: "开发环境初始化"
    
    branch feature/user-auth
    checkout feature/user-auth
    commit id: "实现用户认证"
    commit id: "添加JWT支持"
    checkout develop
    merge feature/user-auth
    commit id: "合并用户认证功能"
    
    branch bugfix/login-error
    checkout bugfix/login-error
    commit id: "修复登录错误"
    checkout develop
    merge bugfix/login-error
    commit id: "修复合并"
    
    branch release/v1.0.0
    checkout release/v1.0.0
    commit id: "版本发布准备"
    commit id: "最终测试"
    checkout main
    merge release/v1.0.0
    commit id: "发布 v1.0.0"
    
    checkout develop
    merge release/v1.0.0
    commit id: "同步发布版本"
    
    branch hotfix/security-patch
    checkout hotfix/security-patch
    commit id: "安全补丁"
    checkout main
    merge hotfix/security-patch
    commit id: "紧急修复"
    
    checkout develop
    merge hotfix/security-patch
    commit id: "同步热修复"
```
