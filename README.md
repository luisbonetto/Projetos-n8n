# 📊 Automação de Relatórios de Vendas com n8n

Este projeto consiste num fluxo de trabalho automatizado desenvolvido no **n8n** para otimizar a criação e o envio de relatórios comerciais. A automação recolhe dados de vendas, processa a informação e envia um relatório consolidado diretamente por e-mail.

---

## 🚀 Como Funciona o Fluxo (Workflow)

O fluxo de trabalho é composto por 5 etapas principais:

1. **Trigger Manual (`When clicking 'Execute workflow'`):** Permite iniciar a execução do fluxo manualmente com um clique.
2. **Google Sheets (`Get row(s) in sheet`):** Acede à folha de cálculo para recolher todos os registos e dados de vendas atualizados.
3. **Processamento (`Summarize`):** Agrupa e resume os dados recolhidos para destacar as métricas comerciais mais relevantes.
4. **Conversão de Ficheiro (`Convert to File`):** Transforma os dados resumidos num formato estruturado (`.xlsx` - Excel).
5. **Envio por E-mail (`Send a message` / Gmail):** Envia automaticamente o relatório convertido como anexo para os destinatários definidos.

---

## 🛠️ Tecnologias Utilizadas

* **[n8n](https://n8n.io/)** - Plataforma de automação de workflows.
* **Google Sheets API** - Fonte de dados para o registo de vendas.
* **Gmail API** - Envio automatizado do relatório final.
* **Formatos:** JSON, XLSX.

---

## ⚙️ Como Importar o Fluxo

1. Descarrega o ficheiro `workflow.json` deste repositório.
2. Abre o teu painel do n8n, vai a **Workflows** e clica em **Import from File**.
3. Configura as tuas credenciais do **Google Sheets** e do **Gmail** nas respetivas nodas.
