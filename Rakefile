require 'rake'
require "sinatra/activerecord/rake"
require ::File.expand_path('../config/environment', __FILE__)

Rake::Task["db:create"].clear
Rake::Task["db:drop"].clear

# NOTE: Assumes SQLire3 DB
desc "create the database"
task "db:create" do
	touch 'db/db.sqlite3'
end

desc "drop the database"
task "db:drop" do
	rm_f 'db/db.sqlite3'
end

desc 'Retrieves the current schema verison number'
task "db:verison" do
	puts "Current verison: #{ActiveRecord::Migrator.current_version}"
end