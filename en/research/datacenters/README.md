# Data centers: operation, impacts, and responsibility

[Português](../../../pt/pesquisa/datacenters/README.md) · **English**

**Study 0.2 · Research cutoff: 2026-09-10 · Public working version**

[Regional cases](cases.md) · [36 sources](sources.md) · [Method and assessment form](method.md) · [Editorial responsibility](../../editorial-credits.md) · [General research](../README.md)

## Main conclusion

Data centers are physical infrastructure for digital services. Their effects depend on scale, utilization, location, and construction and operating decisions. **There is no technical justification for treating them as immaterial; nor is there evidence for attributing the same harm to every facility.**

The evidence gathered supports demanding demonstrated benefits, disclosure of absolute impacts, assessment of cumulative effects, and protection of communities before expansion. Efficiency, renewable contracts, and announced investment are relevant but insufficient to prove sustainability. This conclusion is the project's assessment of the sources below, not certification of any operator.

## Communities and accessible data

Version 0.2 corrects an institutional imbalance in source selection. [Communities](communities.md) incorporates community-authored documents, NGOs, residents, and local reporting. [Accessible data](data.md) preserves the public water series and checks community monitoring aggregates. Government and company statements are assessed against these records; they do not receive automatic priority.

## 1. What is inside a data center

Servers run programs; storage preserves data; networking equipment connects machines and users. The facility adds electricity supply, cooling, security, and redundancy. Enterprise data centers, colocation, and large cloud facilities have different ownership and operating arrangements. One facility may serve several companies and applications. [D01][D01] [D23][D23]

A simplified functional chain:

~~~mermaid
flowchart LR
  A["Electricity grid / on-site generation"] --> B["Transformation, distribution, and UPS"]
  B --> C["Servers, storage, and networking"]
  B --> D["Pumps, fans, and other systems"]
  E["Backup fuel / batteries"] --> B
  C --> F["Heat"]
  F --> G["Heat transfer and rejection"]
  H["Water, depending on design"] --> G
  G --> I["Atmosphere / water / useful recovery"]
  J["Construction and manufacturing"] --> C
  C --> K["Reuse, repair, and end of life"]
~~~

The diagram is the project's synthesis, not a universal blueprint. UPS maintains power through transitions; backup generation serves contingencies. More redundancy and installed capacity do not, by themselves, establish actual consumption. [D01][D01]

AI is part of this universe. Training adjusts models; inference uses them. Video, reasoning, and long tasks have different profiles from a short text response. The IEA report records growing and variable loads; it does not justify attributing all data center consumption to AI or using a fixed cost per question. [D03][D03]

## 2. Cooling: where water enters and heat leaves

Capturing heat at the chip and rejecting it outside the facility are different stages. **A closed internal circuit can transfer heat to another circuit that consumes water in an evaporative tower.** We need to follow the heat to its final destination. [D02][D02]

| Arrangement | What it does | What needs checking |
|---|---|---|
| Air and mechanical refrigeration | Fans and heat exchangers remove heat; compressors may be involved. | Electricity, outdoor temperatures, and refrigerants. |
| Evaporative tower | Evaporation helps reject heat; makeup water and blowdown are involved. | Withdrawals, consumption, water quality, and effluent. |
| Direct liquid cooling | Fluid receives heat close to components. | How the circuit rejects heat to the environment. |
| Dry or hybrid system | Air-based rejection, potentially assisted by evaporation. | Operation during the hottest hours, noise, and the water–energy balance. |
| Heat recovery | Delivers heat to an external use. | Actual demand, distribution network, and additional energy. |

These alternatives are not equally suitable in every climate. The IEA guide shows that cooling's energy share varies between facilities; FEMP describes choices that can save water at the cost of more electricity. We do not apply a universal percentage. [D23][D23] [D02][D02]

## 3. Scale: what is measured and what is projected

| Indicator | Value | Nature and boundary |
|---|---|---|
| Global data center electricity, 2025 | **485 TWh** | IEA estimate, all data centers within scope. |
| Global electricity, 2030 | **950 TWh**, approximately **3%** | IEA projection; not consumption that has already occurred. |
| US electricity, 2030 | **649 TWh**, range **521–843 TWh** | Berkeley Lab scenarios, published in June 2026. |
| Direct US water, 2023 | Approximately **66 billion liters** | Berkeley Lab estimate, 2024 report. |
| Indirect US water through electricity, 2023 | Approximately **800 billion liters** | Estimate using regional electricity mixes. |

Sources: [D03][D03], [D04][D04], [D05][D05]. Global and national projections use different methods. They cannot be added; the difference between them requires attention to assumptions. The water figures are not global AI data and do not describe each basin or facility.

**Power is not energy.** MW describes a rate; MWh describes energy over an interval. As an arithmetic example, a constant average load of 100 MW over 8,760 hours would consume 876,000 MWh, or 0.876 TWh. An authorized 100 MW connection does not demonstrate that this energy was consumed. This is an illustration, not an estimate for a development.

## 4. Useful metrics — and what they hide

PUE relates total facility energy to IT energy. WUE relates reported water use to IT energy, with the unit and boundary declared. These are efficiency indicators; they do not summarize service quality, ecological impact, or distributive justice. [D01][D01] [D18][D18]

Hypothetical example: IT using 100 units at a PUE of 1.5 produces 150 total units. If IT grows to 200 and PUE improves to 1.2, the total becomes 240: **60% more**, despite better efficiency. This calculation does not prove that every improvement causes expansion; it shows why totals must accompany ratios.

For an honest comparison, our assessment form requires:

- total energy and water alongside ratios, for the same period;
- measured values separated from design estimates;
- occupancy, IT load, and the facility boundary;
- withdrawals separated from consumption and reused water;
- seasonality, water source, and basin conditions;
- service benefits and alternatives considered.

Water consumption concerns water not returned to the source considered within the assessment's period and conditions; withdrawals include water that may return. Internally recirculated volume must not be confused with new withdrawals. This distinction is essential for interpreting direct and indirect water modeling. [D05][D05]

## 5. Emissions: contracts do not close the investigation

Location-based electricity accounting uses grid factors; market-based accounting considers eligible contractual instruments. The method must be declared. A renewable contract may finance useful generation, but its annual balance does not prove physically emissions-free supply at every hour and location. [D06][D06]

Boundaries also matter: on-site combustion and leaks, purchased electricity, construction, equipment, and the supply chain are different issues. Scope 3 includes purchased goods, capital goods, and waste. We do not indiscriminately add suppliers' and customers' corporate inventories, which may count the same emission. [D24][D24]

Our assessment proposes checking additionality, location, hourly profiles, physical connection, and who pays for grid reinforcement. “Renewable,” “carbon neutral,” and “no water for cooling” need definitions and documentation. An application's climate benefits also need a demonstrated comparison with an alternative; we do not automatically deduct them from infrastructure impacts.

## 6. People, territory, and the distribution of costs

Investigation must cover continuous and tonal noise, construction, dust, traffic, access to water, electricity reliability, and land-use decisions. Residents' accounts are evidence of experience and conflict; attributing an illness or reduced water pressure requires a specific investigation.

JLARC recorded benefits concentrated in construction, noise problems, and backup generators' relatively small regional contribution to the pollutants examined in 2024. This neither excludes local exposure nor describes continuous diesel operation. [D08][D08]

**The project's criterion:** the recipients of benefits and costs must be identified. Temporary jobs, permanent jobs, tax revenue, incentives, and public expenditure should appear separately. Adding investment announcements does not prove a net benefit to residents.

The [regional cases](cases.md) show real disputes and different responses. Neither a private contract nor a permit removes the need to measure outcomes and assess cumulative effects.

## 7. Equipment also has a material life

Wang and colleagues' study projects **1.2–5.0 million tonnes of cumulative electronic waste associated with generative AI over 2020–2030**, depending on the scenario. This is neither an annual quantity already observed nor waste from all data centers. The research highlights the relevance of equipment lifetimes and circular strategies. [D07][D07]

Our proposal is to document manufacturing, maintenance, repairability, reuse, and final disposal. Replacing equipment with more efficient versions may reduce operating expenditure, but requires comparing those savings with replacement impacts. No universal replacement interval can be recommended without equipment and usage data.

## 8. What has demonstrated improvement and what remains a promise

A 2018 NREL technical report, now hosted by NLR, describes savings of approximately **7,950 m³ of water over two years**, about half of water use, through hybrid cooling at a specific facility. This is an operational engineering result; transfer to another climate and load needs assessment. [D22][D22]

Odense offers an example of useful heat recovery, described in the regional study. Singapore offers a public approach to expansion conditioned on standards and planning. Neither case proves zero impact.

The measures we propose prioritizing are: choosing locations based on actual capacity and vulnerability; reducing unnecessary computation; operating climate-appropriate cooling; measuring absolute consumption; requiring transparency; ensuring public participation; and assigning costs to the development that causes them. The actual order depends on local assessment.

## 9. Conclusion and limitations

**The strongest criticism is verifiable:** who uses which resources, where, during what period, with what benefit, and who bears the risk? We presume neither harmlessness from efficiency nor guilt by association with the sector.

This study brings together 36 sources and seven selected regional cases. It is not a representative global sample, a facility audit, or a systematic review. We did not measure pollution, tariffs, noise, or water in the field; we did not confirm administrative outcomes subsequent to the cited documents.

The next concrete contribution could apply the [assessment form](method.md) to Pecém: collect available permits, studies, and operating data, check responses to the recommendations, and record gaps. The current study does not claim that this audit has already been performed.

[D01]: https://www.energy.gov/sites/default/files/2024-07/best-practice-guide-data-center-design_0.pdf
[D02]: https://www.energy.gov/cmei/femp/cooling-water-efficiency-opportunities-federal-data-centers
[D03]: https://www.iea.org/reports/key-questions-on-energy-and-ai/executive-summary
[D04]: https://seta.lbl.gov/publications/united-states-data-center-energy-2025
[D05]: https://eta-publications.lbl.gov/sites/default/files/2024-12/us_data_center_energy_usage_report_lbnl-2001637_0.pdf
[D06]: https://ghgprotocol.org/sites/default/files/2023-03/Scope%202%20Guidance.pdf
[D07]: https://www.nature.com/articles/s43588-024-00712-6
[D08]: https://jlarc.virginia.gov/landing-2024-data-centers-in-virginia.asp
[D09]: https://www.eia.gov/todayinenergy/detail.php?id=67664
[D10]: https://www.cso.ie/en/releasesandpublications/ep/p-dcmec/datacentresmeteredelectricityconsumption2025/
[D11]: https://www.abc.net.au/news/2026-06-15/ai-data-centre-energy-impact-ireland-cautionary-tale/106758928
[D12]: https://tribunalambiental.cl/sentencia-r27-270-2020-cerrillos-data-center/
[D13]: https://www.t13.cl/noticia/negocios/google-reformulara-desde-cero-plan-data-center-cerrillos-17-9-2024
[D14]: https://www.mpf.mp.br/o-mpf/unidades/pr-ce/noticias/mpf-e-dpu-pedem-adequacoes-em-licenciamento-ambiental-de-data-center-no-ceara-antes-do-inicio-da-operacao
[D15]: https://www.investing.com/news/stock-market-news/brazils-omnia-casa-dos-ventos-sign-2-billion-energy-deal-for-tiktok-data-center-4696380
[D16]: https://www.opovo.com.br/noticias/economia/2026/05/20/amp/mpf-e-dpu-pedem-adequacoes-em-licenciamento-ambiental-do-data-center-pecem.html
[D17]: https://mediaselangor.com/en/2026/07/386144
[D18]: https://www.mida.gov.my/wp-content/uploads/2024/12/Guideline-for-Sustainable-Development-of-Data-Centre.pdf
[D19]: https://www.imda.gov.sg/-/media/imda/files/how-we-can-help/green-dc-roadmap/green-dc-roadmap.pdf
[D20]: https://www.mddi.gov.sg/newsroom/mddi-response-to-pq-on-future-data-centre-capacity-plans-in-support-of-ai-adoption/
[D21]: https://www.fjernvarmefyn.dk/nyheder/glaedens-dag-for-fjernvarme-fyns-kunder-udskaeldt-prisloft-forsvinder-helt/
[D22]: https://research-hub.nlr.gov/en/publications/thermosyphon-cooler-hybrid-system-for-water-savings-in-an-energy-/
[D23]: https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai
[D24]: https://ghgprotocol.org/sites/default/files/standards/Corporate-Value-Chain-Accounting-Reporing-Standard_041613_2.pdf?pdf=download

<!-- editorial-record -->
---

**Model:** GPT-6 Astra (`gpt-6-astra`).

**Reviewer:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
