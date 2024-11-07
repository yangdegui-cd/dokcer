# 安装Keycloak

## Keycloak是什么?
Keycloak 是一个开源的身份和访问管理（Identity and Access Management, IAM）解决方案，主要用于保护现代应用程序和服务。它提供了一系列功能，旨在简化和管理用户身份验证、授权和用户管理任务。
## Keycloak用什么功能
### 1. 单点登录（SSO）
允许用户在多个应用程序之间进行无缝的登录和注销操作，减少重复登录，提高用户体验。
### 2. 身份联合（Identity Federation）
支持与第三方身份提供者集成，如 Google、Facebook、Microsoft Azure AD 等，使用户可以通过已有的社交账户登录。
### 3. 多因子认证（MFA）
提供额外的安全层，支持多种认证方式，如短信验证码、TOTP（基于时间的一次性密码）、硬件令牌等。
### 4. 用户管理
提供用户注册、配置文件管理、密码重置等功能，允许管理员轻松管理用户信息。
### 5. 身份提供者（IDP）支持
支持多种协议，如 OpenID Connect、OAuth 2.0 和 SAML 2.0，让 Keycloak 可以与不同的服务和应用集成。
### 6. 社会登录（Social Login）
支持通过社交媒体账户（如 Facebook、Twitter、Google）进行登录。
### 7. 授权服务
支持基于角色的访问控制（RBAC），可以定义详细的访问策略和权限。
### 8. LDAP/Active Directory 集成
能够与企业目录服务（如 LDAP、Active Directory）集成，从而同步用户信息。
### 9.REST API
提供完整的 REST API，方便开发者进行自动化和自定义集成。
## Keycloak有什么用途？
Keycloak 适用于需要用户身份验证和权限管理的各种场景，具体包括

### 1. Web 应用程序
为 web 应用程序提供身份验证和授权功能，无需在每个应用中重复实现这些功能。
### 2. 移动应用
为移动应用提供 OAuth 2.0 和 OpenID Connect 支持，实现安全的用户身份验证。
### 3. 微服务架构
使用 Keycloak 统一管理微服务中的身份和权限，简化权限管理。
### 4. 企业应用集成
将 Keycloak 用作企业内部应用的身份管理和 SSO 解决方案，减少不同系统之间的身份验证复杂性。
### 5. 安全 API
使用 Keycloak 来保护 API 访问，确保只有授权用户和应用程序可以访问 API。


## 使用本地Mysql安装
### 登录本地Mysql, 创建服务器以及账号
```SQL
CREATE DATABASE keycloak;
CREATE USER 'keycloak'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON keycloak.* TO 'keycloak'@'%';
FLUSH PRIVILEGES;
```
### 下载并启动 docker compose

```Bash
mkdir <path>
cd <path>
https://github.com/yangdegui-cd/dokcer.git
cd docker/keycloak
docker compose up
```

> <a href="https://www.keycloak.org/getting-started/getting-started-docker#_taking_the_next_step">官方文档</a>

> <a href="http://docs.ydgui.com/ms-sd-installkeycloak.html">我的文档集</a>
