source "https://rubygems.org"

# GitHub Pages gem - this ensures compatibility with GitHub Pages
gem "github-pages", "~> 232", group: :jekyll_plugins

# If you have any plugins, put them here
group :jekyll_plugins do
  gem "jekyll-seo-tag"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]
