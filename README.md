# Traefik with Postgres and Pgadmin 
Traefik with postgres and pgadmin

# Run traefik

<h3>Traefik with Docker on UBUNTU</h3>

<strong><i>Note</i></strong> : Make sure docker is up and running .

1) Pull the image from dockerhub:  ``docker pull traefik`` or particular version for Example: ``docker pull traefik:v3.0``
   
2) Open terminal and type ``sudo nano /etc/hosts`` , if you are using <b>nano</b> or else <b>vi</b> or with someother editor.

3) Enter ``127.0.0.1``   ``traefik.testing.de`` ``whoami.testing.de``( add all the domain names by giving the space between them )  according to the ``traefiklatest.yml`` ,
 
    or
  
       127.0.0.1 traefik.testing.de
  
       127.0.0.1 whoami.testing.de
  

   we can change according to our request.If we want to change the domain name , change in the traefiklatest.yaml file and in the hosts file.

4) save by typing <b>ctrl+x</b> enter <b>Y</b> to save and click on <b>ENTER</b> button 

5) Go to the yaml file directory and then open Terminal and type :``docker compose -f traefiklatest.yml up``

6) Open browser and type ``traefik.testing.de``

 # Dashboard

  ![alt text](https://github.com/ramanamuttana/traefik/blob/main/Screenshot%202024-04-03%20at%2018.49.12.png?raw=true)

# Stop Traefik 
 1) Enter <b>Ctrl+c</b> on Terminal , all the containers will be stopped .

![alt text](https://github.com/ramanamuttana/TraefikwithPostgres/blob/main/Screenshot%202024-04-17%20at%2013.36.09.png?raw=true)
