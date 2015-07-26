require 'bundler'
Bundler.require
#require 'opal'

desc "Build /assets/demo.js"
task :build do
  require 'fileutils'

  Opal.append_path "app"
  src = Opal::Builder.build('demo')
  #min = uglify src
  #gzp = gzip min

  File.open('assets/demo.js', 'w+') do |out|
    out << src
  end

  #puts "development: #{src.size}, minified: #{min.size}, gzipped: #{gzp.size}"
end

task :default => [:build]
