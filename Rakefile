# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

Rails.application.load_tasks

Rake::Task["assets:precompile"].clear
task "assets:precompile" do
  puts "loading warbler..."
  require 'warbler'

  puts "Creating war task"
  Warbler::Task.new

  puts "Executing war task"
  Rake::Task["war"].execute

  # clean some things out of the slug that we don't need
  `rm -rf vendor` if ENV['STACK'] == "cedar-14"
end
