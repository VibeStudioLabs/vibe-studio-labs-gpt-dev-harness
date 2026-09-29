---
name: gpt-dev-harness
description: Conduzir desenvolvimento de software com GPT/Codex, do entendimento à entrega, com mapa de impacto, implementação proporcional, testes, revisão, checkpoints e continuidade. Usar em features, correções, refatorações, investigação técnica ou retomada de projeto, especialmente quando o usuário pede um fluxo estruturado ou invoca GPT Dev Harness.
---

# GPT Dev Harness

Conduza o trabalho até um resultado verificável. Ajuste a profundidade ao risco e siga instruções do usuário e do projeto.

1. **Reconheça o estado:** leia instruções, diffs, testes, versões, ambiente e integrações relevantes. Preserve alterações preexistentes; baseie diagnósticos em evidências.
2. **Delimite a mudança:** descreva comportamento esperado, critérios de aceitação e impacto provável. Mapeie dados e consumidores em mudanças transversais. Escolha a solução mais simples suficiente.
3. **Planeje quando necessário:** tarefas pequenas seguem direto à implementação; tarefas extensas ganham etapas e checkpoints verificáveis. Pergunte apenas sobre decisões essenciais que não podem ser inferidas.
4. **Implemente com escopo:** faça alterações coesas; evite refatorações oportunistas. Delegue apenas se autorizado e disponível, com arquivos e dependências separados.
5. **Verifique:** execute primeiro testes focados e depois os gates pertinentes. Valide no ambiente alvo quando necessário. Revise o diff e reporte comandos e resultados reais.
6. **Feche o ciclo:** corrija gates obrigatórios que falharam antes de concluir a etapa. Entregue resumo, evidências, limitações e próximo passo reproduzível. Em diagnóstico read-only, não edite.

Leia `references/checkpoint.md` para handoffs e `references/quality-gates.md` para escolher verificações. A skill orienta o processo; não presume ferramentas externas nem substitui revisão humana.
