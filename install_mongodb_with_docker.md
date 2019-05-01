#### 1. Install MonogoDb firstly
```bash
docker run -d \ 
           -p 27017:27017 \ 
           --name mongodb \ 
           -e MONGO_INITDB_ROOT_USERNAME=mongoadmin \
           -e MONGO_INITDB_ROOT_PASSWORD=mongoadmin \
           mongo
```

#### 2. And then install mongo-express secondly
```bash
docker run -it --restart=always \ 
              --name mongo-express \ 
              --link mongodb:mongo \ 
              -d -p 8081:8081 \ 
              -e ME_CONFIG_OPTIONS_EDITORTHEME="3024-night"   \ 
              -e ME_CONFIG_BASICAUTH_USERNAME="mongoexpress"  \ 
              -e ME_CONFIG_BASICAUTH_PASSWORD="mongoexpress"  \ 
              -e ME_CONFIG_MONGODB_ADMINUSERNAME="mongoadmin" \ 
              -e ME_CONFIG_MONGODB_ADMINPASSWORD="mongoadmin" \ 
              mongo-express
```
