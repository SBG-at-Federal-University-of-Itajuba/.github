# Governança GitHub · SBG UNIFEI

## Objetivo

- Qualquer pessoa acessa repositórios **públicos**.
- Somente **Moderators** (e owners) modificam, criam repos e administram.

## Configuração aplicada (checklist)

1. Org `default_repository_permission` = **none** (membro sem role de time não escreve).
2. `members_can_create_repositories` = **false**.
3. Time **Moderators** com permissão **admin** nos repositórios da org.
4. Repositórios novos: dar acesso ao time Moderators (admin/maintain).
5. Branch `main` protegida (ruleset): PR obrigatório; Moderators/owners podem bypass se necessário.
6. Profile README em `.github/profile/README.md`.

## Adicionar um Moderator

```bash
gh api -X PUT orgs/SBG-at-Federal-University-of-Itajuba/teams/moderators/memberships/USERNAME -f role=member
```

## Adicionar membro só de leitura (sem escrita)

Convide para a org como **Member**. Com `default_repository_permission=none`, essa pessoa não ganha push automático.
