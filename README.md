# Example requests for Vapor Auth Api template
## Make a new template
### Install vapor using brew

```brew install vapor/tap/vapor```

### Make a new vapor authenticated api

https://docs.vapor.codes/3.0/auth/getting-started/

```
vapor new hello --auth
```
```
cd hello
```

then

```
vapor build
```
```
vapor run
``` 
or
```
vapor xcode
```

## Create user # VAPOR 3

```
curl -X "POST" "http://localhost:8080/users" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "name": "",
  "email": "",
  "password": "",
  "verifyPassword = ""
}'

```

## Login

```
curl -X "POST" "http://localhost:8080/login" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -u 'myemail:mypassord' \
     -d $'{}'
```

returns `token` to be used for protected routes.

## Todo object

### get todo

```
curl "http://localhost:8080/todos?" \
     -H 'Authorization: Bearer mytokenhere' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'
```

### post todo

```
curl -X "POST" "http://localhost:8080/todos" \
     -H 'Authorization: Bearer 0BMDp6YeOuH0qYYrXInDhA==' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "title": "Do the dishes"
}'
```
### delete todo
```
curl -X "DELETE" "http://localhost:8080/todos/1" \
     -H 'Authorization: Bearer 0BMDp6YeOuH0qYYrXInDhA==' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'
```

## Create user # VAPOR 2

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
