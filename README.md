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

### register

```
## i-register
curl -X "POST" "http://localhost:8080/users" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "name": "",
  "email": "",
  "password": ""
}'

```

## Login

### login

```
curl -X "POST" "http://localhost:8080/login" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -u 'myemail:mypassord' \
     -d $'{}'
```

returns `token` to be used for protected routes.

## Get protected data

### me

```
curl "http://localhost:8080/me?" \
     -H 'Authorization: Bearer mytokenhere' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'
```
