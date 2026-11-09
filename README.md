<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/rival-afk/zenoku-design/main/assets/auth/png/readme-banner-dark.png">
    <img src="https://raw.githubusercontent.com/rival-afk/zenoku-design/main/assets/auth/png/readme-banner.png" alt="auth" width="440">
  </picture>
</p>

# auth

rival-auth — единый сервис авторизации инфраструктуры zenoku (`auth.rival-afk.com`): HTTP API, JWT/HMAC-токены для [rsh](https://github.com/rival-afk/rsh) и прочих сервисов, SSH-шлюз и jump-хост к домашним узлам.

## Что внутри

- HTTP API с автоматическим TLS (ACME/autocert), DNS-01 челленджи
- выпуск и проверка JWT/HMAC-токенов, SQLite-хранилище
- SSH-шлюз: авторизация и проброс к узлам (permitopen по порту таргета)
- инструменты: `wcman`, `mindpage`, `mcproto`, `rustlings` и пр. (см. `main.go`, `tools/`)

Лого и бренд-ассеты — в [rival-afk/zenoku-design](https://github.com/rival-afk/zenoku-design).

## Сборка

```sh
go build -o rival-auth .     # Go 1.27
```
