# xc-app-services-tf

XC application services in Terraform

Example of deploying Application Services in XC using Terraform.

- Load Balancer
  - IP Reputation
  - Dataguard
  - Source IP Stickiness
- WAF
  - Blocking
  - Default Detection
  - Default Bot
- Service Policy
  - Deny ASN
  - Deny Country List
  - Allow IPv4 Prefix
- Routes
  - Simple [iRule Replacement]
  - Redirect [iRule Replacement: HTTP::redirect]
  - Direct Response [iRule Replacement]
  - Custom
  - [HEADER] [iRule Replacement] Accept-Language Based Redirects
  - [HEADER] [iRule Replacement] WWW-Authenticate NTLM Killer
  - [Rewrites] [iRule Replacement] URI Rewriting
  - [Rewrites] [iRule Replacement] Manual Host Rewriting
  - [iRule Replacement: Pool Command] when HTTP_REQUEST { set uri [HTTP::uri] if { $uri ends_with ".gif" } { pool my_pool }
- Bot Standard
  - POST /login/ protection
  - GET / Web Scraping protection
- Rate Limiting
- Client Side Defense
- App Type & App Settings (ML)

## Usage

Map the VES P12 Password to ENV Var

```bash
. ./prep.sh
```

Deploy

```bash
terraform init
terraform plan
terraform apply
```

Destroy

```bash
terraform destroy
```
