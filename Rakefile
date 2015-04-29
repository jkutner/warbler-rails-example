# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

Rails.application.load_tasks


task "assets:precompile" do
  require 'warbler'
  Warbler::Task.new
  Rake::Task["war"].execute

  # clean some things out of the slug that we don't need
  `rm -rf vendor` if ENV['STACK'] == "cedar-14"
end
