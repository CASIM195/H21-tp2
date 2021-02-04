# Exceptions

## Description

En temps qu'utilisateur du service, j'aimerais être en mesure de mieux comprendre les erreurs du serveur afin de pouvoir les éviter ou les corriger.

## Réponse

```ts
{
  code: string,
  message: string
}
```

### Exemple

`HTTP 400 BAD REQUEST`
```json
{
  "code": "INVALID_DATETIME",
  "message": "birthDate should follow the ISO-8601 standard"
}
```
