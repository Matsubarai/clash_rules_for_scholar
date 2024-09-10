# clash_rules_for_scholar

### NOTE: We fix this YAML config behavior from `classical` to `domain` now. It's working on Clash Verge.

提供了一些和学术相关的网址以方便分流。对于大部分学术网站来说，需要使用订阅了相关权限的学校 ip 访问才能获得完整的内容。



## 订阅链接:



建议中国大陆地区使用 `cdn.jsdelivr.net` 的 CDN:



地址如下:



**scholar.yaml**: 一些学术网站

- [https://cdn.jsdelivr.net/gh/Matsubarai/clash_rules_for_scholar@0.1/rules/scholar.yaml](https://cdn.jsdelivr.net/gh/nerdneilsfield/clash_rules_for_scholar@0.1/rules/scholar.yaml)



## 使用方法

需要使用 [clash-premium](https://github.com/Dreamacro/clash/releases/tag/premium) 使用。如果有多个不同的代理提供商需要整合在一起，推荐使用作者的另外一个基于标签的多提供商管理工具 [nerdneilsfield/clash-tools: A tag based multi-upstream clash configuration generator (github.com)](https://github.com/nerdneilsfield/clash-tools)



添加如下的 provider-set:



```yaml
rule-providers:
  scholar:
    behavior: domain
    type: http
    url: "https://cdn.jsdelivr.net/gh/Matsubarai/clash_rules_for_scholar@0.1/rules/scholar.yaml"
    interval: 86400
    path: ./ruleset/scholar.yaml
```



在 `rules` 下面添加:

```yaml
- RULE-SET, scholar, DIRECT
```

