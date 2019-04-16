---
  title: Getting Started with Jekyll
  permalink: /Getting-Started.html
  nav_exclude: false
  #information for nuighackyhouradminstrator
  #+author: Carlos Sanchez
  #+email: carsandeu@gmail.com
---

[\\]: # Guide to edit, test, and deploy our website

# Getting started with the hh-nuig website
This guide cover the basics of using [https://jekyllrb.com/](Jekyll) to simply
build a static website, our design choices, and our suggestion to our improve
this project.

## Deploy the website locally using Jekyll
Jekyll is a [Ruby Gem](https://guides.rubygems.org/what-is-a-gem/) that can be
installed on any operating system having a `c++` compiler (the common GNU
Compiler Collection would be the best option
[GCC](https://gcc.gnu.org/install/)), [GNU
Make](https://www.gnu.org/software/make/), [Ruby
2.4+](https://www.ruby-lang.org/en/documentation/installation/), and
[RubyGems](https://rubygems.org/pages/download).

A complete installation guide is provided on the [Jekyll Documentation
page](https://jekyllrb.com/docs/installation/) and we especially advice
_Windows_ user to refer to the official guide since we aren't windows users
ourselves.

Here a guide to setup a copy of our environment is provided. If you use Docker,
stay tuned because we will soon provide a Docker container with everything ready
to use.

### Installing Dependencies
First of all check what you have already on your system so you will know what
you need to install, upgrade or keep as it is :smile:

In your terminal emulator run the following code and check the output: `gcc -v`
(8.2+), `make -v` (4.2+), `ruby -v` (2.6.2), `gem -v` (3.0+).

If you don't have `gcc` and `make` installed or updated we ask you to refer to
the official guides (see above) or get in contact with us by opening an issue on
[GitHub](https://github.com/NUIGhackyhour/NUIGhackyhour.github.io/issues). We're
happy to help, but this guide would become too long if we explain each variation
of `c++` compilers and GNU Make. :wink: Now let's focus on Ruby and RubyGems
:smile:

If you don't have Ruby on your system or you need to update, we recommend using
[rbenv](https://github.com/rbenv/rbenv) to setup and manage multiple ruby
instances. To get **rbenv** check the [official
guide]((https://github.com/rbenv/rbenv#installation) or
[this](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-18-0)
guide for _Ubuntu_.

Once you have **rbenv** installed, install ruby 2.6.2 with `rbenv install 2.6.2`
and set version 2.6.2 to be used globally `rbenv global 2.6.2`. If you need to
work on a different project with a different version of ruby simply change the
global version back.

Now its time to install or update RubyGems. If you don't have RubyGems installed
on your system get it from [here](https://rubygems.org/pages/download) or update
is by typing `gem update --system` in your terminal emulator.

Yeah! We're done with dependencies :heavy_exclamation_mark: :heavy_exclamation_mark: :smile:

### Installing Jekyll
This is very easy, since we provided a _Gemfile_ and _Gemfile.lock_ that will
tell RubyGems what to install and which version :smile:

Be sure to be in the repository folder (`cd path/to/repository/clone`) and then
install the RubyGems package manager _Bundler_ by typing `gem install bundler`.
Now is just a matter of installing the gems required for our website by typing
`bundler install`. You can checkout which gems have been installed by using the
command `gem list`.

### Build the site locally
Ok, we're almost done :smile: Now, be sure again to be in the project folder and
type `bundler exec jekyll serve` Here you go :heavy_exclamation_mark:
:heavy_exclamation_mark: The local copy of the website is available at the
address [http://localhost:4000](http://localhost:4000).

## Understanding the folder structure and the developing choices.

This project folder contain the following files:

-   **Basic linux files:** `.`, `..`, and `.directory`
-   **.gitignore:** a list of files not under version control
-   **.jekyll-metadata:** A list of files have not been modified since the last site build and of files that need to be rebuild.
-   **Gemfile and Gemfile.lock:** Ruby files for the required gems name and version.
-   **index.md:** The site homepage written in markdown. If and only if a *front matter* in YAML is provided, Jekyll will process the file.
-   **README.org:** This file.
-   **\_config.yml:** The basic website configuration (e.g., which css theme to use, and so on)

And the following directories:

-   **.git:** Git version control folder
-   **\_data:** Data sets for the website. For example, a `members.yml` file containing the site members' info, to which a post can refer without rewriting the code.
-   **\_drafts:** A folder for posts drafts that will not be processed
-   **\_includes:** Layout for website sub-parts, like the header or the comments section.
-   **\_layouts:** Theme settings. Here is possible to alter the layout of the whole site or of specific types of pages
-   **\_posts:** Posts for the website. The posts files must have the following name structure `YEAR-MONTH-DAY-title.MARKUP`
-   **\_site:** The built site. **This is not tracked by git** and only available locally.
