# README

This is more so some notes on how to update and develop my site.

## How to get this to run on local
1. Run through install - https://jekyllrb.com/docs/installation/macos/
2. Run `bundle update` to get the dependencies for the project. You might need to remove or update strict versions.
3. Run `bundle install` and confirm all `gems` (packages) are installed
4. Run `bundle exec jekyll serve` to run locally
   
## Workflow
Run locally, confirm site looks like what you want then push to prod

## Directory Structure
```
repo/
|── _includes                  # Theme includes
├── _layouts                   # Theme layouts (see below for details)
├── _pages                     # Menu pages
├── _plugins                   # Any plugins the site uses
├── _posts                     # Where all your posts pages will go
├── _projects                  # Where all your project pages go
├── _sass                      # `sass` files
├── files                      # Any pdfs or one off html files
├── images                     # Any images to link to posts or pojects
├── _config.yml                # Site build settings
├── Gemfile                    # Ruby Gemfile for managing Jekyll plugins
└── index.html                 # The other files build on top of this - dont touch
```

## Notes
- `Gemfile` lists dependencies for the project
- `chruby` manages different `ruby` versions
- `/_layouts/blog/html` is what makes the `index.html` landing page. It makes the card for each file in `/_posts`
- `/_layouts/project.html` is the format im using to style my individual post files. I like how it looks better than `/_layouts/post.html`, but I should probably edit it to look like what I want.
- The `yaml` at the top of each post in `/_posts` defines what layout to use that is available in `/_layouts`

## Making Changes
- To make a change in the top right header navbar, edit `./_includes/navigation.html` and make sure there is an appropriate link to the page you want to set up in `./_pages/`
