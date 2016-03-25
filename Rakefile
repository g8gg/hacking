desc "Push to github"
task :push do
  puts   "Pushing to `master' branch:"
  system "git push origin master"
  puts   "`master' branch updated."
  puts

  puts   "Building site...."
  system "jekyll build"
  puts   "Site updated."
  puts
  cd '_site' do
    puts   "Pushing to `gh-ages' branch:"
    system "git add -A"
    system "git commit -m 'update at #{Time.now.utc}'"
    system "git push origin gh-pages"
    puts   "`gh-pages' branch updated."
  end
end