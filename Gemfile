ruby '2.1.10'

source "http://rubygems.org"

gem "rails", "~> 3.2.19"
gem 'test-unit', require: false
gem 'composite_primary_keys', '~> 5.0.14'

gem "rake"
gem "airbrake"

# Warning! We use bundler for Gemfile and Gemfile.lock parsing.
# Please validate the bundler version against the parser.
gem "bundler", "~> 1.5"

# Warning: octokit is extended, please check lib/core_ext/octokit.rb before upgrading
gem "octokit", "~> 3.0"

# To add cache to Octokit requests:
gem 'faraday-http-cache'

gem "pusher"
gem "gems", "~> 0.0"
gem "gemnasium-parser"
gem "unicorn"
gem 'therubyracer'
gem 'activeadmin', '~> 1.0.0.pre2'
gem 'haml'
gem 'rdiscount' # for haml's markdown filter
gem 'pdfkit'
gem 'rubyzip'

# Campfire notifications
gem 'tinder'

gem "resque"
gem 'resque-scheduler', :require => 'resque_scheduler'
gem 'resque-retry'
gem "resque-loner"
gem "resque-status"

gem 'versionist'
gem 'state_machine'
gem 'resque_mailer'

gem 'kaminari'

gem 'vandamme'
gem 'RedCloth' # to allow Vandame to parse .textile changelogs
gem 'nokogiri'
gem 'asciidoctor'
gem 'org-ruby'

gem 'devise'
gem 'devise-async'
gem 'omniauth-github'

# payments
gem 'stripe'

gem 'cancan'
gem 'packagist', git: 'https://git.tech-angels.net/gemnasium/packagist.git'

gem 'krakow', '~>0.4.2'

gem 'drip-ruby', require: 'drip'

group :production, :staging do
  gem "newrelic_rpm"
  gem "dalli"
end

group :production, :staging, :enterprise do
  gem "pg"
  gem 'gelf'
  gem 'lograge'
end

group :assets do
  gem 'sass-rails'
  gem 'coffee-script'
  gem 'uglifier'
  gem 'jquery-rails'
  gem 'twitter-bootstrap-rails'
  gem 'turbo-sprockets-rails3'
end

group :development, :staging do
  gem 'mail_view'
end

group :development, :test do
  gem 'rspec-rails', '~> 2.14.1'
  gem 'email_spec', '~> 1.5.0'
  gem 'shoulda-matchers'

  # do not require factory_girl so Spork does not spook and reload our factories at every run
  # see http://goo.gl/zEbwY
  gem "factory_girl_rails", "~> 4.1.0", :require => false

  gem "webmock",  :require => false
  gem "vcr"
  gem "launchy"
  gem "database_cleaner"

  gem "timecop", "~> 0.3.5"
  gem 'annotator'
  gem "quiet_assets"

  # pretty prints Ruby objects in full color exposing their internal structure with proper indentation
  # see https://github.com/michaeldv/awesome_print
  gem "awesome_print", :require => false
end

group :development do
  gem 'gemnasium'
  gem 'terminal-notifier-guard'

  # generate model diagrams, http://rails-erd.rubyforge.org/
  # Generate diagram with: rake erd indirect=false && mv erd.pdf doc/
  gem "rails-erd"

  # Guard https://github.com/guard/guard

  # OS X specific
  gem 'rb-fsevent', :require => false

  # Linux specific
  gem 'rb-inotify', :require => false
  gem 'libnotify', :require => false

  # automatically run your specs (much like autotest)
  # https://github.com/guard/guard-rspec
  gem 'guard-rspec'

  # automatically manage Spork DRb servers, https://github.com/guard/guard-spork
  gem 'guard-spork'

  # automatically & intelligently install/update bundle when needed, https://github.com/guard/guard-bundler
  gem 'guard-bundler'

  # Better Errors replaces the standard Rails error page with a much better and more useful error page.
  gem "better_errors"
  gem 'binding_of_caller' # To enable the REPL and local/instance variable inspection.
end

group :test do
  # Code coverage for Ruby 1.9 https://github.com/colszowka/simplecov
  gem 'simplecov', :require => false

  gem 'acts_as_fu'

  gem 'resque_spec'
end
