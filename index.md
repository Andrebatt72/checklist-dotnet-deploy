# Checklist  de Deploy .NET no Azure App Service

> **Atenção:** Siga este checklist antes de enviar o pacote para deploy. 

---

## 1. Publicação do Projeto
- Gere o pacote publicado com:
  ```bash
  dotnet publish -c Release -o ./publish
  ```
- Compacte **apenas o conteúdo** da pasta `publish` em um arquivo `.zip` (não a pasta, só os arquivos e subpastas gerados).

## 2. Itens Obrigatórios para Envio
- Arquivo `.zip` do conteúdo da pasta publish
- Arquivo `.csproj` do projeto principal
- Exemplo de `appsettings.json` (sem secrets reais)
- Documentação das variáveis de ambiente obrigatórias
- Instruções de configuração especial (se houver)

## 3. Conteúdo Esperado no Pacote
- Todas as DLLs e arquivos `.exe` necessários
- Pasta `wwwroot` completa (para apps web)
- Arquivos de configuração: `appsettings.json`, `web.config`, etc
- Outras dependências (arquivos estáticos, libs nativas, etc)

## 4. Validações Finais
- O pacote publicado deve funcionar tanto no Azure App Service quanto no IIS
- Informe dependências externas (serviços, storage, etc)
- Informe configurações específicas para ambiente de produção


<div align="center">
  <img src="https://www.sistemasave.com.br/img/errodeployazure.jpg" alt="Exemplo de erro de dependência faltante no Azure App Service" width="400"/>
  <br>
  <sub>Exemplo real: falta da DLL NLog no pacote publicado impede o start do app no Azure App Service.</sub>
</div>

---

