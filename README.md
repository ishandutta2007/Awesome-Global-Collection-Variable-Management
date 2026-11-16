# Awesome-Global-Collection-Variable-Management

# Top Global & Collection Variable Management Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Secrets Management, Environment Configuration & Self-Hosted Vaults*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Global & Collection Variable Management**. These tools help teams manage configuration variables and secrets across environments—covering everything from Postman's collection variables for API testing to enterprise secrets managers like HashiCorp Vault and Infisical, and lightweight `.env` file tooling for local development.

**Examples** include Postman Variables, HashiCorp Vault, Infisical, Doppler, AWS Systems Manager, Azure App Configuration, 1Password Secrets Automation, and dotenv-vault (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted secrets management, open-source environment variable tooling, and community-driven configuration platforms—ideal for teams seeking data sovereignty and avoiding per-secret or per-seat SaaS pricing. The open-source landscape is genuinely mature: **Infisical** has emerged as the leading open-source secrets platform with 28,832 GitHub stars and 15,000+ organizations , **HashiCorp Vault** remains the enterprise standard for dynamic credentials and PKI , and **Vaultwarden** offers a lightweight Bitwarden-compatible server for password and secret storage .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Postman Variables](https://learning.postman.com/docs/sending-requests/variables/variables/)** | **Collection, environment, and global variables for API testing.** Variables can be scoped to a collection, environment, or globally—enabling reusable values across requests. **Postman Vault** stores secrets locally that never sync to the cloud . | Included with Postman (Free/Solo/Team/Enterprise) | **Free**: 1 user only, unlimited collection runs, no team workspace |
| **[Doppler](https://www.doppler.com/)** | **Secrets management platform with runtime injection.** Centralizes environment variables across projects/configs (dev/ci/prod) with CLI injection via `doppler run --`. **Never writes secrets to disk**—runtime injection only . | Quote-only (team-based) | **Free tier** available for small teams |
| **[HashiCorp Vault (HCP)](https://www.hashicorp.com/)** | **Enterprise secret management standard.** Secure storage for key/value pairs, **dynamic secrets** generated on-demand with automatic revocation, encryption-as-a-service, and detailed audit logs . | Quote-only (enterprise); HCP Vault from ~$0.03/hour | **Vault Community Edition** free (self-hosted); HCP trial available |
| **[AWS Systems Manager Parameter Store](https://aws.amazon.com/systems-manager/)** | Secure hierarchical storage for configuration data and secrets. **Advanced Parameters: $0.05/parameter/month**; standard parameters free. Integrates natively with EC2, Lambda, ECS, and CloudFormation . | Advanced: **$0.05/parameter/month**; Standard: **free** | **Free tier**: standard parameters, no additional charge |
| **[Azure App Configuration](https://azure.microsoft.com/en-us/products/app-configuration/)** | Centralized configuration store with feature flags, key-value pairs, and label-based environments. Integrates with .NET, Java, Spring, and Kubernetes . | **$1.20/day** per Standard tier instance; Free tier available | **Free tier**: 10 MB storage, 1,000 requests/day |
| **[1Password Secrets Automation](https://developer.1password.com/docs/secrets-automation/)** | **Secrets automation within 1Password.** Service accounts provide programmatic access to vault items via CLI (`op`) or SDKs. **`op-exec`** runs commands with 1Password secrets as environment variables—similar to `doppler run` but using a 1Password item as the config source . | Included with 1Password Business/Enterprise | No free tier for Secrets Automation; requires paid 1Password plan |
| **[Google Secret Manager](https://cloud.google.com/secret-manager)** | Managed secrets storage with versioning, rotation, and IAM-based access control. | Pay-per-secret-version and access operations | **$300 credit** for new Google Cloud customers (90 days) |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Infisical](https://github.com/Infisical/infisical)** | [![Stars](https://img.shields.io/github/stars/Infisical/infisical?style=social&color=white)](https://github.com/Infisical/infisical/stargazers) | **The most complete open-source secrets management platform with 28,832 GitHub stars and 15,000+ organizations.** **MIT licensed** (enterprise features in `ee/` directory require a license) . **Core capabilities**: secrets storage with AES-256-GCM encryption, E2EE mode, versioning/rollback, **dynamic secrets** for databases and AWS IAM, **machine identity** for CI/CD and AI agents via OIDC (GitHub Actions, AWS, Azure, GCP, Kubernetes), **PKI/certificate management**, **secrets scanning** for hardcoded credentials, **KMS**, and **PAM** for privileged access . **Self-host or use Infisical Cloud**; lighter to operate than HashiCorp Vault with less vendor lock-in than AWS Secrets Manager . **Best for teams wanting a modern, all-in-one secrets platform** without Vault's operational weight. |
| **[HashiCorp Vault (Community)](https://github.com/hashicorp/vault)** | [![Stars](https://img.shields.io/github/stars/hashicorp/vault?style=social&color=white)](https://github.com/hashicorp/vault/stargazers) | **The open-source foundation of enterprise secret management.** **Secure storage** with encryption before persistence. **Dynamic secrets** generated on-demand for AWS/SQL with automatic lease-based revocation. **Encryption as a service** without storing the data. **Revocation trees** for key rolling and intrusion response. **Detailed audit logs** for every access . **Trade-off**: operational complexity—Vault is a high-value target requiring careful hardening, unsealing, and HA setup; heavier than Infisical for smaller teams . **Best for organizations needing dynamic credentials and enterprise-grade audit** at scale. |
| **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** | [![Stars](https://img.shields.io/github/stars/dani-garcia/vaultwarden?style=social&color=white)](https://github.com/dani-garcia/vaultwarden/stargazers) | **Lightweight Rust implementation of the Bitwarden server API for self-hosted password and secret storage.** **AGPL-3.0 licensed**, runs on minimal resources (SQLite by default, MySQL/PostgreSQL supported) . **Web vault and Bitwarden clients** work with it; **admin panel** for user management. **SSO with OpenID Connect** added in v1.35.0 . **Trade-off**: community-supported (no vendor SLA), enterprise features like advanced RBAC are limited . **Best for personal use and small teams** wanting Bitwarden's ecosystem without cloud dependency. |
| **[dotenv-vault](https://github.com/dotenv-org/dotenv-vault)** | [![Stars](https://img.shields.io/github/stars/dotenv-org/dotenv-vault?style=social&color=white)](https://github.com/dotenv-org/dotenv-vault/stargazers) | **Encrypted `.env` file management built on the ubiquitous `dotenv` library.** Syncs `.env` files across teams with **encrypted `.env.vault` files** that can safely live in version control. **`DOTENV_KEY`** decrypts the vault at runtime—no plaintext secrets scattered across platforms . **CLI commands**: `dotenv-vault push/pull` with environment and filename options (e.g., `npx dotenv-vault push production .env.production`) . **Best for teams wanting to keep `.env` files in Git safely** without adopting a full secrets platform. |
| **[SOPS](https://github.com/getsops/sops)** | [![Stars](https://img.shields.io/github/stars/getsops/sops?style=social&color=white)](https://github.com/getsops/sops/stargazers) | **Encrypts values inside YAML/JSON/env files while leaving structure readable.** Keys from **age, GPG, or cloud KMS**. A `.env` file can stay in Git with secrets turned into ciphertext—the "secrets in the repo, but encrypted" approach . **Best for teams wanting encrypted secrets in versioned files** without a server-based vault. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Pulumi ESC](https://github.com/pulumi/esc)** | — | **Open-source (Apache 2.0) environments, secrets, and configuration manager with an open ecosystem approach.** **Pulls secrets from existing stores** (HashiCorp Vault, 1Password, AWS Secrets Manager) rather than acting as the sole vault—unlike Infisical, which stores secrets in its own store and syncs out . **Composable hierarchical environments** inherit values; **versioning with tags** allows importing specific collections of secrets . **Trade-off**: GUI editor lacks YAML support; less of a standalone vault and more of an orchestration layer . **Best for teams wanting to unify secrets across multiple existing stores** rather than migrate to a new one. |
| **[dotenv](https://github.com/motdotla/dotenv)** | — | **The ubiquitous Node.js `.env` file parser.** **Does not modify already-set variables**—collisions are skipped unless `override: true` is passed. Handles quotes, multiline values, backticks, and comments . **Best for local development**—not a replacement for a secret manager in production. |
| **[gitleaks](https://github.com/gitleaks/gitleaks)** | — | **Scans Git history and pull requests for leaked secrets.** **The piece most setups are missing**: a pre-commit hook or CI job that refuses to merge a commit containing a key . **Best for catching secrets before they reach production**—complements any secrets manager. |

**Frameworks for building custom systems**: Choose **Infisical** for an all-in-one open-source secrets platform with dynamic secrets and machine identity , **HashiCorp Vault** for enterprise-grade dynamic credentials and PKI at scale , or **dotenv-vault** for encrypted `.env` files that live safely in Git —all without per-secret or per-seat SaaS fees that compound across teams.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Secrets and variable management platforms handle credentials that grant access to critical systems; enforce strong authentication (MFA), least-privilege access, and **never commit plaintext secrets to version control**. A compromised secret store exposes every connected system.
- **Variable management spans a spectrum from simple `.env` parsing to enterprise vaults.** **Postman Variables** are scoped to API testing—collection/environment/global scopes for reuse across requests, with Postman Vault for local secrets . **Doppler and Infisical** provide runtime injection without writing secrets to disk . **HashiCorp Vault** adds dynamic secrets with automatic revocation—the gold standard for fleet-scale credential management, but operationally heavy . **dotenv-vault and SOPS** solve the "secrets in Git" problem by encrypting values while keeping files version-controlled . **Infisical has emerged as the leading open-source alternative to Vault**—28,832 stars, 15,000+ organizations, MIT licensed, and lighter to operate while covering secrets, PKI, scanning, and PAM in one platform . **Vaultwarden** is best for password storage, not application secrets. **Validate whether you need API-testing variables (Postman), encrypted files in Git (dotenv-vault, SOPS), runtime injection (Doppler, Infisical), or dynamic credentials (Vault)** before committing.

---

**Made for developers, platform engineers, and security teams managing configuration and secrets.**  
Let's make global and collection variable management more open, secure, and injection-first.
