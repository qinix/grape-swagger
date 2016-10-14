# frozen_string_literal: true
source 'http://rubygems.org'

gemspec

case version = ENV['GRAPE_VERSION'] || '~> 0.18'
when 'HEAD'
  gem 'grape', github: 'ruby-grape/grape'
else
  gem 'grape', version
end

gem ENV['MODEL_PARSER'] if ENV.key?('MODEL_PARSER')

group :test do
  # gem 'ruby-grape-danger', '~> 0.1.0', require: false
  gem 'grape-entity', '>=0.6'
  gem 'grape-swagger-entity'
end
