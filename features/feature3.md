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
  initialPrice: number, // arrondi à 2 décimales
  currentPrice: number, // arrondi à 2 décimales
  startTime: datetime, // ISO-8601 at UTC. exemple: "2020-01-01T00:00:00Z"
  endTime: datetime // ISO-8601 at UTC. exemple: "2020-01-01T00:00:00Z"
}
```

## Exceptions

| condition              | status | erreur              |
| ---------------------- | ------ | ------------------- |
| `productId` inexistant | 404    | `PRODUCT_NOT_FOUND` |
