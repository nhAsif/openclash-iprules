# OpenClash Compatible IP Range Rules

This directory contains IP range rules converted from the [ipranges repository](https://github.com/lord-alfred/ipranges) to OpenClash-compatible YAML format.

## Usage

Add these rule providers to your OpenClash configuration:

```yaml
rule-providers:
  country-name:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-REPO/main/openclash-rules/COUNTRY.yaml"
    path: ./ruleset/country-name.yaml
    interval: 43200  # 12 hours
```

Then use in rules:
```yaml
rules:
  - RULE-SET,country-name,DIRECT
```

## Files

- `googlebot-ipv4.yaml` - GOOGLEBOT ipv4 IP ranges
- `googlebot-ipv4_merged.yaml` - GOOGLEBOT ipv4_merged IP ranges
- `protonvpn-ipv4.yaml` - PROTONVPN ipv4 IP ranges
- `protonvpn-ipv4_merged.yaml` - PROTONVPN ipv4_merged IP ranges
- `microsoft-ipv4.yaml` - MICROSOFT ipv4 IP ranges
- `microsoft-ipv4_merged.yaml` - MICROSOFT ipv4_merged IP ranges
- `digitalocean-ipv4.yaml` - DIGITALOCEAN ipv4 IP ranges
- `digitalocean-ipv4_merged.yaml` - DIGITALOCEAN ipv4_merged IP ranges
- `apple-proxy-ipv4.yaml` - APPLE-PROXY ipv4 IP ranges
- `apple-proxy-ipv4_merged.yaml` - APPLE-PROXY ipv4_merged IP ranges
- `vultr-ipv4.yaml` - VULTR ipv4 IP ranges
- `vultr-ipv4_merged.yaml` - VULTR ipv4_merged IP ranges
- `cloudflare-ipv4.yaml` - CLOUDFLARE ipv4 IP ranges
- `cloudflare-ipv4_merged.yaml` - CLOUDFLARE ipv4_merged IP ranges
- `twitter-ipv4.yaml` - TWITTER ipv4 IP ranges
- `twitter-ipv4_merged.yaml` - TWITTER ipv4_merged IP ranges
- `github-ipv4.yaml` - GITHUB ipv4 IP ranges
- `github-ipv4_merged.yaml` - GITHUB ipv4_merged IP ranges
- `linode-ipv4.yaml` - LINODE ipv4 IP ranges
- `linode-ipv4_merged.yaml` - LINODE ipv4_merged IP ranges
- `bing-ipv4.yaml` - BING ipv4 IP ranges
- `bing-ipv4_merged.yaml` - BING ipv4_merged IP ranges
- `oracle-ipv4.yaml` - ORACLE ipv4 IP ranges
- `oracle-ipv4_merged.yaml` - ORACLE ipv4_merged IP ranges
- `google-ipv4.yaml` - GOOGLE ipv4 IP ranges
- `google-ipv4_merged.yaml` - GOOGLE ipv4_merged IP ranges
- `all-ipv4.yaml` - ALL ipv4 IP ranges
- `all-ipv4_merged.yaml` - ALL ipv4_merged IP ranges
- `telegram-ipv4.yaml` - TELEGRAM ipv4 IP ranges
- `telegram-ipv4_merged.yaml` - TELEGRAM ipv4_merged IP ranges
- `openai-ipv4.yaml` - OPENAI ipv4 IP ranges
- `openai-ipv4_merged.yaml` - OPENAI ipv4_merged IP ranges
- `facebook-ipv4.yaml` - FACEBOOK ipv4 IP ranges
- `facebook-ipv4_merged.yaml` - FACEBOOK ipv4_merged IP ranges
- `amazon-ipv4.yaml` - AMAZON ipv4 IP ranges
- `amazon-ipv4_merged.yaml` - AMAZON ipv4_merged IP ranges
- `perplexity-ipv4.yaml` - PERPLEXITY ipv4 IP ranges
- `perplexity-ipv4_merged.yaml` - PERPLEXITY ipv4_merged IP ranges

*Last updated: 2025-08-20T18:22:24.172574Z*
*Total files converted: 38*
