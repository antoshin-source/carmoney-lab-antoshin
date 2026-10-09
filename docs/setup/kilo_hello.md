# Kilo hello

готов.

1) Сервис: учебный проект carmoney-lab — предварительная оценка заявки на заём под ПТС (VIN, год, пробег, оценочная стоимость, сумма, срок), считает LTV и возвращает решение `approve` / `review` / `reject`.
2) Команды: Makefile — `make up` (поднять сервис и базу), `make down`, `make ps`, `make logs`, `make install`, `make test` (PHPUnit), `make lint` (php -l), `make seed`, `make help`; docker-compose.yml — сервисы `backend` (PHP, порт `${APP_PORT:-8080}:8080`) и `db` (mysql:8.0, порт `${DB_PORT:-3307}:3306`, healthcheck, инициализация из db/schema.sql и db/seed.sql).
3) Решение approve / review / reject считается в папке `backend/src/Domain` (DecisionEngine.php, AssessmentService.php), пороги — из backend/config/rules.php.

модель: training-2026-09-glm-5.3