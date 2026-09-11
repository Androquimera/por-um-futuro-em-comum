# Estrutura do acervo

**Português** · [English](../en/structure.md)

Este documento fixa como o projeto nomeia e organiza seus arquivos. A regra existe por um motivo simples: um acervo bilíngue que cresce sem convenção fica ilegível em poucos meses, e quem chega depois não encontra nada. Quem for propor uma mudança de estrutura, altere este documento na mesma entrega.

## O desenho

```
por-um-futuro-em-comum/
├── README.md              porta bilíngue, curta, para quem chega
├── CONTRIBUTING.md        porta bilíngue para quem vai contribuir
├── LICENSE.md             licença, bilíngue
├── CITATION.cff           metadados de citação, lidos por máquina
├── AGENTS.md              instruções para agentes
├── CLAUDE.md              instruções para Claude
│
├── pt/                    todo o acervo em português brasileiro
│   ├── README.md          índice desta árvore
│   ├── manifesto.md
│   ├── pesquisa/
│   │   ├── README.md      índice da pesquisa
│   │   └── datacenters/
│   │       └── README.md  índice deste estudo
│   └── ...
│
├── en/                    todo o acervo em inglês, nomes em inglês
│   ├── README.md
│   ├── manifesto.md
│   └── research/
│       └── datacenters/
│
└── dados/                 dados brutos, sem idioma, citados pelas duas árvores
    └── datacenters/
```

**Uma árvore por idioma, completa e independente.** O leitor entra pela raiz do seu idioma e nunca precisa sair dela, exceto para chegar a um dado bruto. Acrescentar espanhol amanhã é criar `es/` espelhando a estrutura, sem tocar em mais nada.

## Regras de nome de arquivo

**1. Minúsculas, sem acento, sem espaço, hífen entre palavras.**

```
certo:   comunidades-atingidas.md
errado:  Comunidades Atingidas.md, COMUNIDADES.md, comunidades_atingidas.md
```

**2. Sem cedilha, til ou acento no nome do arquivo.** Não é preciosismo:

- Na URL, `ações.md` vira `a%C3%A7%C3%B5es.md`, que ninguém consegue ler ou ditar.
- O Unicode tem duas formas de escrever "ç". Windows, macOS e Linux não concordam sobre qual usar, e o mesmo arquivo pode aparecer duas vezes no histórico, ou sumir na máquina de um colaborador.
- Parte das ferramentas de publicação simplesmente falha.

**O acento vive no título dentro do arquivo.** O nome do arquivo é endereço; o título é o que o leitor lê:

```
arquivo:  pt/pesquisa/acoes.md
primeira linha:  # Caminhos de ação
```

**3. O nome é traduzido junto com o texto.** Um arquivo na árvore inglesa tem nome em inglês, incluindo as pastas. `pt/pesquisa/acoes.md` corresponde a `en/research/actions.md`. Um leitor de inglês nunca deve encontrar uma palavra em português no endereço, nem o contrário: o projeto é bilíngue em todas as instâncias, e o endereço é a primeira coisa que a pessoa lê.

**4. Exceção: nomes que a máquina reconhece não se traduzem.**

| Nome | Quem lê | O que quebra se traduzir |
|---|---|---|
| `README.md` | GitHub, geradores de site | A pasta deixa de ter índice visível |
| `LICENSE.md` | GitHub, ferramentas de licença | O projeto deixa de declarar licença |
| `CONTRIBUTING.md` | GitHub | Some o aviso a quem abre issue ou pull request |
| `CITATION.cff` | GitHub, Zenodo, gerenciadores de referência | Some o botão de citação |
| `AGENTS.md`, `CLAUDE.md` | agentes de IA | O agente não encontra as instruções |

Esses são nomes técnicos, como uma extensão de arquivo. Traduzi-los não deixa o projeto mais bilíngue: só desliga a função. O conteúdo deles, esse sim, é bilíngue.

**5. `README.md` é o índice de toda pasta.** Toda pasta de conteúdo tem um, nos dois idiomas, apresentando o que há ali e por quê. É o arquivo que o GitHub mostra automaticamente ao abrir a pasta.

**6. Nada de arquivo de conteúdo solto na raiz.** A raiz guarda apenas as portas e os nomes técnicos da tabela acima.

## Regras de documento

**Cabeçalho.** Logo abaixo do título, a linha de idioma, com o idioma atual em negrito e o par como link:

```markdown
# Caminhos de ação

**Português** · [English](../../en/research/actions.md)
```

**Links internos sempre relativos** (`../../en/research/actions.md`), nunca começando com `/`. Links relativos funcionam ao navegar pelo GitHub e são convertidos automaticamente no site do projeto. Links absolutos quebram nos dois.

**Rodapé.** Todo documento termina com o registro editorial, na forma definida em [créditos editoriais](creditos-editoriais.md):

```markdown
<!-- editorial-record -->
---

**Modelo:** nome do modelo (`identificador`).

**Revisor:** nome público do revisor.
```

**Datas por extenso numérico, do ano para o dia:** `2026-09-10`. Não use `10/09/2026`, que um leitor de inglês lê como 9 de outubro.

## Como crescer sem se perder

**Um tema novo de pesquisa** é uma pasta nova dentro de `pesquisa/` e `research/`, com `README.md` em cada uma, e o par completo de documentos. Nunca publique um lado só: o par incompleto é o começo de toda bagunça bilíngue.

**Um documento novo** entra na pasta do seu tema, é citado no `README.md` daquela pasta, e nasce com os dois idiomas.

**Um idioma novo** é uma raiz nova (`es/`, `fr/`) espelhando a estrutura, com todos os nomes traduzidos. Acrescente a porta correspondente no `README.md` da raiz.

**Um dado bruto** vai para `dados/`, na subpasta do tema que o cita, com nome descritivo. Use o sufixo `.original` quando o arquivo for cópia fiel do que a fonte publicou, sem nenhum tratamento: `the-dalles-opb.original.json`. Dado não tem idioma e não é duplicado; as duas árvores citam o mesmo arquivo, e é por isso que ele mora fora delas.

**Quando uma pasta passar de uns quinze documentos**, ela virou duas. Divida por tema antes que a lista fique impossível de ler, e atualize o `README.md`.

<!-- editorial-record -->
---

**Modelo:** Claude Opus 5 (`claude-opus-5`).

**Revisor:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
