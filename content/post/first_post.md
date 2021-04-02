---
title: "First_post"
date: 2021-03-27T14:52:14+09:00
# draft: true
toc: true
math: true
tags: 
  - untagged
---

# マークダウン 記法
- 普通のリスト
- [ ] チェックリスト１
- [ ] チェックリスト２
  - 詳細１
  - 詳細２


## 画像
- `![]()`
  - ![first_post/logo.png](logo.png)

## 数式
```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

{{< math.inline >}}
<p>
Inline math: \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\)
</p>
{{</ math.inline >}}

Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$

