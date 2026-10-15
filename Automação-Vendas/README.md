# 📊 Automação de Relatórios de Vendas com n8n

Este projeto consiste num fluxo de trabalho automatizado desenvolvido no **n8n** para otimizar a criação e o envio de relatórios comerciais. A automação recolhe dados de vendas, processa a informação e envia um relatório consolidado diretamente por e-mail.

---

## 🚀 Como Funciona o Fluxo (Workflow)

O fluxo de trabalho é composto por 5 etapas principais:

## 🚀 Como Funciona o Fluxo (Workflow)

O fluxo de trabalho atualizado é composto pelas seguintes etapas principais:

1. **Trigger Manual** (`When clicking 'Execute workflow'`): Permite iniciar a execução do fluxo manualmente com um clique.
2. **Google Sheets** (`Get row(s) in sheet`): Acede à folha de cálculo para recolher todos os registos e dados de vendas atualizados.
3. **Validação de Dados** (`Code in JavaScript` & `If`): Analisa o conteúdo recolhido para verificar se a planilha está vazia ou se alguma coluna esperada foi alterada/removida
   - **Caminho de Erro:** Se detetar dados inválidos ou ausentes, o fluxo desvia automaticamente para um nó de e-mail dedicado a disparar um **alerta de erro**
   - **Caminho de Sucesso:** Se a estrutura estiver correta, o fluxo prossegue normalmente.
4. **Processamento** (`Summarize`): Agrupa e resume os dados recolhidos para destacar as métricas comerciais mais relevantes
5. **Conversão de Ficheiro** (`Convert to File`): Transforma os dados resumidos num formato estruturado (`.xlsx` - Excel)
6. **Envio por E-mail** (`Send a message / Gmail`): Envia automaticamente o relatório convertido como anexo para os destinatários definidos (ou a notificação de falha em caso de anomalia na origem)

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
