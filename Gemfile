# Work around bug in Debian Squeeze - see https://github.com/mysociety/alaveteli/pull/297#issuecomment-4101012
if File.exist? "/etc/debian_version" and File.open("/etc/debian_version").read.strip =~ /^(squeeze.*|6\.0\.[45])$/
    if File.exist? "/lib/libuuid.so.1"
        require 'dl'
        DL::dlopen('/lib/libuuid.so.1')
    end
end
source :rubygems

gem 'rails', '3.0.17'
gem 'pg'

gem 'fastercsv', '>=1.5.5'
gem 'json', '~> 1.5.1'
gem 'mahoro'
gem 'mail', :platforms => :ruby_19
gem 'memcache-client', :require => 'memcache'
gem 'net-http-local'
gem 'net-purge'
gem 'rack'
gem 'rdoc'
gem 'recaptcha', '~> 0.3.1', :require => 'recaptcha/rails'
# :require avoids "already initialized constant" warnings
gem 'rmagick', :require => 'RMagick'
gem 'rake', '0.9.2.2'
gem 'ruby-msg', '~> 1.5.0'
gem 'vpim'
gem 'will_paginate', '~> 2.3.11'
# when 1.2.9 is released by the maintainer, we can stop using this fork:
gem 'xapian-full-alaveteli', '~> 1.2.9.5'
gem 'xml-simple'
gem 'zip'
gem 'capistrano'
gem 'syslog_protocol'
gem 'newrelic_rpm'
gem 'tmail'
# Use until this PR is merged: https://github.com/svenfuchs/globalize3/pull/191
gem 'globalize3', :git => 'git://github.com/henare/globalize3.git', :branch => 'not-null-empty-attributes'
gem 'acts_as_versioned'
gem 'dynamic_form'
# Use until the 'globalize3' branch is merged upstream. TODO: add PR link here
gem 'strip_attributes', :git => 'git://github.com/openaustralia/strip_attributes.git', :ref => '01a7215ffe7603f2726cb91b34cde3756f528f7d'

# Gems related to internationalisation
# Also in vendor/plugins there is globalize2
gem 'fast_gettext'
gem 'gettext_i18n_rails'
gem 'gettext'
gem 'locale'
gem 'routing-filter'

group :test do
  gem 'fakeweb'
  gem 'test-unit', '~> 1.2.3', :platforms => :ruby_19
  gem 'webrat'
end

group :development do
  gem 'mailcatcher'
end

group :develop do
  gem 'ruby-debug', :platforms => :ruby_18
  gem 'ruby-debug19', :platforms => :ruby_19
  gem 'bootstrap-sass'
  gem 'compass'
  gem 'annotate'
end

group :test, :development do
  gem 'rspec-rails'
end
