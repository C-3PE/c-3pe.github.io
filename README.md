# A website template for academics

## Introduction 

This is a statically-generated Jekyll/Liquid/Bootstrap-based website for C-3PE. This is primarily based on the
template provided by [sybryngelson](https://github.com/sbryngelson/academic-website-template) Some features include:

* Automatically generated buttons for DOI/PDF/ARXIV/BIB/Abstract information
  * via Jekyll Scholar
* Bibliography information and abstracts open in drown-down wells via buttons
* Fontawesome icons (email, CV, Google Scholar, ResearchGate, GitHub, etc.)
* Dark color scheme via Bootswatch
* Consistent and attractive `About me` page

## Customization

* Modify `_config.yml` as appropriate
* Modify YAML database files, located in `_data/*.yml`, as appropriate
* Modify individual pages, located in `_pages/*.md`, as appropriate

### Navbar

The pages in the top navbar are in the `_config.yml` file.
The typical options are already included or commented on, though additional pages can be created and listed here.

### Creating or editing pages

All pages are located in the `_pages` directory.
Pages generally load information from YAML databases located as `_data/*.yml`.
Creating new pages can be done by using existing pages as a template.

#### Page header information

All pages require header information.
Example header data for the 'Talks' page is below.
```
---
title: "Talks"
layout: gridlay
sitemap: false
permalink: /talks/
---
```
The `layout` variable corresponds to HTML layouts in the `_layouts` directory.
The difference between most layouts is subtle, and `gridlay` can generally be used.
The permalink must be unique for each page and correspond to the directory storing the page in the compiled HTML.
Refer to your pages in `_config.yml` via the `title` variable.

#### Markdown

All pages are written in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) as `*.md`.
HTML commands and CSS styles can be directly used in a markdown files.

#### Publication page and database

The publications and talks are now listed via Jekyll Scholar.
The bibliography file `ref.bib` is located in the `assets/` directory.
Modify according to your needs.

## Acknowledgment

I credit [sybryngelson](https://github.com/sbryngelson/academic-website-template) and their webpage template for this website

## License

MIT
