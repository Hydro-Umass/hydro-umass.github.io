---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: markdown
    content:
      title: '<span style="color:  #fbfcfc;">Computational Hydrology Research Group at the University of Massachusetts Amherst</span>'
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image:
          filename: flooding.jpg
          filters:
            brightness: 0.8
          parallax: true
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']

  - block: markdown
    content:
      title:
      text: |
        **Welcome to Hydro@UMass!**

        This is the webpage of the Computational hydrology Research Group in the Civil and Environmental Engineering department at the University of Massachusetts Amherst. The group is led by Kostas Andreadis, and the research that we do focuses on the intersection of water resources modeling, remote sensing and in-situ observations, data fusion, and the study of large-scale hydrology as it relates to climate change and environmental monitoring.

  - block: slider
    content:
      slides:
      - title: Computational Hydrology Research
        content: Take a look at what we're working on...
        align: center
        background:
          image:
            filename: watercycle.jpg
            filters:
              brightness: 0.7
          position: right
          color: '#666'
      - title: Remote Sensing
        content: 'We study the use of remote sensing (both satellite and airborne) to monitor freshwater resources globally.'
        align: left
        background:
          image:
            filename: swot.jpg
            filters:
              brightness: 0.7
          position: center
          color: '#555'
      - title: Modeling
        content: 'We develop and implement numerical models to better understand hydrologic processes at multiple scales, and software tools to facilitate their use in applications.'
        align: right
        background:
          image:
            filename: modeling.jpg
            filters:
              brightness: 0.7
          position: center
          color: '#333'
      - title: Data Science
        content: 'We develop data assimilation and machine learning algorithms to integrate models and observations for improving hydrologic prediction and uncertainty characterization.'
        align: left
        background:
          image:
            filename: datascience.jpg
            filters:
              brightness: 0.7
          position: center
          color: '#333'
    design:
      # Slide height is automatic unless you force a specific height (e.g. '400px')
      slide_height: '400px'
      is_fullscreen: false
      # Automatically transition through slides?
      loop: true
      # Duration of transition between slides (in ms)
      interval: 3000

  - block: markdown
    content:
      title: About us
      subtitle:
      text: |
        We are a team of motivated and ambitious scientists and engineers exploring the use of computational technologies for better understanding water availability globally. We strive to excel professionally but also prioritize a balanced, collaborative and supportive environment. We are strongly committed to mentoring and providing opportunities through our links to other research groups within the University of Massachusetts Amherst and other institutions around the world. Our research spans a wide range of topics about water resources engineering and science, and our [current projects]({{< relref "/projects" >}}) should give you a general idea about us.
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
      spacing:
        # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['40px', '0', '0', '0']

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
      page_type: news
    design:
      view: compact
      columns: '1'

  - block: collection
    content:
      title: Recent Publications
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: true
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: publication
    design:
      view: compact
      columns: '1'

---
