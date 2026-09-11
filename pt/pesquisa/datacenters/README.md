# Data centers: funcionamento, impactos e responsabilidade

**Português** · [English](../../../en/research/datacenters/README.md)

**Estudo 0.2 · Corte da pesquisa: 2026-09-10 · Versão pública de trabalho**

[Casos regionais](casos.md) · [36 fontes](fontes.md) · [Método e ficha de avaliação](metodo.md) · [Responsabilidade editorial](../../creditos-editoriais.md) · [Pesquisa geral](../README.md)

## Conclusão principal

Data centers são infraestrutura física para serviços digitais. Seus efeitos dependem da escala, da utilização, do lugar e das decisões de construção e operação. **Não existe justificativa técnica para tratá-los como imateriais; também não existe base para atribuir o mesmo dano a toda instalação.**

A evidência reunida sustenta uma cobrança forte: demonstrar benefício, publicar impactos absolutos, avaliar efeitos cumulativos e proteger comunidades antes da expansão. Eficiência, contratos renováveis e investimento anunciado são informações relevantes, mas insuficientes para provar sustentabilidade. Essa conclusão é a avaliação do projeto a partir das fontes abaixo; não é uma certificação de qualquer operador.

## Comunidades e dados consultáveis

A versão 0.2 corrige um desequilíbrio institucional na seleção de fontes. [Comunidades](comunidades.md) incorpora documentos comunitários, ONGs, moradores e jornalismo local. [Dados consultáveis](dados.md) preserva a série pública de água e confere agregados do monitoramento comunitário. Declarações governamentais e empresariais são examinadas diante desses registros; não recebem prioridade automática.

## 1. O que há dentro de um data center

Servidores executam programas; armazenamento conserva dados; equipamentos de rede conectam máquinas e usuários. A instalação acrescenta alimentação elétrica, resfriamento, segurança e redundância. Data centers empresariais, colocation e grandes instalações de nuvem têm arranjos de propriedade e operação diferentes. Uma instalação pode servir várias empresas e aplicações. [D01][D01] [D23][D23]

A cadeia funcional, simplificada:

~~~mermaid
flowchart LR
  A["Rede elétrica / geração local"] --> B["Transformação, distribuição e UPS"]
  B --> C["Servidores, armazenamento e rede"]
  B --> D["Bombas, ventiladores e outros sistemas"]
  E["Combustível / baterias de reserva"] --> B
  C --> F["Calor"]
  F --> G["Transferência e rejeição de calor"]
  H["Água, conforme o projeto"] --> G
  G --> I["Atmosfera / água / recuperação útil"]
  J["Construção e fabricação"] --> C
  C --> K["Reuso, reparo e fim de vida"]
~~~

O diagrama é uma síntese do projeto, não uma planta universal. UPS mantém alimentação durante transições; geração de reserva atende contingências. Mais redundância e capacidade instalada não informam, sozinhas, consumo efetivo. [D01][D01]

IA é parte desse universo. Treinamento ajusta modelos; inferência os utiliza. Vídeo, raciocínio e tarefas longas têm perfis distintos de uma resposta textual curta. O relatório da IEA registra crescimento e variação de cargas; não autoriza atribuir todo consumo de data centers à IA nem usar um custo fixo por pergunta. [D03][D03]

## 2. Resfriamento: onde a água entra e onde o calor sai

Capturar calor no chip e rejeitá-lo para fora da instalação são etapas diferentes. **Um circuito interno fechado pode transferir calor a outro circuito que consome água em uma torre evaporativa.** É necessário seguir o calor até o destino final. [D02][D02]

| Arranjo | O que faz | O que precisa ser verificado |
|---|---|---|
| Ar e refrigeração mecânica | Ventiladores e trocadores removem calor; compressores podem participar. | Eletricidade, temperaturas externas e refrigerantes. |
| Torre evaporativa | Evaporação ajuda a rejeitar calor; há reposição e purga. | Captação, consumo, qualidade da água e efluente. |
| Resfriamento líquido direto | Fluido recebe calor junto aos componentes. | Como o circuito rejeita calor para o ambiente. |
| Sistema seco ou híbrido | Rejeição a ar, com possível apoio evaporativo. | Operação nas horas mais quentes, ruído e balanço água–energia. |
| Recuperação de calor | Entrega calor a um uso externo. | Demanda real, rede de distribuição e energia adicional. |

As alternativas não têm a mesma adequação em todos os climas. O guia da IEA mostra que o peso energético do resfriamento varia entre instalações; o FEMP descreve escolhas que podem economizar água à custa de mais eletricidade. Não aplicamos uma porcentagem universal. [D23][D23] [D02][D02]

## 3. Escala: o que é medido e o que é projetado

| Indicador | Valor | Natureza e fronteira |
|---|---|---|
| Eletricidade mundial dos data centers, 2025 | **485 TWh** | Estimativa IEA, todos os data centers no escopo. |
| Eletricidade mundial, 2030 | **950 TWh**, aproximadamente **3%** | Projeção IEA; não consumo já ocorrido. |
| Eletricidade nos EUA, 2030 | **649 TWh**, faixa **521–843 TWh** | Cenários Berkeley Lab, publicados em junho de 2026. |
| Água direta nos EUA, 2023 | Aproximadamente **66 bilhões de litros** | Estimativa Berkeley Lab, relatório de 2024. |
| Água indireta pela eletricidade nos EUA, 2023 | Aproximadamente **800 bilhões de litros** | Estimativa com matriz elétrica regional. |

Fontes: [D03][D03], [D04][D04], [D05][D05]. As projeções globais e nacionais usam métodos distintos. Não se somam; a distância entre elas exige atenção às hipóteses. Os números de água não são dados globais de IA e não descrevem cada bacia ou instalação.

**Potência não é energia.** MW descreve uma taxa; MWh descreve energia em um intervalo. Como exemplo aritmético, uma carga média constante de 100 MW durante 8.760 horas consumiria 876.000 MWh, ou 0,876 TWh. Uma conexão autorizada de 100 MW não demonstra que essa energia foi consumida. Exemplo ilustrativo, não estimativa de um empreendimento.

## 4. Métricas que ajudam — e o que elas escondem

PUE relaciona energia total da instalação à energia de TI. WUE relaciona o uso de água informado à energia de TI, com unidade e fronteira declaradas. São indicadores de eficiência; não resumem qualidade do serviço, impacto ecológico ou justiça distributiva. [D01][D01] [D18][D18]

Exemplo hipotético: TI de 100 unidades e PUE de 1,5 resultam em 150 unidades totais. Se a TI crescer para 200 e o PUE melhorar para 1,2, o total passa a 240: **60% a mais**, apesar da melhor eficiência. A conta não prova que toda melhoria cause expansão; mostra por que os totais precisam acompanhar os índices.

Para comparação honesta, nossa ficha exige:

- energia e água totais junto dos índices, no mesmo período;
- valores medidos separados de estimativas de projeto;
- ocupação, carga de TI e fronteira da instalação;
- captação separada de consumo e de água reutilizada;
- sazonalidade, origem da água e situação da bacia;
- benefício do serviço e alternativas consideradas.

Consumo hídrico diz respeito à água não devolvida à fonte considerada no período e nas condições da avaliação; captação inclui água que pode retornar. Volume recirculado internamente não deve ser confundido com nova retirada. Essa distinção é essencial para interpretar a modelagem de água direta e indireta. [D05][D05]

## 5. Emissões: contratos não encerram a investigação

A contabilidade de eletricidade por localização usa fatores da rede; a de mercado considera instrumentos contratuais elegíveis. É necessário declarar o método. Um contrato renovável pode financiar geração útil, mas seu balanço anual não prova fornecimento físico sem emissões em toda hora e local. [D06][D06]

A fronteira também importa: combustão e vazamentos próprios, eletricidade adquirida, construção, equipamentos e cadeia de fornecimento são questões diferentes. O Scope 3 inclui bens adquiridos, bens de capital e resíduos. Não somamos sem cuidado inventários corporativos de fornecedores e clientes, que podem contar a mesma emissão. [D24][D24]

Nossa avaliação propõe conferir adicionalidade, localização, perfil horário, conexão física e quem paga reforços da rede. “Renovável”, “carbono neutro” e “sem água para resfriamento” precisam vir acompanhados de definição e documentação. Benefícios climáticos de uma aplicação também precisam de comparação demonstrável com uma alternativa; não os descontamos automaticamente do impacto da infraestrutura.

## 6. Pessoas, território e distribuição de custos

A investigação deve abranger ruído contínuo e tonal, obras, poeira, tráfego, acesso à água, confiabilidade elétrica e decisões sobre o território. Relatos de moradores são evidência de experiência e de conflito; atribuir uma doença ou uma redução de pressão exige investigação específica.

A JLARC registrou benefícios concentrados na construção, problemas de ruído e contribuição regional relativamente pequena dos geradores de reserva aos poluentes examinados em 2024. Isso não exclui exposição local nem descreve uma operação diesel contínua. [D08][D08]

**Critério do projeto:** benefícios e custos precisam ter destinatários identificados. Empregos temporários, empregos permanentes, receita tributária, incentivos e despesas públicas devem aparecer separados. A soma de anúncios de investimento não prova benefício líquido para moradores.

Os [casos regionais](casos.md) mostram disputas reais e respostas diferentes. Nem um contrato privado nem uma licença eliminam a necessidade de medir resultados e avaliar efeitos cumulativos.

## 7. Equipamentos também têm uma vida material

O estudo de Wang e colaboradores projeta **1,2–5,0 milhões de toneladas acumuladas de lixo eletrônico ligado à IA generativa em 2020–2030**, conforme os cenários. Isso não é uma quantidade anual já observada nem o lixo de todos os data centers. A pesquisa evidencia a relevância da vida útil e das estratégias circulares. [D07][D07]

Nossa proposta é documentar fabricação, manutenção, reparabilidade, reutilização e destinação final. Substituir equipamentos por versões mais eficientes pode reduzir gasto operacional, mas exige comparar essa economia com os impactos da substituição. Não há prazo universal de troca que possa ser recomendado sem dados do equipamento e do uso.

## 8. O que já demonstrou melhoria e o que ainda é promessa

Um relatório técnico de 2018 do NREL, hoje hospedado no NLR, descreve economia de aproximadamente **7.950 m³ de água em dois anos**, cerca de metade do uso, com resfriamento híbrido em uma instalação específica. É um resultado de engenharia em operação; sua transferência para outro clima e outra carga precisa ser avaliada. [D22][D22]

Odense oferece um exemplo de recuperação útil de calor, descrito no estudo regional. Singapura oferece uma abordagem pública de expansão condicionada a padrões e planejamento. Nenhum dos casos comprova impacto zero.

As medidas que propomos priorizar são: localizar segundo capacidade e vulnerabilidade reais; reduzir computação desnecessária; operar resfriamento adequado ao clima; medir consumo absoluto; exigir transparência; garantir participação social; e atribuir custos ao empreendimento que os provoca. A ordem concreta depende do diagnóstico local.

## 9. Conclusão e limites

**A crítica mais forte é verificável:** quem utiliza quais recursos, onde, em que período, com qual benefício e quem assume o risco? Não presumimos inocuidade pela eficiência nem culpa por associação ao setor.

Este estudo reúne 36 fontes e dez casos regionais selecionados. Não é uma amostra representativa do planeta, auditoria de instalações ou revisão sistemática. Não medimos poluição, tarifas, ruído ou água em campo; não confirmamos desfechos administrativos posteriores aos documentos citados.

A próxima contribuição concreta pode aplicar a [ficha de avaliação](metodo.md) ao Pecém: reunir licenças, estudos e dados de operação disponíveis, conferir a resposta às recomendações e registrar lacunas. O estudo atual não declara que essa auditoria já foi realizada.

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

**Modelo:** GPT-6 Astra (`gpt-6-astra`).

**Revisor:** [andromedus. (@Androquimera)](https://github.com/Androquimera).
