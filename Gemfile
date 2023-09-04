# frozen_string_literal: true

source "https://rubygems.org"

ruby RUBY_VERSION

# Inside the development app, the relative require has to be one level up, as
# the Gemfile is copied to the development_app folder (almost) as is.
base_path = ""
base_path = "../" if File.basename(__dir__) == "development_app"
require_relative "#{base_path}lib/decidim/nav/version"

DECIDIM_VERSION = Decidim::Nav.decidim_version

gem "decidim", DECIDIM_VERSION
gem "decidim-nav", path: "."

gem "bootsnap"
gem "uglifier", "~> 4.1"

group :development, :test do
  gem "faker", "~> 2.18"

  gem "decidim-dev", DECIDIM_VERSION
  gem "rubocop-performance"
  gem "simplecov", require: false
end

group :development do
  gem "letter_opener_web", "~> 1.3"
  gem "listen", "~> 3.1"
  gem "spring", "~> 2.0"
  gem "spring-watcher-listen", "~> 2.0"
  gem "web-console", "~> 3.5"
end

group :test do
  gem "rubocop-faker"
end
