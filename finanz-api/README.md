# Finanz API (`finanz-api/`)

API REST para gestion de presupuesto personal construida con Spring Boot, Spring Data JPA e H2.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/fcomartin94/finanz-core)

Si buscas una version corta y orientada a portfolio/demo, revisa `README_PUBLIC.md`.

---

## Ejecucion rapida

Desde la raiz del repositorio:

```bash
cd finanz-api
./mvnw spring-boot:run
```

La API queda disponible en `http://localhost:8080`.

Probar rapido:

```bash
curl http://localhost:8080/api/saldo
```

Tests:

```bash
./mvnw test
```

---

## Endpoints principales

- `POST /api/transacciones`
- `POST /api/transacciones/simple`
- `GET /api/transacciones`
- `GET /api/transacciones/{id}`
- `DELETE /api/transacciones/{id}`
- `GET /api/saldo`
- `GET /api/saldo/mes-actual`
- `GET /api/resumen/mes-actual`

---

## Estructura tecnica

```text
finanz-api/src/main/java/com/finanzapi/
├── FinanzApiApplication.java
├── controller/
├── service/
├── repository/
└── model/
```

---

## Configuracion

- Perfil local: `src/main/resources/application.properties`
- Perfil cloud: `src/main/resources/application-cloud.properties`
- Guia de despliegue: `DEPLOY.md`

---

## Relacion con el monorepo

- `finanz-core/` contiene la version CLI del mismo dominio.
- `finanz-app/` contiene la app Android.
- `finanz-api/` es la capa backend HTTP para el mismo modelo de negocio.
