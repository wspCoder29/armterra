# 🌍 Ambiente Azure + Deploy via Terraform (IaC)

Este repositório contém a construção de um ambiente em **Azure** utilizando **Kubernetes clusters** e sua conversão para **Terraform**, possibilitando a aplicação prática do conceito de **Infrastructure as code (IaC)**.

---

## 📌 Visão Geral

-  **Criação do ambiente**: Feita via **portal Azure**, conforme o tutorial da **aula 7**.
-  **Conversão para Terraform**: Utilizando a ferramenta [aztfexport](https://github.com/Azure/aztfexport).
-  **Automação do deploy**: Verificação da viabilidade de gerenciar o ambiente via Terraform.

---

## Evidência do Ambiente rodando no Portal, antes do destroy



![Ambiente no Azure](evidencia01q.png)

---

## 🛠️ Conversão do Ambiente para Terraform

Para facilitar a conversão do ambiente para Terraform, utilizei a ferramenta **[aztfexport](https://github.com/Azure/aztfexport)**.

### ⚠️ Problema Encontrado
Cometi um erro ao interpretar as instruções da ferramenta:
- Pensei que o **aztfexport** utilizava o **ARM template** gerado no portal da Azure.
- **Deletei o ambiente** antes de rodar o **aztfexport**.
- Descobri que a ferramenta **precisa do ambiente rodando** para capturar seu estado e convertê-lo para Terraform.
- Tenho salvos os arquivos do meu ambiente ARM template (template.json e parameters.json)

---

## 🔄 Próximos Passos

✅ **1. Redeploy do ambiente** seguindo os passos da **aula 7**  
✅ **2. Utilizar aztfexport** para gerar os arquivos `.tf`  
✅ **3. Testar o deployment via Terraform e demonstrar apicação prática de IaC**  
✅ **4. Corrigir possíveis bugs** resultantes da conversão  
✅ **5. Redeploy via Terraform** e validação do ambiente  
✅ **6. Conferência dos logs do pod** para verificação de erros  

---

📌 **Objetivo Final:**  
Garantir que o ambiente seja provisionado corretamente via **Terraform**, sem dependência do portal da Azure.  


