# Getting Started

- Install from http://installrails.com/steps/choose_os

## What is Rails

- DRY - dont repeat yourself.
- Convention over configuration.
- Uses [MVC]() pattern.

<figure align="center">
<img width="300" src="/docs/images/mvc.jpg" alt="ruby logo"/>
</figure>

# Common Commands

- Create Rails Project
  `rails new <project_name> -d mysql`

  - _SQLite is the default database._

- Fetch gems
  `bundle install`
- If commands dont ork use `bundle exec <command>`

## Folder Structure

- **Gemfile**
  - Keeps track of gem versions ( _<b>Gems</b> are libraries that Provide functionality_ )
- **Gemfile.lock**
  - Keeps teack of GEM files for the bundler
- **README.rdoc**
  - For info of your application and what it does.
- **app**
  - aplication code goes here
- **bin**
  - contains files to run your app
- **config**
  - Configure a routes between browser and proper controller.
- **db**
  - Contains your databse schema
- **config.ru**
  - Contains configuration rules for starting your application
- **public**
- **log**
- **lib**
- **Rakefile**
- **test**
- **tmp**
