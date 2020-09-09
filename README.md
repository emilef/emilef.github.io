# emilef.github.io
My content and code blog focusing on everything data

## Set up Git

https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home


## Set up Git

Download and installl
https://git-scm.com/downloads

## Setup Git Large File Stroage (optional)
https://github.com/git-lfs/git-lfs/releases/download/v2.11.0/git-lfs-windows-v2.11.0.exe

## Install cmder and VS Code (optional)
https://code.visualstudio.com/download
https://github.com/cmderdev/cmder/releases/download/v1.3.16/cmder.zip


## Setting up ruby

Before you can use Jekyll to create a GitHub Pages site, you must install Jekyll and Git
https://jekyllrb.com/docs/installation/
https://docs.github.com/en/articles/set-up-git

https://jekyllrb.com/docs/installation/windows/


Ruby version 2.5.0 or higher, including all development headers (check your Ruby version using ruby -v)
RubyGems (check your Gems version using gem -v)
GCC and Make (check versions using gcc -v,g++ -v, and make -v)



## ridk
https://github.com/oneclick/rubyinstaller2#using-the-installer-on-a-target-system

The components are defined here. The single options do:

Download, verify and run the MSYS2-installer. This installs the base MSYS2 environment (bash, pacman, tar, etc.) without development packages.
Download the pacman repository inventory. This retrieves version information about all available MSYS2+MINGW packages.
Download and install the development packages, which are typically required to compile ruby C extensions.
You should usually just press enter and execute all three options. And if something fails, you can restart the MSYS2 installation anytime later per ridk install.



## Setting up ruby gems
https://rubyinstaller.org/downloads/

https://github.com/oneclick/rubyinstaller2#using-the-installer-on-a-target-system


For instance these popular gems can be installed like so from the source gem:

To install sqlite3 gem:
  ridk exec pacman -S mingw-w64-x86_64-sqlite3
  gem install sqlite3 --platform ruby
To install nokogiri gem:
  ridk exec pacman -S mingw-w64-x86_64-libxslt
  gem install nokogiri --platform ruby -- --use-system-libraries


## Setting up Github Pages


## Seting up Github FLow
https://guides.github.com/introduction/flow/


## Using Jekyll

Jekyll is a static site generator with built-in support for GitHub Pages and a simplified build process. Jekyll takes Markdown and HTML files and creates a complete static website based on your choice of layouts. Jekyll supports Markdown and Liquid, a templating language that loads dynamic content on your site

You can configure most Jekyll settings, such as your site's theme and plugins, by editing your _config.yml file.

Some configuration settings cannot be changed for GitHub Pages sites.

lsi: false
safe: true
source: [your repo's top level directory]
incremental: false
highlighter: rouge
gist:
  noscript: false
kramdown:
  math_engine: mathjax
  syntax_highlighter: rouge

By default, Jekyll doesn't build files or folders that:

are located in a folder called /node_modules or /vendor
start with _, ., or #
end with ~
are excluded by the exclude setting in your configuration file


If you want Jekyll to process any of these files, you can use the includes setting in your configuration file.
https://jekyllrb.com/docs/configuration/

Front matter
To set variables and metadata, such as a title and layout, for a page or post on your site, you can add YAML front matter
https://jekyllrb.com/docs/front-matter/

Themes
You can add a Jekyll theme to your GitHub Pages site to customize the look and feel of your site. 
https://jekyllrb.com/docs/themes/

Plugins
You can download or create Jekyll plugins to extend the functionality of Jekyll for your site. 
https://jekyllrb.com/docs/plugins/


GitHub Pages uses plugins that are enabled by default and cannot be disabled:

jekyll-coffeescript
jekyll-default-layout
jekyll-gist
jekyll-github-metadata
jekyll-optional-front-matter
jekyll-paginate
jekyll-readme-index
jekyll-titles-from-headings
jekyll-relative-links

Syntax highlighting
To make your site easier to read, code snippets are highlighted on GitHub Pages sites the same way they're highlighted on GitHub. 
https://docs.github.com/en/articles/creating-and-highlighting-code-blocks


ekyll uses the Rouge highlighter, which is compatible with Pygments. If you specify Pygments in your _config.yml file, Rouge will be used instead. Jekyll cannot use any other syntax highlighter
https://docs.github.com/en/articles/about-jekyll-build-errors-for-github-pages-sites


If you want to use another highlighter, such as highlight.js, you must disable Jekyll's syntax highlighting by updating your project's _config.yml file.

kramdown:
  syntax_highlighter_opts:
    disable : true


If your theme doesn't include CSS for syntax highlighting, you can generate GitHub's syntax highlighting CSS and add it to your project's style.css file.

$ rougify style github > style.css


Building your site locally

Then, test your site locally. For more information, see "Testing your GitHub Pages site locally with Jekyll."
https://docs.github.com/en/articles/testing-your-github-pages-site-locally-with-jekyll