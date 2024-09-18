require "rake/testtask"
require "find"

desc 'Say hello'
task :hello do
  puts "Hello there. This the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

# desc 'List all project files'
# task :list do
#   Find.find(__dir__) do |path|
#     if File.basename(path).start_with?(".") && FileTest.directory?(path)
#       Find.prune
#     end
# 
#     if File.file?(path) && !File.basename(path).start_with?(".")
#       puts path
#     end
#   end
# end

# LS solution

desc 'Display inventory of all files'
task :inventory do
  Find.find(".") do |name|
    next if name.include?('/.') # Excludes files and directories with . names
    puts name if File.file?(name)
  end
end
