---
title: RFFFF语录
layout: gallery-home
---

欢迎来到我们的图片画廊！这里展示了精选的图片集合，每次刷新都会随机显示40张不同的图片。

点击任意图片可以将其复制到剪贴板，方便您保存和分享。

## 图片索引

以下是画廊中所有可用的图片：

{{- $quotesDir := "static/quotes-images" -}}
{{- if fileExists $quotesDir -}}
  {{- range (readDir $quotesDir) -}}
    {{- if and (not .IsDir) (or (strings.HasSuffix .Name ".jpg") (strings.HasSuffix .Name ".jpeg") (strings.HasSuffix .Name ".png") (strings.HasSuffix .Name ".webp") (strings.HasSuffix .Name ".gif")) -}}
- **{{ .Name }}** - {{ strings.TrimSuffix (path.Ext .Name) .Name | humanize }}
    {{- end -}}
  {{- end -}}
{{- else -}}
画廊图片加载中...
{{- end -}}

这些图片文件名包含各种有趣的表情和文字，您可以通过搜索功能快速找到特定的图片。搜索支持中文文件名和表情符号。