---
title: ''
summary: Research portfolio of Reon Tabata
date: 2026-05-26
type: landing

sections:
  - block: resume-biography-3
    content:
      username: me
      text: |
        I am a graduate researcher working on environmental perception and
        autonomous navigation for mobile robots. My research combines LiDAR,
        cameras, computer vision, and machine learning.
      headings:
        about: About
        interests: Research Interests
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
      title: Research
      text: |
        ## Multimodal perception for mobile robots

        I study environmental perception using 3D LiDAR and RGB cameras. My
        work includes image-to-point-cloud registration using generative
        LiDAR upsampling, and slope detection and autonomous guidance for a
        wheelchair-type mobile robot.
    design:
      columns: '1'

  - block: collection
    id: publications
    content:
      title: Publications
      filters:
        folders:
          - publications
    design:
      view: citation

  - block: collection
    content:
      title: Selected Projects
      filters:
        folders:
          - projects
    design:
      view: article-grid
      columns: 3
      show_date: false
      show_read_time: false
---
