# Gemfile for Bell-Torres Family Website
# This file specifies the Ruby gems (packages) needed for the website

source "https://rubygems.org"

# Jekyll - the static site generator
gem "jekyll", "~> 4.3"

# GitHub Pages gem - ensures compatibility with GitHub Pages
# Uncomment if you want to match GitHub Pages' exact environment
# gem "github-pages", group: :jekyll_plugins

# Jekyll plugins
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"           # Generates RSS feed
  gem "jekyll-seo-tag", "~> 2.8"         # Adds SEO metadata
  gem "jekyll-sitemap", "~> 1.4"         # Generates sitemap.xml
  gem "jekyll-paginate", "~> 1.1"        # Adds pagination support
end

# Windows and JRuby specific gems
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# Webrick is needed for Ruby 3.0+
gem "webrick", "~> 1.8"
