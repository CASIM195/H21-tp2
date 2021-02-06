# Feature 4 - Création d'un vendeur

## Description

En tant que commerçant, j'aimerais pouvoir me créer un compte afin de vendre mes produits.

## Requête

`POST /seller`

```ts
{
  name: string,
  description: string
}
```

## Réponse

```
HTTP 201 CREATED
Headers:
  Location: string
```

... où le header `Location` contient l'URL vers le nouveau vendeur (`http://localhost:8080/api/seller/{sellerId}`)

## Exceptions

| condition   | status | erreur          |
| ----------- | ------ | --------------- |
| champs vide | 400    | `MISSING_FIELD` |
