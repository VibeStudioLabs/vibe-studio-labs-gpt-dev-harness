# Vibe Studio Labs GPT Dev Harness

**Um fluxo prático para desenvolver software com GPT e Codex: entender, planejar, implementar e verificar, com contexto suficiente para continuar depois.**

Em vez de despejar um prompt enorme e torcer pelo resultado, o harness orienta o agente a inspecionar o projeto, mapear o impacto, fazer mudanças proporcionais e apresentar evidências de validação. Funciona como instruções de trabalho; não instala ferramentas nem presume acesso a agentes paralelos.

## O que inclui

- `AGENTS.md`: instruções reutilizáveis para agentes de código em um projeto.
- `SKILL.md`: versão no formato de skill para ambientes que oferecem skills.
- `references/checkpoint.md`: modelo de retomada entre fases e sessões.
- `references/quality-gates.md`: verificações proporcionais ao risco da mudança.
- `examples/`: exemplo genérico de checkpoint preenchido.

## Começar

1. Leia `AGENTS.md` e adapte os comandos de verificação ao seu projeto.
2. Coloque as instruções no local que seu agente lê: por exemplo, `AGENTS.md` na raiz do projeto, ou as instruções do projeto/skill no seu ambiente.
3. Peça ao agente para investigar o projeto antes de editar. Para tarefas pequenas, o fluxo deve continuar leve; para migrações e mudanças transversais, registre plano e checkpoints.

Exemplo de pedido:

> Use o GPT Dev Harness neste projeto. Primeiro entenda o estado atual e os critérios de aceitação; depois implemente a menor mudança adequada, rode os testes relevantes e me diga exatamente o que foi validado.

## Princípios

- O código, configuração, logs e instruções atuais do projeto são a fonte de verdade.
- Dimensione o planejamento e os testes pelo risco.
- Preserve alterações locais e invariantes existentes.
- Valide no ambiente de destino quando sistema operacional, empacotamento ou integração fizer diferença.
- Um gate obrigatório com falha bloqueia a conclusão daquela etapa; reporte evidências, não suposições.
- Delegação, publicação e comandos destrutivos dependem de autorização e capacidade disponível.
- Não imponha stack, ferramentas, limites de linhas ou subagentes sem necessidade.

## Limites

O harness orienta o processo; não substitui revisão humana, testes, documentação oficial ou julgamento de produto. O agente precisa ter acesso ao código e às ferramentas de validação para executar essas etapas. Uma skill incluída aqui não se instala automaticamente no ChatGPT ou Codex: siga o fluxo de instalação do ambiente que você usa.

## Origem

O Vibe Studio Labs GPT Dev Harness é uma adaptação original para GPT/Codex, inspirada em práticas descritas no [Vibe Coding Toolkit](https://github.com/soumatheusgomes/vibe-coding-toolkit), licenciado sob MIT. Não é afiliado aos autores do projeto de referência. Veja `LICENSE` para a licença deste repositório.

## Contribuir

Veja [CONTRIBUTING.md](CONTRIBUTING.md). Ideias, exemplos de uso e melhorias são bem-vindos; mantenha instruções independentes de ferramentas opcionais e evite adicionar processo que não resolva um problema real.
