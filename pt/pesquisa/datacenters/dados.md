# Dados consultáveis e limites de reprodução

**Português** · [English](../../../en/research/datacenters/data.md)

**Versão 0.2 · Consulta: 2026-09-10**

[Comunidades](comunidades.md) · [Fontes](fontes.md) · [Método](metodo.md)

## 1. The Dalles: a série pública por trás da reportagem

Obtivemos o [CSV do gráfico OPB/Datawrapper][D35], atribuído à prefeitura. O arquivo contém 13 linhas anuais. Preservamos seu texto original, inclusive separadores, no campo `csv_original` deste [registro de origem](../../../dados/datacenters/the-dalles-opb.original.json), com SHA-256 e descrição nos dois idiomas.

**Fronteira:** uso de água do sistema municipal, em galões americanos por ano. São dados anuais agregados publicados, não leituras individuais de hidrômetros e não uma medição isolada de água evaporada. Mantemos a expressão “uso” do arquivo; não o combinamos com inventários corporativos de outra fronteira.

A coluna final do CSV não tem nome e contém uma fração. Conferimos que corresponde a uso do Google dividido pelo total municipal. A tabela abaixo apresenta essa fração em porcentagem, arredondada a duas casas.

| Ano | Total municipal (gal EUA) | Google (gal EUA) | Participação |
|---|---:|---:|---:|
| 2012 | 967752000 | 104337000 | 10,78% |
| 2013 | 965664000 | 108884000 | 11,28% |
| 2014 | 1012212000 | 132345000 | 13,07% |
| 2015 | 1045056000 | 148254930 | 14,19% |
| 2016 | 1073604000 | 113051140 | 10,53% |
| 2017 | 1102304000 | 124213000 | 11,27% |
| 2018 | 1093469000 | 150658660 | 13,78% |
| 2019 | 1003521000 | 233325170 | 23,25% |
| 2020 | 1128285660 | 279915070 | 24,81% |
| 2021 | 1232269290 | 355149730 | 28,82% |
| 2022 | 1187293000 | 352949820 | 29,73% |
| 2023 | 1238560470 | 383948170 | 31,00% |
| 2024 | 1335854130 | 434428540 | 32,52% |

**Cálculos reproduzidos:** participação = Google ÷ total × 100; crescimento de 2012 a 2024 = (434.428.540 ÷ 104.337.000 − 1) × 100 = **316,37%**. A participação vai de **10,78% para 32,52%**. A alta não demonstra, sozinha, desabastecimento causado pelo Google.

**Discrepância preservada:** a abertura da reportagem D33 informa 12% para 2012; o CSV resulta em 10,78%. Usamos os números do CSV e não escondemos a diferença. D34 apresenta correções da apuração, mas não resolve explicitamente essa divergência. [D33][D33] [D34][D34]

## 2. Memphis: números publicados por monitoramento comunitário

O relatório MCAP/CEEJH apresenta três sensores e o período 11/11/2025–11/03/2026. Transcrevemos os agregados da página 3 e recalculamos as porcentagens. [D30][D30]

| Local | Horas acima de 9 µg/m³ | Horas disponíveis | Parcela recalculada |
|---|---:|---:|---:|
| Boxtown Rd | 1241 | 2835 | 43,8% |
| Ford Rd / West Brooks Rd | 2121 | 2835 | 74,8% |
| Brentwood Dr | 949 | 2835 | 33,5% |

A série horária original, identificadores dos sensores e processamento completo não foram obtidos. Esta tabela reproduz agregados publicados, não dados brutos dos instrumentos. [D30][D30]

**Interpretação necessária:** 9 µg/m³ é o valor do padrão anual da EPA, cuja forma é a média anual calculada sobre três anos. Contar horas acima desse valor não demonstra violação desse padrão. O próprio relatório o usa como referência para horas; preservamos os números e corrigimos essa inferência na nossa análise. Isso não torna irrelevante a exposição registrada. [D31][D31]

Os dados não separam a contribuição do data center das demais fontes. Para essa pergunta, faltam a série original, controle de qualidade, meteorologia, histórico de funcionamento das fontes e método de atribuição. Não transformamos uma medição de vizinhança em inventário de emissões de uma empresa.

## 3. Documentos primários também são dados de investigação

- **Protocolo Anacé:** documento comunitário; páginas 9, 16 e 18–19 orientam a leitura do processo de consulta. [D25][D25]
- **Ata de The Dalles:** páginas 4–7 registram perguntas de moradores, financiamento dos estudos e manifestação sobre transparência. Não copiamos os contatos pessoais anexados. [D36][D36]
- **Relatos publicados:** vinculamos ao veículo, data e pessoa ou organização identificada; não alegamos ter feito entrevistas.

## 4. O que ainda falta

O acervo contém uma série tabular preservada e agregados de monitoramento; não contém um banco global de medições individuais. Para avançar, reunir dados por instalação e período, protocolos de reclamação, séries acústicas e hídricas e documentação de resposta. Ausência desses registros será tratada como lacuna de transparência, nunca como zero impacto.

Os arquivos de terceiros conservam sua autoria e condições de uso. O registro JSON preserva a tabela factual de origem; não altera o idioma do documento-fonte. A análise e o dicionário desta página têm versões completas em português e inglês.

[D25]: https://observatorio.direitosocioambiental.org/wp-content/uploads/2024/12/OFICIAL-PROTOCOLO-DE-CONSULTA-E-CONSENTIMENTO-PREVIO-LIVRE-E-INFORMADO-DO-POVO-ANACE-DA-TERRA-TRADICIONAL-copia.pdf
[D26]: https://www.intercept.com.br/2025/08/04/indigenas-anace-protestam-data-center-tiktok-ceara/
[D27]: https://idec.org.br/pdf/idec_estudo-nao-somos-quintal-de-data-centers.pdf
[D28]: https://apublica.org/2025/09/data-centers-se-escondem-por-tras-de-segredo-industrial-e-acordos-de-confidencialidade/
[D29]: https://www.mississippifreepress.org/xai-faces-fierce-opposition-over-southaven-mississippi-power-plant-permit/
[D30]: https://static1.squarespace.com/static/602aef80ede5cc16ae73697b/t/6a1064ba4158e3099fd14b53/1779459258033/South+Memphis+Follow+Up+Report_Apr26.pdf
[D31]: https://www.epa.gov/criteria-air-pollutants/naaqs-table
[D32]: https://x.ai/memphis/updates
[D33]: https://www.opb.org/article/2026/01/15/as-googles-water-demands-grow-the-dalles-aims-to-pull-more-from-mount-hood-forest/
[D34]: https://www.opb.org/article/2026/01/23/the-dalles-mayor-data-center-google/
[D35]: https://datawrapper.dwcdn.net/BMayV/2/dataset.csv
[D36]: https://ompnetwork.s3-us-west-2.amazonaws.com/sites/312/documents/cc_2021-11-08_council_minutes.pdf?jYfO_44rHBJuOFVzCoOJEEfTLBPitWPC=

<!-- editorial-record -->
---

**Modelo:** GPT-6 Astra (`gpt-6-astra`).

**Revisor:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
