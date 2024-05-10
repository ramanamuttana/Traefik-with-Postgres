# Traefik with Postgres and Pgadmin4
Traefik with postgres and pgadmin

# Run traefik

<h3>Traefik with Docker on Ubuntu</h3>

<strong><i>Note</i></strong> : Make sure docker is up and running .

1) Pull the image from dockerhub:  ``docker pull traefik`` or a particular version , for Example:

       docker pull traefik:v3.0

       docker pull postgres

       docker pull dpage/pgadmin4
      
3) Open terminal and type ``sudo nano /etc/hosts`` , if you are using <b>nano</b> or else <b>vi</b> or with someother editor.

4) Enter ``127.0.0.1``   ``traefik.testing.de`` ``pgadmin.testing.de`` ``postgres.testing.de`` add all the domain names by giving the space between them )  according to the ``traefikwithpostgres.yaml`` ,
 
    or
  
       127.0.0.1 traefik.testing.de
  
       127.0.0.1 postgres.testing.de

       127.0.0.1 pgadmin.testing.de
   

   we can change according to our request.If we want to change the domain name , change in the traefiklatest.yaml file and in the hosts file.

6) save by typing <b>ctrl+x</b> enter <b>Y</b> to save and click on <b>ENTER</b> button 

7) Go to the yaml file directory and then open Terminal and type :``docker compose -f traefikwithpostgres.yaml up``

8) Open browser and type ``traefik.testing.de``

 # Dashboard

  ![alt text](https://github.com/ramanamuttana/traefik/blob/main/Screenshot%202024-04-03%20at%2018.49.12.png?raw=true)

# Pgadmin
 
1) Open browser and type ``pgadmin.testing.de``
       
       Pgadmin credentials :
       
       Username: admin@example.com
       Password: admin

<h2> UI</h2>

<h3>General</h3> 

**Name**: Should be service name according to Traefikwithpostgres.yaml for Example: `Postgresql`

**Shared Username:** `myuser`

<h3>Connection With DB(Postgres)</h3>

 ![alt text](https://github.com/ramanamuttana/TraefikwithPostgres/blob/main/Images/pgadminconnection1.png?raw=true)
       
<p>2)Connection Settings</p>

 ![alt text](https://github.com/ramanamuttana/TraefikwithPostgres/blob/main/Images/pgadminwithpostgres2.png?raw=true)



 ![alt text](https://github.com/ramanamuttana/TraefikwithPostgres/blob/main/Images/pgadminUI.png?raw=true)

# Stop All Running Containers
 1) Enter <b>Ctrl+c</b> on Terminal , all the containers will be stopped .
