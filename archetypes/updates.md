---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
showDate: true
lastmod: 
showDateUpdated: false
# series: [""]
draft: true
disqus_identifier: {{ $x := printf "%s" .Name }}{{ $y := sha256 $x }}{{ crypto.FNV32a $y }}
disqus_title: "{{ replace .Name "-" " " | title }}"
disqus_url: 'https://karnovah.com/updates/{{$name := printf "%s" .Name}}{{ urlize $name | lower }}'
showComments: true
tags: ["Updates"]
---

