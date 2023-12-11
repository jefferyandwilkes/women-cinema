---
# Leave the homepage title empty to use the site title
title: Partners
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Women in Italian Cinema
      image:
        filename: about.jpg
      text: |
        <br>

       The Cineteca di Bologna is one of Europe’s leading film institutions. Founded in the 1960s as an arm of the municipality of Bologna’s 
       cinema commission, the Cineteca today is comprised of cinemas, archives, a library, film laboratories, publishing activities, and an 
       annual film festival (Il cinema Ritrovato). Since it moved to its present premises in 2000, it has become a miniature city of cinema, 
       one of the most innovative and prestigious centres for the preservation, study and promotion of film heritage. Under its director, 
       Gianluca Farinelli, the Cineteca has built an enviable international reputation while developing its local links. It was a partner on 
       Stephen Gundle’s earlier research project on ‘Producers and Production Practices in the History of Italian Cinema, 1949-1976’.	
  
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
      view: card
      columns: '1'
  
  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image: 
          filename: coders.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen
  
  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
---
