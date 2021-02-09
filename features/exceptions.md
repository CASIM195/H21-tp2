# Exceptions

## Description

En temps qu'utilisateur du service, j'aimerais avoir plus d'information concernant les erreurs du serveur afin de mieux les éviter ou les corriger.

## Critères de succès

| critère | description                                                                                                                                                                   |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| C1      | Un status HTTP d'erreur est présent                                                                                                                                           |
| C2      | Pour toute forme de requête `POST`, si un champs est manquant ou vide (`null` ou `""`), le code d'erreur `MISSING_FIELD` ainsi que le status `400 BAD REQUEST` sont renvoyés. |
| C3      | Pour toute erreure inconnue, le code d'erreur `UNKNOWN_ERROR` ainsi que le tatus `500 INTERNAL SERVER ERROR` sont renvoyés.                                                   |
| C4      | Le message d'erreur doit en tout temps être explicatif et clair                                                                                                               |

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
