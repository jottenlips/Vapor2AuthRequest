# Example requests for Vapor 3 Auth Api template
## Make a new template
### Install vapor using brew

```
brew install vapor/tap/vapor
```

### Make a new vapor authenticated api

```
vapor new hello --auth
```

## Create user

### i-register

```
curl -X "POST" "http://localhost:8080/users" \
     -H 'Content-Type: multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__' \
     -F "email=johno@aloompa.com" \
     -F "password=john" \
     -F "name=john"
```

## Login

### i-login

```
curl -X "POST" "http://localhost:8080/login" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -u 'johno@aloompa.com:john' \
     -d $'{
  "email": "johno1@aloompa.com",
  "id": "1",
  "password": "john",
  "name": "john"
}'
```

## Get protected data

### i-me

```
curl "http://localhost:8080/me?token=%2BP6ni9TkzoCSkxepU%2FDH5Q%3D%3D" \
     -H 'Authorization: Bearer tVhHQc4+L+59escVr0P4PQ==' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'
```
