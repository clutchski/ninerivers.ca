
task :autocompile => :clean do
  sh "nanoc autocompile -p 9999"
end

task :compile => :clean do
  sh "nanoc compile"
end

task :clean do
  rm_rf "output"
end

task :default => :autocompile
