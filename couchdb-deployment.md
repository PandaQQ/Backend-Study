# CouchDB Deployment on Ubuntu 16.04


#### Step 1 - Installing CouchDB
```bash
$ mkdir temp
$ cd temp
$ wget https://raw.githubusercontent.com/afiskon/install-couchdb/master/install-couchdb.sh
$ sh install-couchdb.sh
# then see http://localhost:5984/_utils/
```
This will install CouchDB  on your server.

By default, CouchDB runs on localhost and uses the port 5984. You can retrieve this basic information by running curl from the command line:
```bash
$ curl localhost:5984 
```

Note: If you don't have curl installed, you can use the sudo apt-get install curl command to install it.

You should get something similar to the following:

```javascript
{
  "couchdb":"Welcome",
  "uuid":"b9f278c743b5fc0b971c4e587d77582e",
  "version":"2.0.0",
  "vendor":{
      "name":"Ubuntu",
      "version":"14.04"
  }
}
```

#### Step 2 - 
- After installation need to modify config to let couchdb accessible by remote host
``` bash
$ sudo vim /home/couchdb/etc/local.ini

[chttpd]

...

;bind_address = 127.0.0.1
```
- uncomment bind_address under [chttpd] and change the value to 0.0.0.0

- Also need to restart coucdb service so that couchdb can access

``` bash
$ sv status couchdb
$ sv restart couchdb
$ sv stop couchdb
```

- Finally we can access to couchdb with http://{ip_address}:5984/_utils/
