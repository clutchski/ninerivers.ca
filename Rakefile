
desc "Autocompile"
task :autocompile => :clean do
  sh "nanoc autocompile -p 9999"
end

desc "Compile"
task :compile => :clean do
  sh "nanoc compile"
end

desc "Clean"
task :clean do
  rm_rf "output"
end

task :default => :autocompile

desc "Deploy"
task :deploy => [:compile] do
  sh "cd output && s3cmd -c ~/.s3cfg.ninerivers sync . s3://www.ninerivers.ca"
end


