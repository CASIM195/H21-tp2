# Feature 4 - Création d'un vendeur

## Description

En tant que commerçant, j'aimerais pouvoir me créer un compte afin de vendre mes produits.

## Requête

`POST /seller`
```ts
{
  name: string, // max 30 caractères,
  description: string // max 200 caractères
}
```

## Réponse

```
HTTP 201 CREATED
Headers:
  Location: string
```

... où le header `Location` contient l'URL vers le nouveau utilisateur (`http://localhost:8080/api/seller/{sellerId}`)

## Exceptions

| condition               | status | erreur          |
| ----------------------- | ------ | --------------- |
| `name` trop long        | 400    | `TEXT_TOO_LONG` |
| `description` trop long | 400    | `TEXT_TOO_LONG` |
