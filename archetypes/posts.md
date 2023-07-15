---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
showDate: true
lastmod:
showDateUpdated: false
# series: [""]
draft: true
summary:
disqus_identifier: {{ $x := printf "%s" .Name }}{{ $y := sha256 $x }}{{ crypto.FNV32a $y }}
disqus_title: "{{ replace .Name "-" " " | title }}"
disqus_url: 'https://karnovah.com/posts/{{ printf "%s" .Name | lower }}'
showComments: true
tags: [""] 
---

