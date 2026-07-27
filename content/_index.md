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
      
      text: <span style="font-size:0.95em"> We are a computational research group at [National Taiwan University](https://www.ntu.edu.tw) dedicated to studying the genetic epidemiology of human complex traits, with a focus on the susceptibility, severity, and progression of neuro-psychiatric disorders. Our work extends to analyses across diverse ancestries and multi-omics data, aiming to translate genomic discoveries into better healthcare and public health outcomes. </span>
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
      view: minimal
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
      title: Lab Life
      subtitle:
      text: |
        <style>
        div.gallery-grid{display:flex;flex-wrap:nowrap;overflow-x:auto;grid-template-columns:none;grid-auto-rows:auto;gap:14px;grid-gap:14px;padding-bottom:10px;scrollbar-width:thin;}
        div.gallery-item{flex:0 0 auto;width:270px;height:190px;grid-row-end:auto;grid-column-end:auto;border-radius:8px;}
        .film-wrap{position:relative;}
        .film-nav{position:absolute;top:calc(50% - 5px);transform:translateY(-50%);z-index:5;border:none;width:42px;height:42px;border-radius:50%;background:rgba(0,0,0,.55);color:#fff;font-size:1.6rem;line-height:1;cursor:pointer;}
        .film-nav:hover{background:rgba(0,0,0,.8);}
        .film-prev{left:-8px;}
        .film-next{right:-8px;}
        @media(max-width:600px){.film-nav{display:none;}}
        </style>

        {{< gallery album="events" >}}

        <script>
        (function(){var g=document.querySelector('.gallery-grid');if(!g||g.dataset.loop)return;g.dataset.loop=1;var w=document.createElement('div');w.className='film-wrap';g.parentNode.insertBefore(w,g);w.appendChild(g);var reals=[].slice.call(g.children);var N=reals.length;function mk(c,t,d){var b=document.createElement('button');b.type='button';b.className='film-nav '+c;b.textContent=t;b.setAttribute('aria-label',d>0?'Scroll right':'Scroll left');b.addEventListener('click',function(){g.scrollBy({left:d*Math.min(g.clientWidth*0.8,560),behavior:'smooth'});});w.appendChild(b);}if(N>1){function cl(it,i){var c=it.cloneNode(true);var a=c.querySelector('a');if(a){a.removeAttribute('data-fancybox');a.addEventListener('click',function(e){e.preventDefault();var ra=reals[i].querySelector('a');if(ra)ra.click();});}return c;}var f1=document.createDocumentFragment(),f2=document.createDocumentFragment();reals.forEach(function(it,i){f1.appendChild(cl(it,i));});reals.forEach(function(it,i){f2.appendChild(cl(it,i));});g.insertBefore(f1,reals[0]);g.appendChild(f2);var one=0;function measure(){one=reals[0].offsetLeft-g.children[0].offsetLeft;}function center(){measure();if(one>0)g.scrollLeft=one;}center();setTimeout(center,300);window.addEventListener('load',center);window.addEventListener('resize',center);var tick=false;g.addEventListener('scroll',function(){if(tick)return;tick=true;requestAnimationFrame(function(){if(one>0){if(g.scrollLeft<one*0.5)g.scrollLeft+=one;else if(g.scrollLeft>one*1.5)g.scrollLeft-=one;}tick=false;});});}mk('film-prev','‹',-1);mk('film-next','›',1);})();
        </script>
    design:
      columns: '1'
      
      
# html code for centering and adjusting text size
      #        <div style="text-align: center;">
      #    <span style="font-size:1.5em;align=center"> At the intersection of epidemiology and statistical genetics, our lab investigates the genetic basis of human complex traits, focusing on the susceptibility, severity, and progression of neuropsychiatric disorders. Our research extends to multi-omics methodologies and diverse ancestries, aiming to translate genomics research into improved healthcare and public health.
      #    </span>
      #  </div>

---
