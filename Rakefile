namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola desde Rake!"
  end
end

namespace :db do
  desc "migrates changes to your database"

  task :environment do
  require_relative './config/environment'
  end

  task migrate: :environment do
    Student.create_table
  end

  desc "seeds data into database"
  task seed: :environment do
    require_relative './db/seeds'
  end

end

desc "loads up environment"
task :environment do
  require_relative './config/environment'
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end
