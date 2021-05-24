# What is viewtube-swarm
It is a docker swarm that has viewtube

# Requirements
Make sure you have this setup and installed **https://github.com/czadikem/core**

# viewtube-swarm Install
1.  ```git clone https://github.com/czadikem/viewtube-swarm.git```
2.  ```cd viewtube-swarm```
3.  ```rm data/blank.txt```  had to put in this github repository so github would not remove the data folder
4.  ```cp .env.template .env```
5.  ```nano.env``` Put your hostname for viewtube in this file along with the keys you generate in a browser **Below** Also "You can get three free hostnames from noip"
6.  # Generating keys
    * JWT_SECRET **Go to https://guidgenerator.com/ and click *Generate some GUIDS***
    * PUBLIC_VAPID and PRIVATE_VAPID **Go to https://tools.reactpwa.com/vapid put your email into the text box and click *Update subject email & re-generate keys***

# viewtube-swarm Deployment
1.  ```docker stack deploy -c <(docker-compose config) viewtube``` **You must be in the viewtube-swarm folder for this to work**

# viewtube-swarm Stop
1.  ```docker stack down viewtube```

# Acknowledgments
Thanks to https://github.com/ViewTube/viewtube-vue  and thanks too Oscar at https://silkky.cloud/ for helping me learn, setup and understand docker swarm
Also thanks to the wonderful people that created these sites https://tools.reactpwa.com/vapid, https://guidgenerator.com/
