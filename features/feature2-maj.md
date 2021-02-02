# Feature 2 - Mise à jour

## Description

En temps qu'utilisateur du service, je désire pouvoir visionner l'ensemble des offres publiées.

## Requête

```
HTTP GET /inventory
```

## Réponse

```
HTTP 200 OK
```
```ts
{
  items: [
    {
      id: string,
      name: string,
      publisher: string,
      description: string,
      currentPrice: number, // 2 decimals
      endTime: datetime // ISO-8601 at UTC
    }
  ]
}
```
