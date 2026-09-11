# Dados brutos · Raw data

**🇧🇷** Esta pasta guarda os dados brutos citados pelo acervo. Dado não tem idioma, por isso mora fora das árvores `pt/` e `en/`: as duas citam o mesmo arquivo, e assim nenhuma versão pode divergir da outra.

**🇬🇧** This folder holds the raw data cited by the collection. Data has no language, so it lives outside the `pt/` and `en/` trees: both cite the same file, and no version can drift from the other.

---

## Como os arquivos são nomeados · How files are named

O nome descreve o caso e a fonte, em minúsculas e com hífen. O sufixo **`.original`** marca cópia fiel do que a fonte publicou, sem nenhum tratamento nosso — é o que permite a qualquer pessoa refazer a conferência do zero.

The name describes the case and the source, lowercase and hyphenated. The **`.original`** suffix marks a faithful copy of what the source published, with no processing on our side — this is what lets anyone redo the verification from scratch.

```
the-dalles-opb.original.json
└── caso ──┘ └ fonte ┘ └ cópia fiel ┘
```

Um arquivo derivado, tratado ou recortado por nós, perde o sufixo e ganha, ao lado, a explicação de como foi produzido.
A file we derived, processed, or trimmed loses the suffix and gains, beside it, an explanation of how it was produced.

## Onde estão descritos · Where they are described

Cada dado é explicado, com método e limites, no documento que o cita:
Each dataset is explained, with method and limits, in the document that cites it:

| Pasta · Folder | Descrição · Described in |
|---|---|
| `datacenters/` | [pt/pesquisa/datacenters/dados.md](../pt/pesquisa/datacenters/dados.md) · [en/research/datacenters/data.md](../en/research/datacenters/data.md) |

As regras completas estão em [estrutura do acervo](../pt/estrutura.md) · [collection structure](../en/structure.md).
