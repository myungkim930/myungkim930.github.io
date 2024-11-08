The website will look somewhat empty at first. That's normal. Follow the next instructions to complete the header and footer components, and the home and blog pages.

### Header
Open the `_config.yml` file and add the following:
```yml
header:
  pages:
    - name: Home
      slug: /     # <-- index.md
    - name: Blog  # <-- blog.md
    - name: Whatever  # <-- whatever.md
```
Re-run `jekyll serve` to see the header updated.

### Footer
Open the `_config.yml` file and add the following:
```yml
footer:
  show_powered_by: true
  contact:
    - type: email
      name: Email
      value: yourmail@domain.com
    - type: wechat
      value: YourWeChatUsername
      link: "#"
  follow:
    - type: twitter
      name: Twitter
      link: http://twitter.com/YourTwitterUsername
      username: "@YourTwitterUsername"
    - type: facebook
      name: Facebook
      link: http://facebook.com/YourFacebookUsername
    - type: linkedin
      name: LinkedIn
      link: http://linkedin.com/in/YourLinkedInUsername
    - type: github
      name: GitHub
      link: http://github.com/YourGitHubUsername
    - type: dribbble
      name: Dribbble
      link: https://dribbble.com/YourDribbbleUsername
    - type: rss
      name: RSS
      link: /feed.xml
```
Re-run `jekyll serve` to see the footer updated.

### Home page
Create (or edit) the `index.markdown` file and add the following:
```yml
---
layout: home
profile_picture:
  src: /assets/img/profile-pic.jpg
  alt: website picture
---

<p>
  Welcome to mysite!
</p>
```

### Blog page
Create `blog.markdown` file and add the following:
```yml
---
layout: blog
title: Blog
slug: /blog
---

This is an example of a "Blog" page, displaying a list of posts.
<br />
```


Your website is ready!


### Development

#### Run development instance (with hot-reload)
```sh
bundle exec jekyll serve
```

#### Build and publish the gem
```sh
gem build bay_jekyll_theme.gemspec
```

```sh
gem push bay_jekyll_theme-1.x.x.gem
```
