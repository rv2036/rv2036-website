source "https://rubygems.org"

# 针对 Ruby 3.4+ 的兼容性补丁
gem "base64"
gem "bigdecimal"
gem "mutex_m"


# 1. 核心依赖
gem "jekyll", "~> 3.10.0"
gem "minimal-mistakes-jekyll", "~> 4.24.0" 
gem "faraday-retry" 
gem "kramdown-parser-gfm"

# 2. 插件组 
gem "jekyll-polyglot"
gem "jekyll-remote-theme"
gem "jekyll-include-cache" 
gem "jekyll-feed"
gem "jekyll-paginate"
gem "jekyll-sitemap"
gem "jekyll-gist"

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library. 
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows 
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
