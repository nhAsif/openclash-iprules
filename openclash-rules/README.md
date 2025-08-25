# OpenClash Compatible IP Range Rules

This directory contains IP range rules converted from multiple repositories to OpenClash-compatible YAML format.

## Sources

- [ipranges repository](https://github.com/lord-alfred/ipranges) - Various service IP ranges
- [YouTube IP list](https://github.com/touhidurrr/iplist-youtube) - YouTube IP ranges (IPv4, IPv6, CIDR)
- [IP-Prefix-List](https://github.com/sakib-m/IP-Prefix-List) - IP prefixes for many companies

## Usage

Add these rule providers to your OpenClash configuration:

```yaml
rule-providers:
  # Example for Facebook IPs (from ipranges repository)
  facebook-ip:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-REPO/main/openclash-rules/ipranges/facebook-ipv4.yaml"
    path: ./ruleset/facebook-ip.yaml
    interval: 86400  # 24 hours

  # Example for YouTube IPv4 (from YouTube repository)
  youtube-ipv4:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-REPO/main/openclash-rules/youtube/ipv4.yaml"
    path: ./ruleset/youtube-ipv4.yaml
    interval: 86400  # 24 hours

  # Example for YouTube IPv6 (from YouTube repository)
  youtube-ipv6:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-REPO/main/openclash-rules/youtube/ipv6.yaml"
    path: ./ruleset/youtube-ipv6.yaml
    interval: 86400  # 24 hours
```

Then use in rules:
```yaml
rules:
  - RULE-SET,facebook-ip,DIRECT
  - RULE-SET,youtube-ipv4,DIRECT
  - RULE-SET,youtube-ipv6,DIRECT
```

## Files

- `ipranges/googlebot-ipv6_merged.yaml` - IPRANGES GOOGLEBOT ipv6_merged IP ranges
- `ipranges/googlebot-ipv4.yaml` - IPRANGES GOOGLEBOT ipv4 IP ranges
- `ipranges/googlebot-ipv6.yaml` - IPRANGES GOOGLEBOT ipv6 IP ranges
- `ipranges/googlebot-ipv4_merged.yaml` - IPRANGES GOOGLEBOT ipv4_merged IP ranges
- `ipranges/protonvpn-ipv4.yaml` - IPRANGES PROTONVPN ipv4 IP ranges
- `ipranges/protonvpn-ipv4_merged.yaml` - IPRANGES PROTONVPN ipv4_merged IP ranges
- `ipranges/microsoft-ipv6_merged.yaml` - IPRANGES MICROSOFT ipv6_merged IP ranges
- `ipranges/microsoft-ipv4.yaml` - IPRANGES MICROSOFT ipv4 IP ranges
- `ipranges/microsoft-ipv6.yaml` - IPRANGES MICROSOFT ipv6 IP ranges
- `ipranges/microsoft-ipv4_merged.yaml` - IPRANGES MICROSOFT ipv4_merged IP ranges
- `ipranges/digitalocean-ipv6_merged.yaml` - IPRANGES DIGITALOCEAN ipv6_merged IP ranges
- `ipranges/digitalocean-ipv4.yaml` - IPRANGES DIGITALOCEAN ipv4 IP ranges
- `ipranges/digitalocean-ipv6.yaml` - IPRANGES DIGITALOCEAN ipv6 IP ranges
- `ipranges/digitalocean-ipv4_merged.yaml` - IPRANGES DIGITALOCEAN ipv4_merged IP ranges
- `ipranges/apple-proxy-ipv6_merged.yaml` - IPRANGES APPLE-PROXY ipv6_merged IP ranges
- `ipranges/apple-proxy-ipv4.yaml` - IPRANGES APPLE-PROXY ipv4 IP ranges
- `ipranges/apple-proxy-ipv6.yaml` - IPRANGES APPLE-PROXY ipv6 IP ranges
- `ipranges/apple-proxy-ipv4_merged.yaml` - IPRANGES APPLE-PROXY ipv4_merged IP ranges
- `ipranges/vultr-ipv6_merged.yaml` - IPRANGES VULTR ipv6_merged IP ranges
- `ipranges/vultr-ipv4.yaml` - IPRANGES VULTR ipv4 IP ranges
- `ipranges/vultr-ipv6.yaml` - IPRANGES VULTR ipv6 IP ranges
- `ipranges/vultr-ipv4_merged.yaml` - IPRANGES VULTR ipv4_merged IP ranges
- `ipranges/cloudflare-ipv6_merged.yaml` - IPRANGES CLOUDFLARE ipv6_merged IP ranges
- `ipranges/cloudflare-ipv4.yaml` - IPRANGES CLOUDFLARE ipv4 IP ranges
- `ipranges/cloudflare-ipv6.yaml` - IPRANGES CLOUDFLARE ipv6 IP ranges
- `ipranges/cloudflare-ipv4_merged.yaml` - IPRANGES CLOUDFLARE ipv4_merged IP ranges
- `ipranges/twitter-ipv6_merged.yaml` - IPRANGES TWITTER ipv6_merged IP ranges
- `ipranges/twitter-ipv4.yaml` - IPRANGES TWITTER ipv4 IP ranges
- `ipranges/twitter-ipv6.yaml` - IPRANGES TWITTER ipv6 IP ranges
- `ipranges/twitter-ipv4_merged.yaml` - IPRANGES TWITTER ipv4_merged IP ranges
- `ipranges/github-ipv6_merged.yaml` - IPRANGES GITHUB ipv6_merged IP ranges
- `ipranges/github-ipv4.yaml` - IPRANGES GITHUB ipv4 IP ranges
- `ipranges/github-ipv6.yaml` - IPRANGES GITHUB ipv6 IP ranges
- `ipranges/github-ipv4_merged.yaml` - IPRANGES GITHUB ipv4_merged IP ranges
- `ipranges/linode-ipv6_merged.yaml` - IPRANGES LINODE ipv6_merged IP ranges
- `ipranges/linode-ipv4.yaml` - IPRANGES LINODE ipv4 IP ranges
- `ipranges/linode-ipv6.yaml` - IPRANGES LINODE ipv6 IP ranges
- `ipranges/linode-ipv4_merged.yaml` - IPRANGES LINODE ipv4_merged IP ranges
- `ipranges/bing-ipv4.yaml` - IPRANGES BING ipv4 IP ranges
- `ipranges/bing-ipv4_merged.yaml` - IPRANGES BING ipv4_merged IP ranges
- `ipranges/oracle-ipv4.yaml` - IPRANGES ORACLE ipv4 IP ranges
- `ipranges/oracle-ipv4_merged.yaml` - IPRANGES ORACLE ipv4_merged IP ranges
- `ipranges/google-ipv6_merged.yaml` - IPRANGES GOOGLE ipv6_merged IP ranges
- `ipranges/google-ipv4.yaml` - IPRANGES GOOGLE ipv4 IP ranges
- `ipranges/google-ipv6.yaml` - IPRANGES GOOGLE ipv6 IP ranges
- `ipranges/google-ipv4_merged.yaml` - IPRANGES GOOGLE ipv4_merged IP ranges
- `ipranges/all-ipv6_merged.yaml` - IPRANGES ALL ipv6_merged IP ranges
- `ipranges/all-ipv4.yaml` - IPRANGES ALL ipv4 IP ranges
- `ipranges/all-ipv6.yaml` - IPRANGES ALL ipv6 IP ranges
- `ipranges/all-ipv4_merged.yaml` - IPRANGES ALL ipv4_merged IP ranges
- `ipranges/telegram-ipv6_merged.yaml` - IPRANGES TELEGRAM ipv6_merged IP ranges
- `ipranges/telegram-ipv4.yaml` - IPRANGES TELEGRAM ipv4 IP ranges
- `ipranges/telegram-ipv6.yaml` - IPRANGES TELEGRAM ipv6 IP ranges
- `ipranges/telegram-ipv4_merged.yaml` - IPRANGES TELEGRAM ipv4_merged IP ranges
- `ipranges/openai-ipv4.yaml` - IPRANGES OPENAI ipv4 IP ranges
- `ipranges/openai-ipv4_merged.yaml` - IPRANGES OPENAI ipv4_merged IP ranges
- `ipranges/facebook-ipv6_merged.yaml` - IPRANGES FACEBOOK ipv6_merged IP ranges
- `ipranges/facebook-ipv4.yaml` - IPRANGES FACEBOOK ipv4 IP ranges
- `ipranges/facebook-ipv6.yaml` - IPRANGES FACEBOOK ipv6 IP ranges
- `ipranges/facebook-ipv4_merged.yaml` - IPRANGES FACEBOOK ipv4_merged IP ranges
- `ipranges/amazon-ipv6_merged.yaml` - IPRANGES AMAZON ipv6_merged IP ranges
- `ipranges/amazon-ipv4.yaml` - IPRANGES AMAZON ipv4 IP ranges
- `ipranges/amazon-ipv6.yaml` - IPRANGES AMAZON ipv6 IP ranges
- `ipranges/amazon-ipv4_merged.yaml` - IPRANGES AMAZON ipv4_merged IP ranges
- `ipranges/perplexity-ipv4.yaml` - IPRANGES PERPLEXITY ipv4 IP ranges
- `ipranges/perplexity-ipv4_merged.yaml` - IPRANGES PERPLEXITY ipv4_merged IP ranges
- `youtube/cidr6.yaml` - YOUTUBE  cidr6 IP ranges
- `youtube/ipv4.yaml` - YOUTUBE  ipv4 IP ranges
- `youtube/ipv6.yaml` - YOUTUBE  ipv6 IP ranges
- `youtube/cidr4.yaml` - YOUTUBE  cidr4 IP ranges
- `ip-prefix-list/AWS_EC2-only_ip_blocks.yaml` - IP-PREFIX-LIST AWS_EC2 only_ip_blocks IP ranges
- `ip-prefix-list/IMO_PageBites-only_ip_blocks.yaml` - IP-PREFIX-LIST IMO_PAGEBITES only_ip_blocks IP ranges
- `ip-prefix-list/MICROSOFT-only_ip_blocks.yaml` - IP-PREFIX-LIST MICROSOFT only_ip_blocks IP ranges
- `ip-prefix-list/NETFLIX-only_ip_blocks.yaml` - IP-PREFIX-LIST NETFLIX only_ip_blocks IP ranges
- `ip-prefix-list/FREE-FIRE_GARENA-only_ip_blocks.yaml` - IP-PREFIX-LIST FREE-FIRE_GARENA only_ip_blocks IP ranges
- `ip-prefix-list/BIGO-only_ip_blocks.yaml` - IP-PREFIX-LIST BIGO only_ip_blocks IP ranges
- `ip-prefix-list/FACEBOOK-only_ip_blocks.yaml` - IP-PREFIX-LIST FACEBOOK only_ip_blocks IP ranges
- `ip-prefix-list/AMAZON-only_ip_blocks.yaml` - IP-PREFIX-LIST AMAZON only_ip_blocks IP ranges
- `ip-prefix-list/GOOGLE-only_ip_blocks.yaml` - IP-PREFIX-LIST GOOGLE only_ip_blocks IP ranges
- `ip-prefix-list/FASTLY-only_ip_blocks.yaml` - IP-PREFIX-LIST FASTLY only_ip_blocks IP ranges
- `ip-prefix-list/CDN77-only_ip_blocks.yaml` - IP-PREFIX-LIST CDN77 only_ip_blocks IP ranges
- `ip-prefix-list/AWS_S3-only_ip_blocks.yaml` - IP-PREFIX-LIST AWS_S3 only_ip_blocks IP ranges
- `ip-prefix-list/AKAMAI-only_ip_blocks.yaml` - IP-PREFIX-LIST AKAMAI only_ip_blocks IP ranges
- `ip-prefix-list/LINODE-only_ip_blocks.yaml` - IP-PREFIX-LIST LINODE only_ip_blocks IP ranges
- `ip-prefix-list/ZOOM-only_ip_blocks.yaml` - IP-PREFIX-LIST ZOOM only_ip_blocks IP ranges
- `ip-prefix-list/DIGITALOCEAN-only_ip_blocks.yaml` - IP-PREFIX-LIST DIGITALOCEAN only_ip_blocks IP ranges
- `ip-prefix-list/ZENLAYER-only_ip_blocks.yaml` - IP-PREFIX-LIST ZENLAYER only_ip_blocks IP ranges
- `ip-prefix-list/TELEGRAM-only_ip_blocks.yaml` - IP-PREFIX-LIST TELEGRAM only_ip_blocks IP ranges
- `ip-prefix-list/AWS_CLOUDFRONT-only_ip_blocks.yaml` - IP-PREFIX-LIST AWS_CLOUDFRONT only_ip_blocks IP ranges
- `ip-prefix-list/GOOGLE_CLOUD-only_ip_blocks.yaml` - IP-PREFIX-LIST GOOGLE_CLOUD only_ip_blocks IP ranges
- `ip-prefix-list/VALVE-only_ip_blocks.yaml` - IP-PREFIX-LIST VALVE only_ip_blocks IP ranges
- `ip-prefix-list/PUBG_TENCENT-only_ip_blocks.yaml` - IP-PREFIX-LIST PUBG_TENCENT only_ip_blocks IP ranges
- `ip-prefix-list/CLOUDFLARE-only_ip_blocks.yaml` - IP-PREFIX-LIST CLOUDFLARE only_ip_blocks IP ranges
- `ip-prefix-list/ALIBABA-only_ip_blocks.yaml` - IP-PREFIX-LIST ALIBABA only_ip_blocks IP ranges

*Last updated: 2025-08-25T12:31:39.739353Z*
*Total files converted: 94*
