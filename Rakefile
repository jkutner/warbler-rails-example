# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

Rails.application.load_tasks

#Rake::Task["assets:precompile"].clear
#Rake::Task["assets:clean"].clear
task "assets:precompile" do
  #require 'warbler'
  #Warbler::Task.new

  puts "Executing war task"
  #Rake::Task["war"].execute
  exec('warble')
end

task "assets:clean" do
  # clean some things out of the slug that we don't need
  #`rm -rf vendor/ruby-2.2.2-jruby-9.0.0.0.pre2`
  `find vendor/* ! -name jvm -print0 | xargs -0 rm -rf --`
end
