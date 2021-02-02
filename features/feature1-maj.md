# Feature 1 - Mise à jour

## Description

En temps qu'utilisateur du service, je désire pouvoir ajouter un item en vente.

## Requête

```
HTTP POST /inventory
```
```ts
{
  accountId: string,
  name: string, // max 40 caractères
  description: string, // max 500 caractères
  initialPrice: number, // 2 decimals
  startTime: datetime, // ISO-8601 at UTC
  duration: number // milliseconds, max 6 mois
}
```

## Réponse

```
HTTP 201 CREATED
Headers:
  Location: string
```

... où le header `Location` contient l'URL vers le nouvel item publié (`http://localhost:8080/api/inventory/{id}`)

## Exceptions

| condition                     | status | erreur              |
| ----------------------------- | ------ | ------------------- |
| `name` trop long              | 400    | `TEXT_TOO_LONG`     |
| `description` trop long       | 400    | `TEXT_TOO_LONG`     |
| `startTime` mauvais format    | 400    | `INVALID_DATE`      |
| `duration` trop long          | 400    | `INVALID_DATERANGE` |
| `initialPrice` mauvais format | 400    | `INVALID_AMOUNT`    |
| champs vide                   | 400    | `MISSING_FIELD`     |
