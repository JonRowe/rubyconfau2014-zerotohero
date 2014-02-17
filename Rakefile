require "rake"

begin
  require 'rspec/core/rake_task'

  desc "Run RSpec tests"
  RSpec::Core::RakeTask.new(:spec) do |t|
    t.ruby_opts = %w[-w]
    t.pattern = 'spec/**/*_spec.rb'
  end

  task default: %w[spec]

  require 'rake/testtask'

  desc "Run MiniTest tests"
  Rake::TestTask.new do |t|
    t.libs << "test"
    t.ruby_opts = %w[-w]
    t.test_files = FileList['test/**/*.rb']
  end

rescue LoadError
  task default: %w[setup]
end

task :setup do
  begin
    require 'bundler'
  rescue LoadError
    puts "Please install bundler (hint: `gem install bundler`)"
    exit(1)
  end
  `bundle install --standalone --binstubs`
  Bundler.require
  puts "You're good!"
end
