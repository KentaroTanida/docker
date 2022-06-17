## マニュアル

### docker build

```
docker build -t node/server_react .
```


### docker run 
```
docker run -it -p 3000:3000 --rm --mount type=bind,src=`pwd`/my-app,dst=/usr/src/app -d node/server_react
```

### docker run 後、Node実行
```
docker exec -it 9204b81c16c7 sh -c "npm start"
npm start
```