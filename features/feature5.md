# Feature 5

## Description

En tant qu'utilisateur du service, je désire renchérir sur un produit dans le but d'avoir une chance de l'obtenir.

## Requête

`POST /inventory/{id}/offer`

```ts
{
    accountId: string,
    amount: number // max 2 decimals
}
```

## Réponse

`HTTP 200 OK`

## Exceptions

| condition                                 | status | erreur              |
| ----------------------------------------- | ------ | ------------------- |
| `id` inexistant                           | 404    | `PRODUCT_NOT_FOUND` |
| `amount` format invalide, pas assez élevé | 400    | `INVALID_AMOUNT`    |
| enchère terminée                          | 400    | `BIDDING_CLOSED`    |
