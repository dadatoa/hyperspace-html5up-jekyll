---
layout: home2
sections :
# intro : layout hard coded from config info, should not be modified unless you know what you are doing
    - id: intro
      title: welcome
      template: intro
# one
    - id: one
      title: who we are
      template: posts-list
      #show-title: false 
      color-style: style2
      animate: spotlights
      source: posts
# two
    - id: two
      title: what we do
      template: features-list
      #show-title: true
      color-style: style3
      animate: fade-up
      source: pages
      description: Phasellus convallis elit id ullamcorper pulvinar. Duis aliquam turpis mauris, eu ultricies erat malesuada quis. Aliquam dapibus, lacus eget hendrerit bibendum, urna est aliquam sem, sit amet imperdiet est velit quis lorem.
# three 
    - id: three
      html_id: three
      title: get in touch
      template: follow-me #contact-form or change to follow-me if you just want to make contact info appear with email-me button
      color-style: style1
      animate: fade-up
      description: Phasellus convallis elit id ullamcorper pulvinar. Duis aliquam turpis mauris, eu ultricies erat malesuada quis. Aliquam dapibus, lacus eget hendrerit bibendum, urna est aliquam sem, sit amet imperdiet est velit quis lorem.
---