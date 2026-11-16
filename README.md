# Awesome Global & Collection Variable Management

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Tracked Repositories](https://img.shields.io/badge/Maintained%20Tools-Open%20Source%20%26%20SaaS-blue.svg)](#table-of-contents)

> A curated list of top SaaS platforms and open-source tools for **Global & Collection Variable Management**, **Secrets Management**, **Environment Configuration**, and **Self-Hosted Vaults**.

Centralized variable and secrets management ensures secure, consistent configuration across multi-stage CI/CD pipelines, container clusters, local developer machines, and API workspaces. This repository indexes the leading cloud services and battle-tested open-source repositories to manage `.env` files, dynamic credentials, API environment scopes, and encryption keys.

---

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS & Hosted Platforms](#saas--hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Feature Matrix & Selection Guide](#feature-matrix--selection-guide)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global secrets and environment configuration management market is estimated at **$4.2B to $4.6B in 2025** and projected to surpass **$5.3B by 2026** (CAGR ~14–15%), driven by the exponential proliferation of machine-to-machine identities, microservices, and automated CI/CD pipelines. The sector is **moderately fragmented**: baseline adoption is heavily concentrated among hyperscale cloud providers (AWS, Microsoft Azure, Google Cloud) and established enterprise vaults, yet intensely contested by fast-growing developer-first platforms, open-source challengers, and specialized runtime injection tooling.

---

## SaaS & Hosted Platforms

*Ranked in descending order by company valuation / market capitalization.*

| Product | Company Size (Valuation / Market Cap) | Starting Price (Paid Tier) | Free Tier / Trial Limits | Description & Scope |
| :--- | :--- | :--- | :--- | :--- |
| **[Microsoft Azure App Configuration](https://azure.microsoft.com/en-us/products/app-configuration/)** | **~$3.1 Trillion** (Public: MSFT) | **$1.20/day** per Standard store instance | **Free tier**: 1 store per subscription, 10 MB storage, 1,000 requests/day | Centralized configuration store with feature flag management, key-value labels, and native integration across Azure services and Kubernetes. |
| **[Google Cloud Secret Manager](https://cloud.google.com/secret-manager)** | **~$2.2 Trillion** (Public: GOOGL) | **$0.06/active secret version/month** (+ $0.03 per 10k API operations) | **Free tier**: 6 active secret versions, 10,000 access operations/month, plus $300 new customer credit (90 days) | Fully managed, audit-logged secret storage with automated replication, fine-grained Cloud IAM policies, and rotation workflows. |
| **[AWS Systems Manager Parameter Store](https://aws.amazon.com/systems-manager/)** | **~$2.1 Trillion** (Public: AMZN) | **$0.05/parameter/month** (Advanced tier; Standard tier is free) | **Free tier**: Unlimited Standard parameters (up to 10,000 per account/region), 4 KB size limit per parameter | Hierarchical key-value configuration and encrypted secret store tightly integrated with EC2, ECS, EKS, and AWS Lambda. |
| **[HashiCorp Vault (HCP Vault Dedicated)](https://www.hashicorp.com/products/vault)** | **$6.4 Billion** (Acquired by IBM) | **~$0.62/cluster hour** (~$450/month for Development tier) | **Free trial**: $500 trial credits valid for up to 6 months (capped at 1 Development cluster; CE self-hosted is free) | Enterprise cloud-managed secrets engine supporting dynamic on-demand credentials, encryption-as-a-service, and strict audit logs. |
| **[1Password Secrets Automation](https://developer.1password.com/docs/secrets-automation/)** | **$6.8 Billion** (Private) | **$8.99/user/month** (Included in 1Password Business plan) | **Free trial**: 14-day full-featured free trial (no permanent free tier for business/automation) | Programmatic secrets injection and service accounts powered by 1Password Connect Server, `op` CLI, and developer SDKs. |
| **[Postman Variables](https://learning.postman.com/docs/sending-requests/variables/variables/)** | **$5.6 Billion** (Private) | **$19/user/month** (Team tier, billed annually) or **$9/month** (Solo) | **Free tier**: 1 user only, unlimited collection runs, up to 3 public workspace variables, Postman Vault for local secrets | Scoped variable ecosystem (global, environment, collection, data, and local) built for automated API testing and team workflows. |
| **[Doppler](https://www.doppler.com/)** | **~$45 Million** (Private VC-backed) | **$8/user/month** (Developer tier for >3 users) or **$21/user/month** (Team tier) | **Free tier**: Free forever for up to 3 users with Doppler CLI, integrations, service tokens, and 3-day log history | Centralized secrets platform featuring zero-file runtime injection via `doppler run --`, auto-sync integrations, and environment branches. |

---

## Open-Source GitHub Projects

*Ranked in descending order by GitHub stargazers.*

| Project | Stars | Primary Focus | License | Key Capabilities |
| :--- | :--- | :--- | :--- | :--- |
| **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** | [![Stars](https://img.shields.io/github/stars/dani-garcia/vaultwarden?style=social&color=white)](https://github.com/dani-garcia/vaultwarden/stargazers) | Self-Hosted Password & Secret Vault | AGPL-3.0 | Lightweight Bitwarden-compatible server written in Rust. Supports SQLite/PostgreSQL, Bitwarden desktop/CLI apps, web vault, and OIDC SSO. |
| **[HashiCorp Vault (Community Edition)](https://github.com/hashicorp/vault)** | [![Stars](https://img.shields.io/github/stars/hashicorp/vault?style=social&color=white)](https://github.com/hashicorp/vault/stargazers) | Enterprise Secrets & PKI Engine | BSL-1.1 | Industry-standard engine for dynamic database/cloud credentials, leased secrets, transit encryption, revocation trees, and detailed audit trails. |
| **[Gitleaks](https://github.com/gitleaks/gitleaks)** | [![Stars](https://img.shields.io/github/stars/gitleaks/gitleaks?style=social&color=white)](https://github.com/gitleaks/gitleaks/stargazers) | Secret Scanning & Leak Prevention | MIT | Blazing-fast Go-based static secret scanner for Git repositories, pre-commit hooks, and CI/CD pipelines to block leaked tokens before merge. |
| **[Infisical](https://github.com/Infisical/infisical)** | [![Stars](https://img.shields.io/github/stars/Infisical/infisical?style=social&color=white)](https://github.com/Infisical/infisical/stargazers) | Developer-First Secrets Platform | MIT / PolyForm | Comprehensive secrets platform with E2EE, Kubernetes operator, dynamic database credentials, PKI certificate management, and agent identity. |
| **[age](https://github.com/FiloSottile/age)** | [![Stars](https://img.shields.io/github/stars/FiloSottile/age?style=social&color=white)](https://github.com/FiloSottile/age/stargazers) | File Encryption & Key Tooling | BSD-3-Clause | Modern, simple, and composable command-line encryption tool with small explicit keys, SSH key support, and UNIX-style piping architecture. |
| **[SOPS (Secrets OPerationS)](https://github.com/getsops/sops)** | [![Stars](https://img.shields.io/github/stars/getsops/sops?style=social&color=white)](https://github.com/getsops/sops/stargazers) | Encrypted Files in Git (GitOps) | MPL-2.0 | Encrypts values within YAML, JSON, ENV, and INI files while retaining structural keys. Interoperates with AWS KMS, GCP KMS, Azure Key Vault, and age. |
| **[dotenv](https://github.com/motdotla/dotenv)** | [![Stars](https://img.shields.io/github/stars/motdotla/dotenv?style=social&color=white)](https://github.com/motdotla/dotenv/stargazers) | Local Node.js `.env` Loader | BSD-2-Clause | The standard Node.js zero-dependency module for loading environment variables from `.env` files into `process.env`. |
| **[Bitnami Sealed Secrets](https://github.com/bitnami-labs/sealed-secrets)** | [![Stars](https://img.shields.io/github/stars/bitnami-labs/sealed-secrets?style=social&color=white)](https://github.com/bitnami-labs/sealed-secrets/stargazers) | Kubernetes Asymmetric Encryption | Apache-2.0 | Encrypts Kubernetes Secrets into one-way `SealedSecret` custom resources safe for public Git storage; decryptable only by the in-cluster controller. |
| **[External Secrets Operator](https://github.com/external-secrets/external-secrets)** | [![Stars](https://img.shields.io/github/stars/external-secrets/external-secrets?style=social&color=white)](https://github.com/external-secrets/external-secrets/stargazers) | Multi-Backend K8s Synchronizer | Apache-2.0 | Kubernetes operator synchronizing secrets from external APIs (AWS SSM, Vault, Infisical, 1Password, GCP) directly into native K8s Secrets. |
| **[dotenv-vault](https://github.com/dotenv-org/dotenv-vault)** | [![Stars](https://img.shields.io/github/stars/dotenv-org/dotenv-vault?style=social&color=white)](https://github.com/dotenv-org/dotenv-vault/stargazers) | Encrypted `.env` Synchronization | CC-BY-NC-ND | Encrypts `.env` files into `.env.vault` files safe for version control, decodable in production environments using a single runtime `DOTENV_KEY`. |
| **[CyberArk Summon](https://github.com/cyberark/summon)** | [![Stars](https://img.shields.io/github/stars/cyberark/summon?style=social&color=white)](https://github.com/cyberark/summon/stargazers) | CLI Runtime Secret Injection | MIT | Command-line utility that fetches secrets from storage providers defined in `secrets.yml` and injects them as ephemeral process environment variables. |
| **[Pick](https://github.com/bndw/pick)** | [![Stars](https://img.shields.io/github/stars/bndw/pick?style=social&color=white)](https://github.com/bndw/pick/stargazers) | Minimalist Terminal Vault | MIT | Lightweight, secure command-line password and secret manager for UNIX-like environments written in Go, using GPG encryption. |
| **[Pulumi ESC](https://github.com/pulumi/esc)** | [![Stars](https://img.shields.io/github/stars/pulumi/esc?style=social&color=white)](https://github.com/pulumi/esc/stargazers) | Composable Environment Orchestration | Apache-2.0 | Hierarchical environment configuration and secret orchestration layer aggregating data across Vault, 1Password, AWS Secrets Manager, and Azure. |

---

## Feature Matrix & Selection Guide

```
+-----------------------------------------------------------------------------------+
|                           USE-CASE SELECTION GUIDE                                |
+-----------------------------------------------------------------------------------+
| Local Dev Only              -> dotenv, Pick                                       |
| Encrypted Files in Git      -> SOPS, age, dotenv-vault, Bitnami Sealed Secrets    |
| Multi-Cloud / Dynamic Leases-> HashiCorp Vault, Infisical, External Secrets       |
| API Testing Scopes          -> Postman Variables                                  |
| Zero-File Process Injection -> Doppler, CyberArk Summon, 1Password Secrets        |
| Secret Leak Interception    -> Gitleaks (pre-commit / CI)                         |
+-----------------------------------------------------------------------------------+
```

---

## How to Contribute

1. Fork the repository.
2. Add or update tool entries in `README.md` respecting established table schemas and sorting.
3. Ensure exact pricing data, specific free tier limits, and stargazer social badge links are supplied.
4. Submit a Pull Request with a clear description of changes.

---

## Disclaimer

- This is a community-curated directory intended for research, architectural comparisons, and technical selection.
- Secrets and variable managers handle mission-critical credentials. Always implement multi-factor authentication (MFA), least-privilege role-based access control (RBAC), and never push unencrypted credentials to public repositories.

---

*Maintained by the DevOps and security community for safer, decoupled configuration.*
