#precondition  
one of those listed below is installed.  
docker for mac / docker for windows / docker toolbox for windows  

#commands to create rails 5.0 environment using docker  
git clone https://github.com/kappyhappy/docker_rails  
cd docker_rails  

#create rails project  
docker-compose run web rails new . --force --database=mysql  

#build rails project  
docker-compose build  

#modify default password and host.  
vi config/database.yml  

#in my case, default part is started from row number 12.  
<p>  
default: &default  
  adapter: mysql2  
  encoding: utf8  
  pool: 5  
  username: root  
  password: password  
  host: db  
</p>  

#update db settings  
docker-compose up -d  

#check current docker status  
docker-compose ps  

#create db if not exists  
docker-compose run web bundle exec rake db:create  

#check whether rails screen is available when accessing to localhost:3000 with your browser  
localhost:3000  

#if you use docker toolbox for windows, check IP first and try to see with your browser  
docker-machine ip default

#type IP checked above instead of localhost 
http://IP:3000  