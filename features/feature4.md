# Feature 4

## Description

En tant qu'utilisateur, j'aimerais pouvoir me créer un compte utilisateur afin de conserver certaines informations utiles.

## Requête

`POST /account`
```ts
{
  name: string, // max 30 caractères,
  birthDate: datetime, // ISO-8601
}
```

## Réponse

```
HTTP 201 CREATED
Headers:
  Location: string
```

... où le header `Location` contient l'URL vers le nouveau utilisateur (`http://localhost:8080/api/account/{id}`)
