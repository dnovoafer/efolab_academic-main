---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: hero
    demo: false # Only display this section in the Hugo Blox Builder demo site
    content:
      title: '**Welcome to the website of the <br> Extreme Fibre Optics Lab**'
      text: |-
              **Explore our [research interests](#projects) and [publications](#publication)**
    design:
      background:
       image:
       # Name of image in `assets/media/`.
        filename: Frontpage_picture.png
        # Apply image filters?
       filters:
         # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
          brightness: 1
        #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
       size: cover
       # Image focal point. Options include `left`, `center` (default), or `right`.
       position: center
       # Use a fun parallax-like fixed background effect on desktop? true/false
       parallax: true
      # Text color (true=light, false=dark, or remove for the dynamic theme color).
       text_color_light: true
      spacing:
        # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['20px', '0', '500px', '0']
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      spacing:
      # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['0px', '0', '20px', '0']
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Ikerbasque Research Fellow and Visiting Professor
          company: University of the Basque Country (UPV/EHU)
          company_url: ''
          location: Spain
          date_start: '2021-04-01'
          date_end: ''
          description: ''
        - title: W2 Associate Research Professor
          company: Max Planck Institute for the Science of Light
          company_url: ''
          location: Germany
          date_start: '2017-08-01'
          date_end: '2021-03-31'
          description: Group Leader in the Russell division. Supervisor of 6 PhD students to completion
        - title: Postdoctoral scientist
          company: Max Planck Institute for the Science of Light
          company_url: ''
          location: Germany
          date_start: '2013-01-01'
          date_end: '2017-07-31'
          description: ''
        - title: Postdoctoral researcher
          company: CLPU – Centro de Láseres Pulsados
          company_url: ''
          location: Spain
          date_start: '2011-09-01'
          date_end: '2012-12-31'
          description: ''     
        - title: Invited Professor
          company: University of Vigo
          company_url: ''
          location: Spain
          date_start: '2008-06-01'
          date_end: '2010-06-01'
          description: Taught Optics, Quantum Physics and Classical Electrodynamics
    design:
      columns: '2'
  - block: people
    id: people
    content:
      title: Meet the EFO Team
      filters:
        folders:
          - people
      # Choose which groups/teams of users to display.
      #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
      user_groups:
          - Head of the EFO-Lab
          - Researchers
          - PhD Students
          - Administration
          - Visitors
          - Alumni
      sort_by: Params.last_name
      sort_ascending: true
    design:
      show_interests: false
      show_role: true
      show_social: true
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Deep Learning
          tag: Deep Learning
        - name: Other
          tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: markdown
    content:
      title: Gallery
      subtitle: ''
      text: |-
        {{< gallery album="demo" >}}
    design:
      columns: '1'
  - block: collection
    id: publication
    content:
      title: Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam mi diam, venenatis ut magna et, vehicula efficitur enim.
      # Contact (add or remove contact options as necessary)
      email: test@example.org
      phone: 888 888 88 88
      appointment_url: 'https://calendly.com'
      address:
        street: 450 Serra Mall
        city: Stanford
        region: CA
        postcode: '94305'
        country: United States
        country_code: US
      directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
      office_hours:
        - 'Monday 10:00 to 13:00'
        - 'Wednesday 09:00 to 10:00'
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '37.4275'
        longitude: '-122.1697'  
      contact_links:
        - icon: twitter
          icon_pack: fab
          name: DM Me
          link: 'https://twitter.com/Twitter'
        - icon: skype
          icon_pack: fab
          name: Skype Me
          link: 'skype:echo123?call'
        - icon: video
          icon_pack: fas
          name: Zoom Me
          link: 'https://zoom.com'
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
      sections:
---
