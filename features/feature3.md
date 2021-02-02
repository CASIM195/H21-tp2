# Feature 3

## Description

En tant qu'utilisateur du service, je désire visualiser les détails d'un produit en vente.

## Requête

`GET /inventory/{id}`

## Réponse

`HTTP 200 OK`
```ts
{
  id: string,
  name: string,
  publisher: string,
  description: string,
  initialPrice: number, // 2 decimals
  currentPrice: number, // 2 decimals
  startTime: datetime, // ISO-8601 at UTC
  endTime: datetime // ISO-8601 at UTC
}
```

## Exceptions

| condition       | status | erreur              |
| --------------- | ------ | ------------------- |
| `id` inexistant | 404    | `PRODUCT_NOT_FOUND` |
