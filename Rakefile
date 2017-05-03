
desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

task :environment do
  require_relative './config/environment'
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end

end



#in this case-- migrating your new students table to your database which is created in th environment.rb
namespace :db do
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

end


# desc 'migrate changes to your database'
# namespace :db do
#   task :migrate => :environment do
#     Student.create_table
#   end
# end
