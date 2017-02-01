Refer : https://github.com/Eugeny/ajenti-v

## Run
```
docker run -td --name ajenti-db imamdigmi/ajenti-db
docker run -d -p 8000:8000 -p 80:80 -p 443:443 -p 2222:22 -p 21:21 --volumes-from ajenti-db imamdigmi/ajenti
```

## Build it yourself
```
git clone https://github.com/imamdigmi/dockerize-ajenti.git && cd dockerize-ajenti
docker build -t ajenti .
docker run -d -p 8000:8000 -p 80:80 -p 443:443 -p 2222:22 -p 21:21 ajenti
```

## Browse
Visit [https://localhost:8000](https://localhost:8000) on your browser
default login : user `root` and password `admin`

## SSH Access
default ssh port `2222`
default logins `root/ch@ngem3`

on the docker-run command you can use different external ports than defaults for more security
ex  -p 7090:8000 , -p 2345:22  so it wont be obvious target for the attacker/viruses to try and hit your server.

Inspired by : whatpanel
