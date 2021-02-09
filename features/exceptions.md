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

### Champ vide ou manquant

Pour toute forme de requête `POST`, si un champs est manquant ou vide (`null` ou `""`), vous devez retourner le code `MISSING_FIELD` ainsi que le status `400 BAD REQUEST`. Le message d'erreur doit en tout temps être explicatif et clair.
