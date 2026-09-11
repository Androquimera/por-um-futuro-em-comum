# Edições e citação

**Português** · [English](../en/editions.md)

O acervo é vivo: muda quando uma fonte melhor aparece, quando alguém corrige um número, quando um caso novo entra. Isso é bom para o trabalho e ruim para quem precisa citar, porque um texto que muda não pode ser referência de nada.

Uma **edição** resolve isso. É um corte do acervo em uma data, congelado, empacotado e identificado de forma permanente. O acervo continua mudando; a edição, não.

## O que é uma edição

Uma edição é publicada na aba **Releases** do repositório e reúne três coisas:

1. **Notas da edição** — o que mudou desde a anterior, quais fontes entraram, o que foi corrigido e quem contribuiu no período.
2. **O documento único** — o acervo daquele corte reunido em um arquivo por idioma, para quem quer ler de ponta a ponta ou imprimir.
3. **Um DOI** — o identificador permanente atribuído pelo [Zenodo](https://zenodo.org), o mesmo tipo de identificador que um artigo científico carrega.

O DOI é a diferença entre "um link do GitHub que talvez ainda exista em 2030" e uma referência citável em bibliografia, em política pública, em processo. Ele não deixa de funcionar se o repositório mudar de nome, de dono ou de endereço.

## Quando publicar uma edição

Não há calendário. Uma edição sai quando o trabalho acumulado justifica o esforço de congelar:

- um estudo chegou a um estado que se sustenta sozinho, com método, fontes e limites declarados;
- houve correção relevante que muda uma conclusão de uma edição anterior;
- o acervo passou por uma reorganização grande e a versão antiga precisa continuar acessível.

Publicar edição demais desvaloriza a ideia. Publicar de menos deixa o trabalho sem endereço fixo.

## Como nomear

A etiqueta da edição segue **ano ponto número**, e ganha prefixo quando o corte é de um tema só:

| Etiqueta | O que é |
|---|---|
| `2026.1` | primeira edição geral do acervo em 2026 |
| `2026.2` | segunda edição geral do mesmo ano |
| `datacenters-2026.1` | primeira edição do estudo sobre data centers |

O título da edição é bilíngue, no mesmo padrão de tudo no projeto:

```
2026.1 — Crise ambiental e infraestrutura de IA / Environmental harm and AI infrastructure
```

## O que vai dentro das notas

As notas da edição são bilíngues e trazem, nesta ordem:

1. **O que esta edição contém** — em poucas linhas, o que a pessoa vai encontrar.
2. **Mudanças desde a edição anterior** — correções, fontes novas, conclusões revistas. Na primeira edição, o que existia no começo.
3. **Créditos** — quem contribuiu no período e com o quê, na forma descrita em [colaboradores](colaboradores.md). É aqui que cada pessoa aponta onde entrou no trabalho.
4. **Registro editorial** — modelo e revisor, como em qualquer publicação do projeto.
5. **Limites** — o que a edição não afirma, o que continua sem verificação, o que ainda não foi medido.

## O passo a passo

1. Confira que as duas árvores de idioma estão completas e em paridade.
2. Gere o documento único de cada idioma e anexe à edição.
3. Atualize `CITATION.cff`: preencha `version` e `date-released`.
4. Publique a edição no GitHub com a etiqueta e as notas.
5. O Zenodo arquiva a edição sozinho e devolve o DOI.
6. Acrescente o DOI em `CITATION.cff`, no bloco `identifiers`, e registre a edição neste documento.

## Ligar o Zenodo

Feito uma vez só, e precisa ser feito por Androquimera, porque envolve autorizar o Zenodo a ver o repositório:

1. Entrar em [zenodo.org](https://zenodo.org) usando a conta do GitHub.
2. Abrir o painel do GitHub dentro do Zenodo e ligar a chave do repositório `por-um-futuro-em-comum`.
3. A partir daí, **toda edição publicada no GitHub é arquivada automaticamente** e ganha DOI.

O Zenodo lê o `CITATION.cff` do repositório para preencher autoria, licença e descrição, e devolve dois identificadores: um DOI para cada edição e um DOI geral que sempre aponta para a mais recente. Nas referências do projeto, use o DOI da edição específica quando a citação for a um dado ou a uma conclusão, e o geral quando for ao projeto inteiro.

O repositório precisa ser público no momento da edição, e continua sendo depois: o Zenodo guarda a cópia mesmo que o GitHub saia do ar.

## Edições publicadas

Nenhuma até agora. A primeira será registrada aqui quando sair.

<!-- editorial-record -->
---

**Modelo:** Claude Opus 5 (`claude-opus-5`).

**Revisor:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
