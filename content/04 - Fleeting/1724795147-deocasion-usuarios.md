---
id: 1724795147-deocasion-usuarios
aliases:
  - deocasion-usuarios
tags: []
---

# Creacion de usuario:

## historia:

https://mrmisti.atlassian.net/browse/DO-96

## endpoints:

Para crear el usuario: `/api/v1/user-management/create-user`

## endpoints dependientes

Para obtener la lista de organizaciones:
`/api/v1/organization-management/find-organizations` Para obtener la lista de
roles: `/api/v1/role-configuracion/find-roles`

> Nota: lo que era antes find-organizations que devolvia un endpoint paginado
> ahora devuelve una lista sin paginar, esta funcionalidad paso a
> find-organizations-paginated

## Detalles

todos los tipo de usuario:

```ts
export enum UserType {
  SuperAdmin = "SUPER_ADMIN", //Super Adminitrador
  PlatformAdmin = "PLATFORM_ADMIN", // Administrador de plataforma
  PlatformUser = "PLATFORM_USER", // Usuario plataforma
  OrganizationAdmin = "ORGANIZATION_ADMIN", // Adminitrador de organizacion
  OrganizationUser = "ORGANIZATION_USER", // Usuario de organizacion
  Participant = "PARTICIPANT", // Participante
}
```

- El formulario debe permite crear todos los tipos menos `SuperAdmin` y
  `Participant`
- Si el tipo de usuario es `OrganizationAdmin` o `OrganizationUser` el select de
  organizacion no debe ser multiple, solo podra elegir uno
