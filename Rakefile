IMAGE_NAME = "zenspider/emacs-ruby"
TAG_NAME   = "26.2_2.5.5p157_0"

task :image do
  sh "docker build --squash --rm -t #{IMAGE_NAME}:#{TAG_NAME} ."
  sh "docker tag #{IMAGE_NAME}:#{TAG_NAME} #{IMAGE_NAME}:latest"
end

task :push => :image do
  sh "docker push #{IMAGE_NAME}:#{TAG_NAME}"
  sh "docker push #{IMAGE_NAME}:latest"
end

task :sh do
  sh %(docker run --rm -i -t #{IMAGE_NAME}:#{TAG_NAME} /bin/sh)
end

task :purge do
  sh "docker system prune -f"
end

task :purgeall => :purge do
  sh "docker system prune -f -a"
end
