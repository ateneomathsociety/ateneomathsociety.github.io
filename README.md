# AMS Website 

This is the repository for the Ateneo Mathematics Society (AMS) website, powered by [Jekyll](https://jekyllrb.com/) using the [Yet Another Theme (YAT) theme](https://github.com/jeffreytse/jekyll-theme-yat). See their corresponding documentations for more details.

## Installation

To manage and update the contents of this repository and website, download and install the following dependencies following the official guides:

- [Git](https://docs.github.com/en/get-started/git-basics/set-up-git#setting-up-git)

    - Make sure to also [add your SSH key to GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) 

- [Ruby & Jekyll](https://jekyllrb.com/docs/installation/)

## Local Deployment

Run the following command to clone the repository

```bash
git clone git@github.com:ateneomathsociety/ateneomathsociety.github.io.git
```

Run the following command during the initial set-up to install the dependencies

```bash
bundle install
```

Run the following command to deploy the website locally at [http://localhost:3000](http://localhost:3000)

```bash
bundle exec jekyll serve --livereload --port 3000
```

Run the following command, after making the necessary modifications, to commit your changes and push to GitHub

```bash
git add .   # This will add all files
git commit -m "Commit Message" -m "More Details"
git push 
```

## Updating Contents

With Jekyll, managing and updating the contents of the website reduces to updating the contents of Markdown and YAML files.

The general format for the Markdown files is as follows

```markdown
---
layout:       default                           # DO NOT CHANGE, unless you know what you are doing (optional for some pages)
title:        "Home"                            # The page title used for indexing
heading:      "Ateneo Mathematics Society"      # The page heading
subheading:   "Where Everybody Counts."         # The page subheading (optional)
permalink:    "/about"                          # The relative url of the page (optional)
banner:
  image:      "/assets/images/banners/default.png"      # The path to the page banner image (can be set to a default image)
  height:     180px                                     # The height of the page banner image (optional, defaults to 180px)
  opacity:    1.00                                      # The opacity of the page banner image (optional, defaults to 1.00)
---

Some page content
```

### Home

To update the `/` (home) page, navigate to the `index.html` file. 

### About

To update the `/about` page, navigate to the `about.md` file. To update its contents, navigate to the `_data/about.yml` file and update the corresponding fields. Make sure the file is a valid YAML file!

### Departments

To update the `/about/departments` page, navigate to the `departments.md` file. DO NOT MODIFY THE CODE below the second `---` line in the file unless you know what you are doing. 

To add a department, create a new Markdown file at `_departments` with the format `department-name.md`. MAKE SURE THIS NAME IS CONSISTENTLY USED IN THE ENTIRE WEBSITE. You can add descriptions of the department below the second `---` line in the file.

### Offices

To update the `/about/offices` page, navigate to the `offices.md` file. DO NOT MODIFY THE CODE below the second `---` line in the file  unless you know what you are doing. 

To add an office, create a new Markdown file at `_offices` with the format `office-name.md`. MAKE SURE THIS NAME IS CONSISTENTLY USED IN THE ENTIRE WEBSITE. You can add descriptions of the office below the second `---` line in the file. You can also add a list of efforts between the `---` lines as follow

```markdown
---
title:          "Sample Office"
heading:        "Sample Office"
subheading:     ""
icon:           "/assets/images/icons/default.png"
banner:
  image:        "/assets/images/banners/default.png"
  height:       180px
  opacity:      1.00
efforts:
  - image:        ""                        # A logo for the effort (optional)
    external_url: ""                        # An external link for the effort (optional)
    include_url:  false                     # Set to true only if an external link is provided
    title:        "Sample Effort A"         # The title of the effort
    content:      "Sample Effort A..."      # The description of the effort
  - image:        ""
    external_url: ""
    include_url:  false
    title:        "Sample Effort B"
    content:      "Sample Effort B..."
---

The Sample Office is ...

```

### Pools & Teams

To update the `/about/pools-teams` page, navigate to the `pools-teams.md` file. DO NOT MODIFY THE CODE below the second `---` line in the file unless you know what you are doing. 

To add a pool or team, create a new Markdown file at `_pools_teams` with the format `pool-or-team-name.md`. MAKE SURE THIS NAME IS CONSISTENTLY USED IN THE ENTIRE WEBSITE. You can add descriptions of the pool or team below the second `---` line in the file. You can also specify the parent department between the `---` lines as follow

```markdown
---
title:          "Sample Team"
heading:        "Sample Team"
subheading:     ""
parent:         "department-name"                       # Make sure this name is consistent with the filename of the department in _departments
icon:           "/assets/images/icons/default.png"
banner:
  image:        "/assets/images/banners/default.png"
  height:       180px
  opacity:      1.00
---

The Sample Team is ...

```

### Projects

To update the `/projects` page, navigate to the `projects.md` file. DO NOT MODIFY THE CODE below the second `---` line in the file unless you know what you are doing. 

To add a project, create a new Markdown file at `_projects` with the format `project-name.md`. MAKE SURE THIS NAME IS CONSISTENTLY USED IN THE ENTIRE WEBSITE. You can add descriptions of the project below the second `---` line in the file. You can also specify the parent department, office, pool, or team between the `---` lines as a comma-separated string as follow

```markdown
---
title:          "Sample Project"
heading:        "Sample Project"
subheading:     ""
parent:         "department-name, pool-name"                       # Make sure this name is consistent with the filename of the department, office, pool, or team
icon:           "/assets/images/icons/default.png"
banner:
  image:        "/assets/images/banners/default.png"
  height:       180px
  opacity:      1.00
---

The Sample Project is ...

```

### Services

To update the `/services` page, navigate to the `services.md` file. DO NOT MODIFY THE CODE below the second `---` line in the file unless you know what you are doing. 

To add a service, create a new Markdown file at `_services` with the format `service-name.md`. MAKE SURE THIS NAME IS CONSISTENTLY USED IN THE ENTIRE WEBSITE. You can add descriptions of the service below the second `---` line in the file. You can also specify the parent department, office, pool, or team between the `---` lines as a comma-separated string as follow

```markdown
---
title:          "Sample Service"
heading:        "Sample Service"
subheading:     ""
parent:         "department-name, pool-name"                       # Make sure this name is consistent with the filename of the department, office, pool, or team
icon:           "/assets/images/icons/default.png"
banner:
  image:        "/assets/images/banners/default.png"
  height:       180px
  opacity:      1.00
---

The Sample Service is ...

```

### Pages 

To update the `/pages` page, navigate to the `pages.md` file. To update its contents, navigate to the `_data/pages.yml` file and update the corresponding fields. Make sure the file is a valid YAML file!

### News 

To update the `/news` page, navigate to the `news.md` file. To add an article, create a new Markdown file at `_posts` with the format `year-month-day-some-title.md`. Refer to the following [samples](https://github.com/jeffreytse/jekyll-theme-yat/tree/master/_posts) on how to write a post in Markdown.

```markdown
---
layout:       post                              # DO NOT CHANGE, unless you know what you are doing (optional for some pages)
title:        "Sample Post Title"               # The post title
subtitle:     "Sample Post Subtitle"            # The post subtitle (optional)
author:         "Matt E. Matics"                # The author name
banner:
  image:        "/assets/images/banners/default.png"
  height:       180px
  opacity:      1.00
---

Post contents here
```
