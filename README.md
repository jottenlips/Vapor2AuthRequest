# Example requests for Vapor 3 Auth Api template
## Make a new template
### Install vapor using brew

```
brew install vapor/tap/vapor
```

### Make a new vapor authenticated api

https://github.com/vapor/auth-template

```
vapor new hello --auth
```

## Create user

### i-register

```
curl -X "POST" "http://localhost:8080/users" \
     -H 'Content-Type: multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__' \
     -F "email=" \
     -F "password=" \
     -F "name="
```

## Login

### i-login

```
curl -X "POST" "http://localhost:8080/login" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -u 'myemail:mypassord' \
     -d $'{}'
```

## Get protected data

### i-me

```
curl "http://localhost:8080/me?" \
     -H 'Authorization: Bearer mytokenhere' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'
```
