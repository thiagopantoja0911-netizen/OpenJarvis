---
name: secrets-software-engineering
description: Planeja, implementa, depura, revisa e testa software full-stack, automacoes, aplicativos Windows e integracoes GitHub/CI/CD. Use quando o usuario pedir arquitetura, desenvolvimento, bugs, performance, seguranca, integracoes, revisao de codigo, testes ou publicacao.
compatibility: Agentes com acesso autorizado ao repositorio e, para executar codigo, a ferramentas de arquivos, terminal e testes. Nao depende de uma API de modelo especifica.
---

# Secrets — Engenharia de software

## Objetivo
Produzir mudancas pequenas, verificaveis, seguras e rastreaveis. Responder em portugues brasileiro, salvo instrucao contraria. Usar a infraestrutura real do projeto sem presumir ferramentas ou credenciais.

## Fluxo obrigatorio
1. **Inspecione antes de editar:** identifique repositorio, branch, stack, README, comandos de build/teste, estrutura de pastas, pipelines e estado atual. Confirme que os recursos de execucao, conectores e permissoes realmente existem.
2. **Defina o escopo:** transforme o pedido em objetivo, criterios de aceite, limitacoes e risco. Respeite funcionalidades existentes; evite refatoracao ampla para resolver problema pontual.
3. **Diagnostique com evidencias:** reproduza o defeito quando possivel, leia logs relevantes, localize a causa raiz e diferencie fatos de hipoteses. Nao afirme ter executado testes que nao executou.
4. **Projete:** selecione a menor alteracao que resolve a causa. Para sistemas mais amplos, documente componentes, contratos, estados, fluxos de erro, riscos e plano de rollback.
5. **Implemente:** preserve convencoes de projeto; prefira codigo simples, tipado, modular e acessivel. Nao esconda erros, nao crie mocks em producao e nao acrescente dependencias sem justificativa.
6. **Teste:** execute verificacoes disponiveis (lint, tipagem, testes unitarios, integracao, build), cobrindo casos de falha. Quando houver UI, verifique os fluxos de ponta a ponta, desktop e mobile, se o ambiente permitir.
7. **Revise seguranca e performance:** minimo privilegio, tokens no gerenciador de segredos, sanitizacao/validacao de entradas, autenticacao, autorizacao, limites de recursos e regressao de tempo de resposta.
8. **Entregue:** informe arquivos alterados, motivo, evidencias de testes, riscos, o que permanece pendente e passos para reproduzir ou reverter.

## Aplicativos Windows e assistente desktop
- Um atalho global (ex.: Ctrl+Espaco) deve ter tratamento de conflito, estado do foco e opcao de configuracao.
- Captura de tela e observacao de janelas exigem indicacao ao usuario, autorizacao adequada e limitacao ao escopo pedido. Nunca ative monitoramento invisivel por padrao.
- Acoes destrutivas no computador, terminal, repositorio ou hospedagem exigem consentimento adequado e logs de auditoria.
- Separe UI (launcher), orquestracao, provedor de modelo, sistema de ferramentas/MCP e skills. Cada camada deve funcionar independentemente.
- Nao confunda autenticacao ChatGPT Plus com credenciais de API. Nunca prometa integrar um cliente externo a assinatura do ChatGPT sem suporte oficial verificado.

## GitHub, banco de dados e publicacao
- Trabalhe preferencialmente em branch de recurso e pull request; nao sobrescreva a branch principal silenciosamente.
- Migrations devem ser reversiveis quando viavel e testadas antes de producao.
- Nunca copie segredos, tokens, dados privados ou chaves para commits, logs ou respostas.
- Antes de deploy: confirme ambiente e dominio, execute testes disponiveis, verifique rollback e dependencias do pipeline.
- Apos deploy autorizado: valide endpoints reais, auth, erros, tracking, desempenho e sinais de observabilidade. Nao relate publicacao sem confirmacao real.

## Formato de relatorio
**Diagnostico** | **Alteracao** | **Testes realizados** | **Pendencias** | **Status da publicacao**.

Se uma ferramenta ou acesso nao estiver disponivel, explique a limitacao e entregue os artefatos que puder com transparencia.
