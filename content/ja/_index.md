---
title: ''
summary: 田畑玲穏の研究ポートフォリオ
date: 2026-05-26
type: landing

sections:
  - block: resume-biography-3
    content:
      username: me-ja
      text: |
        自律移動ロボットの環境認識と自律移動に取り組む大学院生です。
        LiDAR、カメラ、コンピュータビジョン、機械学習を組み合わせた
        ロボットシステムを研究しています。
      headings:
        about: 自己紹介
        interests: 研究分野
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

  - block: markdown
    id: research
    content:
      title: 研究
      text: |
        ## 移動ロボットのマルチモーダル環境認識

        3D LiDARとRGBカメラを用いた環境認識を研究しています。生成モデル
        によるLiDAR点群の高密度化を利用した画像・点群間の位置合わせや、
        車椅子型移動ロボットによるスロープ検出・自律誘導に取り組みました。
    design:
      columns: '1'

  - block: collection
    id: publications
    content:
      title: 研究業績
      filters:
        folders:
          - publications
    design:
      view: citation

  - block: collection
    content:
      title: 主なプロジェクト
      filters:
        folders:
          - projects
    design:
      view: article-grid
      columns: 3
      show_date: false
      show_read_time: false
---
