#### This is the process I used to deploy to my cluster. you will need to make changes for yours.

Follow along at https://youtu.be/lRae2jJfuqA

Or join me on Twitch, Tuesday-Thursday (2-5pm pacific) for homelab stuff fridays and randomly for gaming

https://twitch.tv/attentiontoodetail


# drone.io install doc:

requirements:  
  kubernetes (version?) v1.29.5 tested  
  postgres (version?) PostgreSQL 15.7 tested  
    
  ports:  
    80:80  
    
Steps:  
  - Create shared secret:     
    - openssl rand -hex 16  
  - Create an OAuth Application in gitea  
    - clientid:   
    - secrat:  
  - Create secret housing above: droneio  
    - clientid:   
    - secrat:   
    - rpc-secrat:   
  - create database on postgres server:  
    - server:  
    - CREATE USER droneiodev WITH PASSWORD '';  
    - CREATE DATABASE droneiodev with OWNER=droneiodev;  
  - restart database to make the user take effect  
  - create postgres password secret: droneio-psql  
    - secret: xxxxxxxxxxx  
    
  - Deploy yaml files to cluster   

    
