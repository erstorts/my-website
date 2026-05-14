source "https://rubygems.org"

# `github-pages` pins Jekyll 3.9 + Liquid 4.0.3, which still call `String#tainted?` (removed in Ruby 3.2).
# Use Ruby 3.1.x locally — e.g. Homebrew: `brew install ruby@3.1` then put
# `/opt/homebrew/opt/ruby@3.1/bin` before `/opt/homebrew/opt/ruby/bin` in PATH.
# See `.ruby-version`.

gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-sitemap"
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
end

# Ruby 3.0+ removed webrick from the stdlib; Jekyll 3's local server still needs it.
gem "webrick", "~> 1.8"
