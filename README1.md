1. First we need to build the IMAGE (Developer will build)
2. Push the Image to Hub.
3. All Images should be available in hub then we can define the dependency and run the containers. (docker compose helps in achieving it)

**docker-compose.yml**
 - can start all the containers at a time
 - can stop all at a time
 - define networking
 - define volumes

 **YAML**
 -- It is markup language
 --  

**Build all at once**
`for i in web mongodb catalogue user cart mysql shipping payment ratings; do cd $i ; docker build -t $i:v1 . ; cd .. ; done`

**Build and push all at once**
`for i in web mongodb catalogue user cart mysql shipping payment ratings; do cd $i ; docker build -t rohitsingirikonda/$i:v1 . ; docker push rohitsingirikonda/$i:v1 ; cd .. ; done`