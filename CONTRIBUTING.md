# Como contribuir

1. Abra uma **issue** para propor experimentos, relatar problemas ou discutir mudanças relevantes.
2. Crie uma branch a partir de `main` (`feat/...`, `fix/...`, `docs/...` ou `experiment/...`).
3. Faça commits pequenos, com mensagens descritivas, e abra um **Pull Request** para `main`.
4. Solicite revisão de outro participante antes de integrar, registrando o que mudou e como foi testado.
5. Evite alterar silenciosamente um experimento já divulgado: preserve a versão anterior e documente correções e diferenças de metodologia.

## Organização

- `data/raw/`: dados originais pequenos, com fonte, licença e versão identificadas; nunca incluir dados pessoais identificáveis.
- `data/processed/`: bases processadas pequenas, acompanhadas do código que as gerou.
- `src/preprocessing/`: limpeza, transformação, codificação e escalonamento.
- `src/feature_selection/`: métodos de seleção de atributos.
- `src/models/`: arquiteturas e rotinas de treinamento.
- `src/evaluation/`: divisão de dados, validação cruzada e métricas.
- `experiments/`: execuções organizadas por método (`mlp-binary`, `mlp-multiclass`, `model-comparison`), com parâmetros, sementes e referências aos dados.
- `results/`: métricas, tabelas e figuras produzidas nos experimentos.
- `docs/`: documentação metodológica, decisões e notas de pesquisa.

**Atenção metodológica:** toda avaliação deve distinguir dados de treinamento e de validação/teste. Ajustes como seleção de atributos, imputação e normalização devem ocorrer exclusivamente nos dados de treinamento de cada partição, quando aplicável.

**Revisão por PR:** este documento estabelece o procedimento da equipe. Para impedir merges sem revisão, também é necessário configurar uma regra de proteção para a branch `main` nas configurações do GitHub.
