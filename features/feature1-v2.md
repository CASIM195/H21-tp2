# Feature 1 - Création d'un produit (v2)

## Description

En temps que vendeur, je désire pouvoir ajouter un produit en vente.

## Requête

`HTTP POST /inventory`
```ts
{
  sellerId: string,
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

... où le header `Location` contient l'URL vers le nouvel item publié (`http://localhost:8080/api/inventory/{productId}`)

## Exceptions

| condition                     | status | erreur              |
| ----------------------------- | ------ | ------------------- |
| `sellerId` inexistant         | 404    | `SELLER_NOT_FOUND`  |
| `name` trop long              | 400    | `TEXT_TOO_LONG`     |
| `description` trop long       | 400    | `TEXT_TOO_LONG`     |
| `startTime` mauvais format    | 400    | `INVALID_DATETIME`  |
| `duration` trop long          | 400    | `INVALID_DATERANGE` |
| `initialPrice` mauvais format | 400    | `INVALID_AMOUNT`    |
| champs vide                   | 400    | `MISSING_FIELD`     |
