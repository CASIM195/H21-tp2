# Feature 3 - Affichage d'un produit

## Description

En tant qu'acheteur, je désire visualiser les détails d'un produit en vente.

## Requête

`GET /inventory/{productId}`

## Réponse

`HTTP 200 OK`
```ts
{
  id: string,
  name: string,
  sellerId: string,
  description: string,
  initialPrice: number, // 2 decimals
  currentPrice: number, // 2 decimals
  startTime: datetime, // ISO-8601 at UTC
  endTime: datetime // ISO-8601 at UTC
}
```

## Exceptions

| condition              | status | erreur              |
| ---------------------- | ------ | ------------------- |
| `productId` inexistant | 404    | `PRODUCT_NOT_FOUND` |
