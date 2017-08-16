IMAGE_NAME = "zenspider/emacs-ruby"

task :image do
  sh "docker build --rm -t #{IMAGE_NAME} ."
end

task :push do
  sh "docker push #{IMAGE_NAME}:latest"
end
