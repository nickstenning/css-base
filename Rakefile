task :default => [:sass, :haml]

task :sass do
  %w( screen ie print ).each do |x|
    `sass -t compressed sass/#{x}.sass > out/#{x}.css`
  end
end

task :haml do
  files = FileList['tpl/*.haml']
  
  files.each do |f|
    new_name = f.sub(/^tpl/, 'out').sub(/\.haml$/, '.html')
    `haml #{f} > #{new_name}`
  end
end