# Feature 1 - Création d'un produit (v2)

## Description

En temps que vendeur, je désire pouvoir ajouter un produit en vente.

## Requête

`HTTP POST /inventory`

```ts
{
  sellerId: string,
  name: string,
  description: string,
  initialPrice: number, // positif, arrondi à 2 décimales, min 1.00
  startTime: datetime, // ISO-8601 at UTC
  duration: number // **DAYS**, min 1 max 31
}
```

## Réponse

```
HTTP 201 CREATED
Headers:
  Location: string
```

... où le header `Location` contient l'URL vers le nouveau produit (`http://localhost:8080/api/inventory/{productId}`)

## Exceptions

| condition                  | status | erreur              |
| -------------------------- | ------ | ------------------- |
| `sellerId` inexistant      | 404    | `SELLER_NOT_FOUND`  |
| `startTime` mauvais format | 400    | `INVALID_DATETIME`  |
| `duration` invalide        | 400    | `INVALID_DATERANGE` |
| `initialPrice` invalide    | 400    | `INVALID_AMOUNT`    |
| champs vide                | 400    | `MISSING_FIELD`     |
