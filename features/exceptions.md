# Exceptions

## Description

En temps qu'utilisateur du service, j'aimerais avoir plus d'information concernant les erreurs du serveur afin de mieux les éviter ou les corriger.

## Critères de succès

| critère | description                                                                                                                                                                   |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| C1      | Un status HTTP d'erreur (4xx ou 5xx) est présent.                                                                                                                             |
| C2      | Un code d'erreur est présent.                                                                                                                                                 |
| C3      | Un message d'erreur explicatif et clair est présent.                                                                                                                          |
| C4      | Pour toute forme de requête `POST`, si un champs est manquant ou vide (`null` ou `""`), le code d'erreur `MISSING_FIELD` ainsi que le status `400 BAD REQUEST` sont renvoyés. |
| C5      | Pour toute erreure inconnue, le code d'erreur `UNKNOWN_ERROR` ainsi que le tatus `500 INTERNAL SERVER ERROR` sont renvoyés.                                                   |
| C6      | **Aucune** erreur préformattée par Jersey ne doit se rendre au client.                                                                                                        |

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
