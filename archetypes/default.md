{{- $fileContentBaseName := .File.ContentBaseName -}}
---
title: {{ replace $fileContentBaseName "-" " " | title }}
slug: {{ $fileContentBaseName | lower }}
date: {{ .Date }}
# lastmod: {{ .Date }} # Last modification date
tags:
  - tag1
categories:
  - category1
# draft: true
---
