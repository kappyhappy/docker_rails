#precondition
one of those listed below is installed.
docker for mac / docker for windows / docker toolbox for mac / docker toolbox for windows 

#commands to create rails 5.0 environment using docker
git clone https://github.com/kappyhappy/docker_rails

cd docker_rails

docker-compose run web rails new . --force --database=mysql


