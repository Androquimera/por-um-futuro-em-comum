# Accessible data and limits of reproduction

[Português](DADOS.md) · **English**

**Version 0.2 · Accessed: 2026-09-10**

[Communities](COMUNIDADES.en.md) · [Sources](FONTES.en.md) · [Method](METODO.en.md)

## 1. The Dalles: the public series behind the reporting

We obtained the [OPB/Datawrapper chart CSV][D35], attributed to the city. It contains 13 annual rows. Its original text, including separators, is preserved in the `csv_original` field of this [source record](dados/the-dalles-opb.original.json), with SHA-256 and a description in both languages.

**Boundary:** municipal-system water use, in US gallons per year. These are published annual aggregates, not individual meter readings or an isolated measurement of evaporated water. We retain the file's term “use” and do not combine it with corporate inventories having different boundaries.

The CSV's final column is unnamed and contains a fraction. We checked that it equals Google's use divided by the municipal total. The table below expresses that fraction as a percentage rounded to two decimal places.

| Year | Municipal total (US gal) | Google (US gal) | Share |
|---|---:|---:|---:|
| 2012 | 967752000 | 104337000 | 10.78% |
| 2013 | 965664000 | 108884000 | 11.28% |
| 2014 | 1012212000 | 132345000 | 13.07% |
| 2015 | 1045056000 | 148254930 | 14.19% |
| 2016 | 1073604000 | 113051140 | 10.53% |
| 2017 | 1102304000 | 124213000 | 11.27% |
| 2018 | 1093469000 | 150658660 | 13.78% |
| 2019 | 1003521000 | 233325170 | 23.25% |
| 2020 | 1128285660 | 279915070 | 24.81% |
| 2021 | 1232269290 | 355149730 | 28.82% |
| 2022 | 1187293000 | 352949820 | 29.73% |
| 2023 | 1238560470 | 383948170 | 31.00% |
| 2024 | 1335854130 | 434428540 | 32.52% |

**Reproduced calculations:** share = Google ÷ total × 100; growth from 2012 to 2024 = (434,428,540 ÷ 104,337,000 − 1) × 100 = **316.37%**. The share rises from **10.78% to 32.52%**. The increase alone does not demonstrate shortages caused by Google.

**Discrepancy retained:** D33's opening reports 12% for 2012; the CSV yields 10.78%. We use the CSV figures and disclose the difference. D34 presents reporting corrections but does not explicitly resolve this discrepancy. [D33][D33] [D34][D34]

## 2. Memphis: figures published by community monitoring

The MCAP/CEEJH report describes three sensors and the period 2025-11-11–2026-03-11. We transcribed page 3 aggregates and recalculated the percentages. [D30][D30]

| Location | Hours above 9 µg/m³ | Available hours | Recalculated share |
|---|---:|---:|---:|
| Boxtown Rd | 1241 | 2835 | 43.8% |
| Ford Rd / West Brooks Rd | 2121 | 2835 | 74.8% |
| Brentwood Dr | 949 | 2835 | 33.5% |

The original hourly series, sensor identifiers, and full processing were not obtained. This table reproduces published aggregates, not raw instrument data. [D30][D30]

**Necessary interpretation:** 9 µg/m³ is the EPA annual standard's value, whose form is an annual mean averaged over three years. Counting hours above that value does not demonstrate violation of that standard. The report itself uses it as an hourly reference; we preserve the figures and correct that inference in our analysis. This does not make the recorded exposure irrelevant. [D31][D31]

These data do not separate the data center's contribution from other sources. That question requires the original series, quality control, meteorology, source operating histories, and an attribution method. We do not turn neighborhood measurements into one company's emissions inventory.

## 3. Primary documents are also investigative data

- **Anacé protocol:** community document; pages 9, 16, and 18–19 guide assessment of consultation. [D25][D25]
- **The Dalles minutes:** pages 4–7 record residents' questions, study funding, and a transparency submission. We do not copy attached personal contact details. [D36][D36]
- **Published accounts:** linked to the outlet, date, and identified person or organization; we do not claim to have conducted interviews.

## 4. What is still missing

The collection contains a preserved tabular series and monitoring aggregates; it is not a global database of individual measurements. Further work should obtain facility-specific data by period, complaint records, acoustic and water series, and documented responses. Missing records will be treated as a transparency gap, never as zero impact.

Third-party files retain their authorship and terms of use. The JSON record preserves the original factual table without changing the source document's language. This page's analysis and dictionary have complete Portuguese and English versions.

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

**Model:** GPT-6 Astra (`gpt-6-astra`).

**Reviewer:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
