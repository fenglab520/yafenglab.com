---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        <span style="font-size:0.8em">  **Neuropsychiatric and Statistical Genomics Lab</span>**
      #image:
      #  filename: homepage_dna.png
      
      text: 
  - block: hero
    content:
      title: 
      image:
        filename: group_photo.png
      
      text: <span style="font-size:0.95em"> We are a computational research group dedicated to studying the genetic epidemiology and biology of human complex traits, with an emphasis on the susceptibility, severity, and progression of neuro-psychiatric disorders. Our work extends to analyses across diverse ancestries and multi-omics data, aiming to translate genomics research into better healthcare and public health outcomes. </span>
  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: compact
      columns: '1'

  # - block: markdown
  #   content:
  #     title:
  #     subtitle: ''
  #     text:
  #   design:
  #     columns: '1'
  #     background:
  #       image: 
  #         filename: coders.jpg
  #         filters:
  #           brightness: 1
  #         parallax: false
  #         position: center
  #         size: cover
  #         text_color_light: true
  #     spacing:
  #       padding: ['20px', '0', '20px', '0']
  #     css_class: fullscreen

  # - block: collection
  #   content:
  #     title: Latest Preprints
  #     text: ""
  #     count: 5
  #     filters:
  #       folders:
  #         - publication
  #       publication_type: 'article'
  #   design:
  #     view: citation
  #     columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
      
      
# html code for centering and adjusting text size
      #        <div style="text-align: center;">
      #    <span style="font-size:1.5em;align=center"> At the intersection of epidemiology and statistical genetics, our lab investigates the genetic basis of human complex traits, focusing on the susceptibility, severity, and progression of neuropsychiatric disorders. Our research extends to multi-omics methodologies and diverse ancestries, aiming to translate genomics research into improved healthcare and public health.
      #    </span>
      #  </div>

---
