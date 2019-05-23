### abstruct
Example implementations of using oauth2-server.
(using slim framework)

### what you need
php (>= 7.0), composer

### how it works
1. ```composer install```
2. ```openssl genrsa -out private.key 2048```
3. ```openssl rsa -in private.key -pubout > public.key```
4. ```cd public```
5. ```php -S localhost:3000```

then, access with below
```
curl -X "POST" "http://localhost:3000/client_credentials.php/access_token" \
	-H "Content-Type: application/x-www-form-urlencoded" \
	-H "Accept: 1.0" \
	--data-urlencode "grant_type=client_credentials" \
	--data-urlencode "client_id=myawesomeapp" \
	--data-urlencode "client_secret=abc123" \
	--data-urlencode "scope=basic email"

```
