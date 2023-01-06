# Spring Security JWT: How to secure your Spring Boot REST APIs with JSON Web Tokens
Just the code sample from a YouTube tutorial regarding Spring Security implementing Jwt using RSA.

- Youtube link: https://www.youtube.com/watch?v=KYNR5js2cXE
- Article link: https://www.danvega.dev/blog/2022/09/06/spring-security-jwt/

## Tech stack:
- [X] Spring Boot
- [X] JWT
- [X] Spring Security
- [X] RSA

## RSA PUBLIC & PRIVATE KEYS:
- Create rsa key pair
```bash
openssl genrsa -out keypair.pem 2048
```

- Extract public key
```bash
openssl rsa -in keypair.pem -pubout -out public.pem
```

- Create private key in PKCS#8 format
```bash
openssl pkcs8 -topk8 -inform PEM -outform PEM -nocrypt -in keypair.pem -out private.pem
```