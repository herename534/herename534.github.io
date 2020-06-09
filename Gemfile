source "https://rubygems.org"
ruby RUBY_VERSION
require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem "jekyll", "~>3.8.7"
gem "minima", "~> 2.0"
gem 'github-pages', versions['github-pages']
group :jekyll_plugins do
   gem "jekyll-feed", "~> 0.6"
end
gem "jekyll-paginate"
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

