---
id: 1724779162-deocasion-sprint-4-2-3
aliases:
  - DeOcasion Sprint 4 2-3
tags:
  - deocasion
---

# DeOcasion Sprint 4

## Accesos Jira

- email: <fcary@novaly.com.pe>
- password: Ggej9db6$

## Tareas

### [Visualizacion de Pujas](https://novaly-team.atlassian.net/browse/PSD-55)

#### Detalles

- Se podra ver el boton de 'Ver pujas' y se quitara el boton de 'Anadir ofertas'
  cuando el evento tenga el estado
  'FINISHED'[figma](https://www.figma.com/design/7h5bUXzvQMQYmOc7jNNm4b/Subastas-UI?node-id=1727-58818&t=1gF1Kx63LP3LUSWz-4)
- La vista de visualizacion de pujas es
  [esta](https://www.figma.com/design/7h5bUXzvQMQYmOc7jNNm4b/Subastas-UI?node-id=1403-111987&t=1gF1Kx63LP3LUSWz-4)

#### Tech

- Endpoint: /v1/offer-management/find-offers-with-bid-paginated

```ts
type OfferWithBidDto = {
  id: string;
  title: string;
  appraisal: number;
  bid: {
    createdAt: string; // Iso Format
    amount: number;
    status: BidStatus;
  };
};

type BidStatus = {
  Base = "BASE"; // Base
  GivenUp = "GIVEN_UP"; // Desistida
  Winner = "WINNER"; // Ganadora
  Discarded = "DISCARDED"; // Descartada
}
```

### [Confirmacion de ofertas](https://novaly-team.atlassian.net/browse/PSD-37)

### [Debate de ofertas](https://novaly-team.atlassian.net/browse/PSD-38)

### [Retiro de ofertas](https://novaly-team.atlassian.net/browse/PSD-39)

### [Modificacion de tasaciones](https://novaly-team.atlassian.net/browse/PSD-41)

### [Historial de tasaciones](https://novaly-team.atlassian.net/browse/PSD-40)

### [Suspension de organizacion](https://novaly-team.atlassian.net/browse/PSD-20)

### [Publicacion de evento](https://novaly-team.atlassian.net/browse/PSD-33)

### [Inicio de evento](https://novaly-team.atlassian.net/browse/PSD-89)

### [Finalizacion de evento](https://novaly-team.atlassian.net/browse/PSD-90)

## Resumen reunion

## Links

- [Reunion](https://novalysac-my.sharepoint.com/personal/cflores_novaly_com_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fcflores%5Fnovaly%5Fcom%5Fpe%2FDocuments%2FRecordings%2FConsultas%20sprint%204%2D20240816%5F170217%2DGrabaci%C3%B3n%20de%20la%20reuni%C3%B3n%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E5d42ec70%2D442c%2D4ca3%2Dad8b%2Ded5230943b31)
