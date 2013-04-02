# jekyll-wiki

This project is supposed to serve as foundation of a responsive and flexible guerilla wiki for hackers.
It transfers your markdown/textile notes to satic html layout inspired by sublime text editor.

## Preview/Current Demo

![Version 0.1](https://github.com/dataduke/jekyll-wiki/raw/master/%E2%80%8E_demo/version01.jpg)

## Project Structure

    .
    |-- _demo (can be ignored; used for project information only)
    |-- _backup (can be ignored; used for backup of development files)
    |-- _includes (used for building index pages)
    |   |-- main-index-sidebar.md
    |   |-- main-index-box-N.md
    |   |-- box-N-index-sidebar.md
    |   |-- box-N-index.md
    |-- _layouts
    |   |-- default.html
    |   |-- post.html
    |-- _site (created by jekyll for deployment; not checked in)
    |-- _plugins 
    |   |-- additional-feature-X
    |-- assets (for layout dependencies only)
    |   |-- css
    |       |-- style.css
    |   |-- img
    |   |-- js
    |   |-- favicon.ico
    |-- box-N (box 1-4 implemented for testing; boxes can be added if needed and be renamed as wished)
    |   |-- _posts
    |   |   |-- 2013-01-01-hello-world.markdown (.md or .textile or .taskpaper)
    |   |   |-- 2013-01-01-hello-world (folder for post attachments)
    |   |       |-- attachment-1.jpg
    |   |       |-- attachment-2.pdf
    |   |-- atom.xml
    |   |-- index.html
    |-- _config.yml
    |-- index.html
    |-- atom.xml

## Change History

- **Version 0.1** Inital commit, not working

## Implemented Features

- multiple boxes/repositories (blogs) for notes (markdown, textile)
- sort by date created

## To Be Done

- basic layout  
  - fix horizontal scrolling
  - post layout
  - box layout
- advanced layout
  - card stack view
  - show/hide box column by selesction in main view
  - allow drag and drop to sort columns
- sorting
  - sort by date modified
  - sort by category
  - sort by tags
  - sort by name
- set box/post/content column width
  - 300px
  - 600px
  - 900px
- switch scrolling for post
  - horizontal
  - vertical 
- markup
  - add syntax highlighting
  - add mathjs
- special cards
  - add support for .taskpaper files
  - add support for .rst file (reStructuredText)
  - add support for learning card attribute (POI pile of index cards)
- attachment and image support
  - attachment folder has same name as post (sits in same directory)
  - create automatic links to images in attachment folders
  - add support for post/card attachments (contained in post-name-folders)
- add top bar
  - add search box on left
  - add breadcrumb path
  - filter box (for highlighting words in content area)
- add config file
  - global font with font size
  - contains attributes for each box (box name, relative box path, box foreground color, box background color)
- themes
  - finish sublime text theme
  - build theme Simple Github / jekyll-bootstrap with [twitter theme](http://themes.jekyllbootstrap.com/)
  - build theme [Apple Developer Wiki](https://developer.apple.com/technologies/ios/)
  - build theme [FoldingText Website](http://www.foldingtext.com/)
  - build theme [docs](https://readthedocs.org/)
  - build theme paint-pot-like (website suitable)
  - build theme scientific thesis (website suitable)
  - add theme switcher
- individual columns
  - show/hide boxes on landing page
  - change view/sorting of each box individually
- small appify
  - launch local website in safari via alfred app
  - search local website in safari via alfred app
  - only create local relate links that don't need a webserver (static html only), like:
    `<a href='./folder/2011-12-29-jekyll-introduction.html' title='Jekyll Introduction'>Jekyll Introduction</a>`
- big appify (maybe not to be done)
  - create browser app which wraps all dependencies (jekyll, ruby)
  - implement toggle to source view on post layout
  - allow editing inside source view
  - separate/strip boxes to folders outside of app
  - allow only custom folder path for boxes outside of wiki instance
- mobile appify
  - make it deployable via dropbox for mobile use (ios, android)
  - every box has its own feed which is usable by rss-reader apps

## References

### Core Technologies

- [ruby](http://www.ruby-lang.org/en/)
- [jekyll](https://github.com/mojombo/jekyll)

### Related Technologies

- [jekyll-bootstrap](https://github.com/plusjade/jekyll-bootstrap) 
- [multi-blog-jekyll](https://github.com/ggarron/multi-blog-jekyll)
- [github pages](http://pages.github.com/)  
- [github pages help](https://help.github.com/categories/20/articles) 

### Design Inspirations

- **Sublime Text Theme (default)**
  - [Sublime Text](http://www.sublimetext.com/)
  - [Soda-Dark.sublime-theme](https://github.com/buymeasoda/soda-theme)
  - [Monokai-Soda.tmtheme](https://github.com/simeonv/st2-color-schemes)

### Markup Languages

- [markdown](http://daringfireball.net/projects/markdown/) by John Gruber
- [multimarkdown](http://fletcherpenney.net/multimarkdown/) by Fletcher Penny
- [github flavored markdown](https://help.github.com/articles/github-flavored-markdown) by GitHub
- [textile](http://textism.com/tools/textile/) by Dean Allan
- [taskpaper](http://www.hogbaysoftware.com/products/taskpaper) by Jesse Grosjean