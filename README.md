# Guia Profissional de Deploy .NET no Azure App Service com Bicep

Este documento apresenta o fluxo padronizado para migração e publicação de aplicações .NET no Azure App Service, com infraestrutura provisionada via Bicep. Inclui checklist técnico, boas práticas e exemplo real de erro para garantir confiabilidade e padronização.

---

## ✅ Checklist Técnico para Deploy

### 1. Publicação do Projeto

Utilize o comando abaixo para gerar o pacote publicado:

```bash
dotnet publish -c Release -o ./publish
