# Exemplo fictício de checkpoint

Objetivo e escopo autorizado: corrigir ordenação de itens na tela de relatórios.
Ambiente e versões fixadas: Python 3.12; aplicação web de desenvolvimento.
Baseline (commit/checkpoint, testes): branch `fix/report-order`; teste de ordenação falhava antes da mudança.
Arquivos alterados e motivo: `reports/service.py` para ordenar pela data normalizada.
Decisões e invariantes preservadas: não alterar o formato dos dados persistidos.
Validação executada (comandos, resultado, plataforma): `pytest tests/reports/test_order.py` — passou; Linux.
Falhas abertas e evidência: nenhuma conhecida.
Próxima ação reproduzível: abrir a tela de relatórios e conferir datas iguais.
Itens fora do escopo: refatoração do módulo de relatórios.
