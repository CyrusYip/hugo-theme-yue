{{- $fileContentBaseName := .File.ContentBaseName -}}
---
title: {{ replace $fileContentBaseName "-" " " | title }}
slug: {{ $fileContentBaseName | lower }}
date: {{ .Date }}
tags:
  - tag1
categories:
  - category1
draft: true # Remove this line if your post is ready to be published
---
