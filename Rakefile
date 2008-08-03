task :default => [:sass, :haml]

task :sass do
  `sass -t compressed sass/screen.sass > out/screen.css`
  `sass -t compressed sass/ie.sass > out/ie.css`
end

task :haml do
  files = FileList['tpl/*.haml']
  
  files.each do |f|
    new_name = f.sub(/^tpl/, 'out').sub(/\.haml$/, '.html')
    `haml #{f} > #{new_name}`
  end
end