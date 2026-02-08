---
title: "python pip vs pipx"
date: 2026-01-25
categories: 
  - "fsse"
---

pip vs pipx

```
PIP
    /home/cdarra/.local/bin/uv
    /home/cdarra/.local/bin/uvx
    /home/cdarra/.local/lib/python3.13/site-packages/uv-0.9.26.dist-info/*
    /home/cdarra/.local/lib/python3.13/site-packages/uv/*

PIPX
    /home/cdarra/.local/bin/uv
    /home/cdarra/.local/bin/uvx
    uv -> /home/cdarra/.local/share/pipx/venvs/uv/bin/uv
    uvx -> /home/cdarra/.local/share/pipx/venvs/uv/bin/uvx
    /home/cdarra/.local/share/pipx/venvs/uv/lib/python3.13/site-packages/uv
    /home/cdarra/.local/share/pipx/venvs/uv/lib/python3.13/site-packages/uv-0.9.26.dist-info

```
