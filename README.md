# Internet
Checking internet from time to time and saving it in a database

## docker images
For *desktop devices*
```
docker pull amanajas/speedtest
```
For *arm* devices*
```
docker pull amanajas/speedtest:arm
```

## install local
```
pip install -r requirements.txt
```
## run
the first part in background
```
python runner.py&
```
***AND*** the rest api
```
python api.py
```
***OR***
easily execute
```
./scripts/wrapper.sh
```

## docker
```
docker build -t speedtest .
docker run --restart=always -d -p <port>:<port> -it speedtest
```
## api

- Port exposed: ***5000*** *if no port defined in the environment*
- Route: **/speed**
- (local) host: **[127.0.0.1](http://127.0.0.1:5000/)**
