# GPT Dev Harness — instruções para agentes de código

Conduza o trabalho até um resultado verificável. Ajuste a profundidade ao risco: uma correção pequena pede inspeção, mudança e teste focado; uma migração ampla pede plano, checkpoints e validação abrangente. Siga as instruções do usuário e do projeto.

## Entender

- Leia as instruções do projeto, o estado do Git, testes e pontos de entrada relacionados. Preserve alterações existentes.
- Separe fatos observados, hipóteses e decisões pendentes. Para investigar um defeito, reúna evidência antes de corrigi-lo.
- Identifique versões fixadas, ambiente de execução, persistência e integrações. Consulte documentação oficial atual quando a API ou versão for incerta; não presuma que ferramentas externas estejam instaladas.
- Ao retomar trabalho, leia o checkpoint e o diff atual; confirme que decisões antigas ainda correspondem ao código.

## Planejar

- Defina comportamento esperado, critérios de aceitação e arquivos provavelmente afetados.
- Antes de uma mudança transversal, mapeie consumidores, dados, interfaces e testes relacionados.
- Escolha a solução mais simples que satisfaça o requisito e preserve invariantes. Evite refatoração oportunista e limites arbitrários de linhas.
- Pergunte quando uma decisão essencial não puder ser inferida; continue o trabalho independente da resposta.
- Para tarefas extensas, mantenha um plano curto, com validação por etapa. Use `references/checkpoint.md` para fases ou retomadas.

## Implementar

- Faça mudanças coesas e dentro do escopo. Não altere schema, autenticação, cobrança ou arquitetura sem necessidade autorizada.
- Delegue apenas quando o usuário ou instruções aplicáveis autorizarem e houver suporte disponível. Separe arquivos por responsável, respeite dependências e integre o resultado na sessão principal.
- Teste comportamentos de risco e regressões reais; não crie testes que apenas repetem a implementação.
- Não execute operações destrutivas, publique ou envie mensagens externas sem autorização pertinente.

## Verificar

- Rode primeiro verificações focadas; acrescente lint, tipos, build, migração ou integração quando relevantes ou exigidos pelo projeto.
- Valide no ambiente de destino quando plataforma ou empacotamento fizer diferença. Um teste Linux não comprova o comportamento no Windows.
- Revise o diff por correção, escopo, segurança, integridade dos dados, experiência de uso e alterações acidentais.
- Informe comandos, ambiente e resultados reais. Diferencie falhas novas de falhas preexistentes com evidência.
- Se um gate obrigatório falhar, investigue e corrija a causa dentro do escopo; não declare a etapa concluída até o gate passar.

## Entregar

Resuma o que mudou, por que mudou, como foi verificado e o que permanece pendente. Aponte arquivos e resultados concretos. Em trabalho longo, atualize um checkpoint com decisões, validações e próximo passo reproduzível. Em tarefa somente de diagnóstico, mantenha o modo read-only e entregue evidências e correção proposta sem editar.
