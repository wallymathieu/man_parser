desc "Run all specs in spec directory"
task :default do
  options = "--colour --format progress --loadby --reverse"
  files = FileList['spec/**/*_spec.rb']
  system("spec #{options} #{files}")
end

task :rdoc do
end

begin
  require 'jeweler'
  project_name = 'man_parser'
  Jeweler::Tasks.new do |gem|
    gem.name = project_name
    gem.summary = "Parse unix man pages into ruby-readable format"
    gem.email = "grosser.michael@gmail.com"
    gem.homepage = "http://github.com/grosser/#{project_name}"
    gem.authors = ["Michael Grosser"]
    gem.rubyforge_project = 'man-parser'
  end
  Jeweler::GemcutterTasks.new
  Jeweler::RubyforgeTasks.new do |gem|
    gem.doc_task = "rdoc"
  end
rescue LoadError
  puts "Jeweler, or one of its dependencies, is not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end