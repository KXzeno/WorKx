---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
showDate: true
lastmod:
showDateUpdated: false
series: ["beKnighted, vol. 1"]
series_order: {{ .Name }}
draft: true
layout: "simple"
disqus_identifier: {{ $x := printf "%s" .Name }}{{ $y := sha256 $x }}{{ crypto.FNV32a $y }}
disqus_title: {{ replace .Name "-" " " | title }}
disqus_url: 'https://kaszworkx.netlify.app/chapters/{{ printf "%s" .Name | lower }}'
tags: ["beKnighted", "Chapter"]
showComments: true
publishDate:
---

