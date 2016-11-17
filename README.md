# goapi2-autobuild
go1.6+echo2  
 
1.genSSL.sh  
2.rebuild.sh  

run ./goapi

ex:  
```
docker run -d -it -p 80:8888 -p 443:8443 --restart=on-failure:5 --name=api -v /home/app/api:/go bowwow/goapi2-autobuild
```  

```
docker run --rm -v /home/app/api:/go -w /go bowwow/goapi2-autobuild go get -d -v && go build -o goapi .  
```
