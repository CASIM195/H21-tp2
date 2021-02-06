# Feature 5 - Affichage d'un vendeur

## Description

En tant qu'utilisateur du service, je désire visualiser les détails d'un vendeur.

## Requête

`GET /seller/{sellerId}`

## Réponse

`HTTP 200 OK`

```ts
{
  id: string,
  name: string,
  description: string,
  createdAt: datetime // ISO-8601 at UTC
}
```

## Exceptions

| condition             | status | erreur             |
| --------------------- | ------ | ------------------ |
| `sellerId` inexistant | 404    | `SELLER_NOT_FOUND` |
