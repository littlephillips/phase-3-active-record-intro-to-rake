#to view the list of available rake tasks
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'outputs a greetings message'
task :greet do
  puts "Hello World, from Phillip Kinuthia"
end

#namespace , group or contain 

namespace :greeting do
  desc 'ouputs hola to the terminal'
  task :hola do
    puts "hola de rake"
  end


  desc 'outputs a greetings message'
  task :greet do
    puts "Hello World, from Phillip Kinuthia"
  end
end

#bundle exec rake
# rake greeting:hola 
# rake aborted!
# Gem::LoadError: You have already activated rake 10.4.2,
# but your Gemfile requires rake 10.4.0.
# Prepending `bundle exec` to your command may solve this.

# bundle exec rake greeting:hola

#common Rake Tasks
  #rake db:migrate

  task :environment do 
    require_relative './config/environment.rb'
  end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end
end

namespace :db do
  desc  'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds.rb'
  end
end

#interacting  with our class and database without having to run our entire program...
#build a Rake task that will load up Pry console for us


#rake console
desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end