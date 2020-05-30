# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "heroku-deflater"
  gem.homepage = "http://github.com/romanbsd/heroku-deflater"
  gem.license = "MIT"
  gem.summary = %Q{Deflate sprockets and webpacker assets on heroku}
  gem.description = gem.summary
  gem.email = "romanbsd@yahoo.com"
  gem.authors = ["Roman Shterenzon"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new


begin
  require 'rspec/core/rake_task'
  RSpec::Core::RakeTask.new(:spec)
rescue LoadError
end

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "heroku-deflater #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
