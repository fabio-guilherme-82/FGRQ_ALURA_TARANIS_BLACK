# Challenge ONE G11 — Taranis Black

## Rota 4 — IA para Finanças e Operações

Projeto executivo desenvolvido por **Fabio Guilherme Ribeiro Queiroz** para a formação **G11 - BUSINESS AI BUILDER**.

## Objetivo

Analisar os gargalos no fluxo B2B de aprovação de pedidos, faturamento e expedição da Taranis Black e propor melhorias com apoio de inteligência artificial, mantendo supervisão humana nas decisões financeiras, fiscais e de crédito.

## Diagnóstico

A operação processa aproximadamente 180–220 pedidos corporativos por mês. O fluxo atual depende de e-mails, três planilhas locais e um ERP legado. Como consequência, o ciclo de pedidos supera cinco dias úteis, a análise de crédito pode levar até 48 horas e o fechamento contábil sofre atrasos e retrabalho.

Os principais pontos de atenção são:

- entrada de pedidos sem padrão;
- consultas manuais em sistemas desconectados;
- aprovação centralizada por e-mail;
- erros de cadastro e transposição de dados;
- ausência de indicadores de SLA por etapa;
- divergências entre orçamento, DRE e custos logísticos.

## Casos de uso de IA

1. **Extração e validação de pedidos:** OCR e IA assistiva para identificar campos incompletos, divergências de cadastro, produtos, preços e modalidade CIF/FOB.
2. **Conciliação financeira assistida:** comparação entre pedidos, planilhas, notas fiscais, boletos e ERP, com sinalização de anomalias.
3. **Alertas operacionais:** priorização de pedidos parados e identificação de risco de atraso, condicionada à existência de histórico confiável.

A IA recomenda e sinaliza. Crédito, pagamentos, lançamentos contábeis, alterações bancárias e decisões materiais continuam sob responsabilidade de pessoas autorizadas.

## Priorização

| Iniciativa | Esforço | Impacto | Ordem |
|---|---:|---:|---:|
| POP, checklist, fila/status e responsáveis | Baixo | Alto | 1 |
| Regras determinísticas e conciliação assistida | Médio | Alto | 2 |
| Integração gradual com o ERP | Alto | Alto | 3 |
| Modelos preditivos | Alto | A validar | 4 |

## SIPOC resumido

- **Fornecedores:** Comercial, cliente, Financeiro, Operações/Logística e sistemas/cadastros.
- **Entradas:** pedido, cadastro fiscal e de crédito, itens, preços e condição CIF/FOB.
- **Processo:** receber, conferir, aprovar, faturar, validar frete, liberar e expedir.
- **Saídas:** pedido aprovado, NF, frete, despacho e dados para fechamento.
- **Clientes:** cliente, Comercial, Financeiro, Logística e Controladoria.

## Ishikawa — causas-raiz

- **Método:** ausência de POP, dependência de e-mails, aprovação geral e validação tardia de frete.
- **Máquina:** ERP sem API, planilhas desconectadas e transposição manual.
- **Mão de obra:** consulta de crédito manual e espera por aprovação gerencial.
- **Material:** cadastros e tabelas divergentes.
- **Medição:** falta de SLA, baixa visibilidade e fechamento atrasado.
- **Meio ambiente:** crescimento da demanda e comunicação fragmentada entre áreas.

## Intervenção prioritária

Pilotar um fluxo padrão com checklist, fila/status único, responsáveis, alçadas e validações preventivas de cadastro, crédito e frete. A implantação deve começar sem substituir o ERP, medir a linha de base por etapa e só então decidir a escala da solução.

## Indicadores

- ciclo total: meta de até 24 horas úteis;
- aprovação de crédito: meta de até 4 horas;
- fechamento contábil: meta de até 2 dias;
- pedidos com status e responsável: mínimo de 95%;
- adoção do novo fluxo: mínimo de 90%;
- redução de retrabalho e erros de cobrança;
- custo de fretes emergenciais e reentregas.

ROI e economia não são apresentados como valores garantidos. Devem ser calculados após medir volume elegível, tempo poupado, custo-hora e custos efetivamente evitados.

## Governança e LGPD

Dados devem ser minimizados, mascarados quando possível e tratados somente em ferramentas aprovadas. É proibido enviar dados sensíveis para ferramentas públicas não homologadas ou aceitar decisões automatizadas sem validação. O processo deve manter fontes, logs, revisão humana, controle de acesso, monitoramento e resposta a incidentes.

## Entrega oficial

O relatório executivo completo e a entrega oficial estão disponíveis no Google Docs:

[Relatório Executivo — Taranis Black](https://docs.google.com/document/d/1DEB24nkC-loCnLlaA6d4EFXWLzncqkWvqAUkX2r9quY/edit?usp=sharing)

## Observação sobre dados

Este repositório não contém planilhas financeiras, dados pessoais ou documentos sigilosos. Os artefatos públicos devem ser anonimizados e revisados antes do compartilhamento.

## Status

- [x] Rota 0 — base estratégica
- [x] Rota 4 — SIPOC e Ishikawa
- [x] Política de IA responsável
- [x] README público do projeto
- [ ] Inserir evidências públicas adicionais, se necessário
