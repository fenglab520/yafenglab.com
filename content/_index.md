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
        filename: group_photo.jpeg
      
      text: <span style="font-size:0.95em"> We are a computational research group [@NTU](https://www.ntu.edu.tw) dedicated to studying the genetic epidemiology and biology of human complex traits, with an emphasis on the susceptibility, severity, and progression of neuro-psychiatric disorders. Our work extends to analyses across diverse ancestries and multi-omics data, aiming to translate genomics research into better healthcare and public health outcomes. </span>
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
      title: Lab Life & Events
      subtitle:
      text: |
        <style>
        div.gallery-grid{display:flex;flex-wrap:nowrap;overflow-x:auto;grid-template-columns:none;grid-auto-rows:auto;gap:14px;grid-gap:14px;scroll-behavior:smooth;scroll-snap-type:x proximity;padding-bottom:10px;}
        div.gallery-item{flex:0 0 auto;width:270px;height:190px;grid-row-end:auto;grid-column-end:auto;scroll-snap-align:start;border-radius:8px;}
        .film-wrap{position:relative;}
        .film-nav{position:absolute;top:calc(50% - 5px);transform:translateY(-50%);z-index:5;border:none;width:42px;height:42px;border-radius:50%;background:rgba(0,0,0,.55);color:#fff;font-size:1.6rem;line-height:1;cursor:pointer;}
        .film-nav:hover{background:rgba(0,0,0,.8);}
        .film-prev{left:-8px;}
        .film-next{right:-8px;}
        @media(max-width:600px){.film-nav{display:none;}}
        </style>

        {{< gallery album="events" >}}

        <script>
        (function(){var g=document.querySelector('.gallery-grid');if(!g||g.dataset.filmstrip)return;g.dataset.filmstrip=1;var w=document.createElement('div');w.className='film-wrap';g.parentNode.insertBefore(w,g);w.appendChild(g);function mk(c,t,d){var b=document.createElement('button');b.type='button';b.className='film-nav '+c;b.textContent=t;b.setAttribute('aria-label',d>0?'Scroll right':'Scroll left');b.addEventListener('click',function(){g.scrollBy({left:d*g.clientWidth*0.8,behavior:'smooth'});});w.appendChild(b);}mk('film-prev','‹',-1);mk('film-next','›',1);})();
        </script>
    design:
      columns: '1'
      
      
# html code for centering and adjusting text size
      #        <div style="text-align: center;">
      #    <span style="font-size:1.5em;align=center"> At the intersection of epidemiology and statistical genetics, our lab investigates the genetic basis of human complex traits, focusing on the susceptibility, severity, and progression of neuropsychiatric disorders. Our research extends to multi-omics methodologies and diverse ancestries, aiming to translate genomics research into improved healthcare and public health.
      #    </span>
      #  </div>

---
