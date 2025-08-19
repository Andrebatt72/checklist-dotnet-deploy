# Checklist para Deploy de Sistemas .NET no Azure App Service/IIS

# Checklist para Deploy de Sistemas .NET no Azure App Service/IIS

![Exemplo de erro de dependência faltante no Azure App Service](https://www.sistemasave.com.br/img/errodeployazure.jpg)

> Exemplo real de erro: falta da DLL NLog no pacote publicado impede o start do app no Azure App Service.

## 1. Publicação do Projeto
- [ ] Gerar o pacote publicado com:

```bash
dotnet publish -c Release -o ./publish
```

- [ ] Compactar todo o conteúdo da pasta `publish` em um arquivo `.zip` (não a pasta, mas o conteúdo dela).
## 2. Itens a serem enviados

- [ ] Arquivo `.zip` do conteúdo da pasta publish.
- [ ] Arquivo `.csproj` do projeto principal.
- [ ] Exemplo de `appsettings.json` (sem secrets reais).
- [ ] Documentação de variáveis de ambiente obrigatórias.
- [ ] Instruções de configuração especial (se houver).
## 3. Conteúdo do pacote publicado

- [ ] Todas as DLLs e arquivos `.exe` necessários.
- [ ] Pasta `wwwroot` completa (para apps web).
- [ ] Arquivos de configuração: `appsettings.json`, `web.config`, etc.
- [ ] Outras dependências (arquivos estáticos, libs nativas, etc).

## 4. Observações
- [ ] O pacote publicado deve funcionar tanto no Azure App Service quanto no IIS.
- [ ] Informar se há dependências externas (serviços, storage, etc).
- [ ] Informar se há configurações específicas para ambiente de produção.
---

## Modelo de E-mail para Solicitação

**Assunto:** Solicitação de pacote publicado (.NET) para deploy no Azure App Service/IIS
Olá [Nome do responsável],

Estou organizando a migração de nossos sistemas para o Azure App Service e preciso garantir que o deploy seja feito de forma correta e padronizada. Para isso, solicito o envio do pacote publicado do sistema, gerado via comando:

```
dotnet publish -c Release -o ./publish
```

**Por favor, envie:**

- O arquivo `.zip` contendo todo o conteúdo da pasta `publish` (não a pasta em si, mas todos os arquivos e subpastas gerados pelo publish).
- O arquivo `.csproj` do projeto principal.
- Um exemplo de `appsettings.json` (sem secrets/senhas reais).

**Observações importantes:**

- O pacote publicado é o mesmo utilizado para deploy no Azure App Service e para rodar no IIS.
- Inclua todas as dependências, DLLs, arquivos de configuração e a pasta wwwroot.
- Se houver dependências externas, variáveis de ambiente obrigatórias ou configurações específicas, favor documentar.

Com esse material, conseguiremos realizar o deploy no Azure e, se necessário, rodar o sistema localmente no IIS.

Aguardo o envio para dar continuidade ao processo.

Obrigado!
# Checklist para Deploy de Sistemas .NET no Azure App Service/IIS

## 1. Publicação do Projeto
- [ ] Gerar o pacote publicado com:
  ```
  dotnet publish -c Release -o ./publish
  ```
- [ ] Compactar todo o conteúdo da pasta `publish` em um arquivo `.zip` (não a pasta, mas o conteúdo dela).

## 2. Itens a serem enviados
- [ ] Arquivo `.zip` do conteúdo da pasta publish.
- [ ] Arquivo `.csproj` do projeto principal.
- [ ] Exemplo de `appsettings.json` (sem secrets reais).
- [ ] Documentação de variáveis de ambiente obrigatórias.
- [ ] Instruções de configuração especial (se houver).

## 3. Conteúdo do pacote publicado
- [ ] Todas as DLLs e arquivos `.exe` necessários.
- [ ] Pasta `wwwroot` completa (para apps web).
- [ ] Arquivos de configuração: `appsettings.json`, `web.config`, etc.
- [ ] Outras dependências (arquivos estáticos, libs nativas, etc).

## 4. Observações
- [ ] O pacote publicado deve funcionar tanto no Azure App Service quanto no IIS.
- [ ] Informar se há dependências externas (serviços, storage, etc).
- [ ] Informar se há configurações específicas para ambiente de produção.

---

## Modelo de E-mail para Solicitação

**Assunto:** Solicitação de pacote publicado (.NET) para deploy no Azure App Service/IIS

Olá [Nome do responsável],

Estou organizando a migração de nossos sistemas para o Azure App Service e preciso garantir que o deploy seja feito de forma correta e padronizada. Para isso, solicito o envio do pacote publicado do sistema, gerado via comando:

```
dotnet publish -c Release -o ./publish
```

**Por favor, envie:**
- O arquivo `.zip` contendo todo o conteúdo da pasta `publish` (não a pasta em si, mas todos os arquivos e subpastas gerados pelo publish).
- O arquivo `.csproj` do projeto principal.
- Um exemplo de `appsettings.json` (sem secrets/senhas reais).

**Observações importantes:**
- O pacote publicado é o mesmo utilizado para deploy no Azure App Service e para rodar no IIS.
- Inclua todas as dependências, DLLs, arquivos de configuração e a pasta wwwroot.
- Se houver dependências externas, variáveis de ambiente obrigatórias ou configurações específicas, favor documentar.

Com esse material, conseguiremos realizar o deploy no Azure e, se necessário, rodar o sistema localmente no IIS.

Aguardo o envio para dar continuidade ao processo.

Obrigado!
