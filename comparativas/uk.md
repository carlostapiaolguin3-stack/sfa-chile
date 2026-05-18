# Reino Unido — Open Banking UK

## Resumen ejecutivo

UK fue el primero (2018). Stack FAPI 1.0 Advanced (Chile salta directo a FAPI 2.0). Adopción modesta: 12M usuarios activos en 8 años. PISPs y AISPs sí funcionaron. Lección: legal mandate alone no asegura adopción consumer.

## Diferencias UK vs Chile

| Aspecto | UK | Chile |
|---|---|---|
| Trigger | Competition and Markets Authority (CMA) | Ley 21.521 |
| Bancos obligados | CMA9 (9 bancos top retail) | Grupo 1 (todos) |
| Stack técnico | FAPI 1.0 Advanced | FAPI 2.0 |
| Operador del directorio | Open Banking Limited (OBL) | CMF directa |
| Roles | AISP (data) + PISP (pagos) + CBPII | PSBI + PSIP + IPI + IPCP |
| Maturity | Productivo desde ene 2018 | Vigencia jul 2027 |

## Cronología

| Hito | Fecha |
|---|---|
| CMA Banking Order | ago 2017 |
| Open Banking arranca | ene 2018 |
| Migración a v3.x | 2019-2020 |
| Variable Recurring Payments (VRP) | 2022 |
| 10M usuarios activos | mar 2024 |
| 12M usuarios activos | 2026 |

## Lo que funcionó

1. **CMA9 mandate fuerte**: los 9 bancos top obligados día 1, sin negociación
2. **OBL como entidad operadora**: separada del regulador, con presupuesto y mandate
3. **PISPs en pagos**: TrueLayer, Tink (vendida a Visa por USD 2B en 2022), GoCardless lideran
4. **AISPs en lending**: aggregators tipo Plaid (que llegó a UK) habilitaron credit scoring fintech
5. **Variable Recurring Payments**: VRP permite cobros recurrentes con consentimiento dinámico. El modelo más interesante a copiar

## Lo que NO funcionó

1. **Adopción consumer**: 12M de 50M bancarizados (24%) en 8 años. Esperaban más
2. **PFM no despegó**: Yolt (ING) cerró. Otros nunca pegaron mainstream
3. **Comerciantes lentos**: Variable Recurring Payments adopción tibia. Stripe domina sin necesidad de PISP
4. **Costo de cumplimiento**: 9 bancos top gastaron £200M+ acumulado en implementación
5. **OBL tuvo crisis de gobernanza**: Trustee Imran Gulamhuseinwala renunció en 2021 tras investigación interna

## Players UK relevantes

### Bancos (CMA9)
HSBC, Lloyds, Barclays, Santander UK, Nationwide, RBS, Bank of Scotland, Danske, AIB

### PISPs / AISPs
- **TrueLayer** (Francesco Simoneschi): líder en data + pagos
- **Tink** (vendida a Visa 2022 por USD 2B): líder histórico
- **Yapily** (Stefano Vaccino): API-only
- **Plaid UK**: llegó tarde pero pega fuerte
- **GoCardless**: Variable Recurring Payments para subscripciones
- **Token.io**: PISP enterprise

### Banking-as-a-Service que apalancan Open Banking
- **Modulr**, **Railsr (Railsbank)**, **ClearBank**

### Referentes públicos
- **Helen Child** (Open Banking Excellence, OBE): el modelo de "convener neutral". 34.000+ pioneros en su comunidad
- **Imran Gulamhuseinwala** (ex Trustee OBL): voz histórica
- **Sarah Cardell** (CMA actual): regulador
- **Daniel Kjellén** (Tink/Visa): vendor side

## Recursos para aprender

- Portal oficial: openbanking.org.uk
- Directory de estándares: github.com/OpenBankingUK
- Open Banking Excellence community: openbankingexcellence.org
- Helen Child / OBE Substack y eventos
- TrueLayer Docs: docs.truelayer.com

## Lo que Chile debería aprender

1. **Mandate sin educación = adopción mediocre**: UK no hizo campaña masiva. Chile debe evitarlo
2. **Branding consumer débil**: "Open Banking" no calza en marketing consumer. Chile necesita branding mejor
3. **Variable Recurring Payments es el feature killer**: aplicarlo desde día 1 para cobranza recurrente B2C
4. **Convener neutral es clave**: el rol de Helen Child / OBE es replicable. En Chile aún no lo ocupa nadie demand-side
5. **No esperes que PFM consumer despegue solo**: requiere o capital VC fuerte o partnership banco

## Lecciones para tú

- En UK el modelo "Helen Child / OBE" demostró que un convener neutral sin vendor ni regulador puede construir autoridad
- Newsletter + community + eventos presenciales funcionaron mejor que sites institucionales
- La parte de pagos (PISP) generó más valor económico que la lectura de datos
- 8 años después, sigue habiendo gaps que cubrir (PFM consumer, VRP para PYMES, scoring as a service)

## Fuentes

- openbanking.org.uk anuales reports
- Helen Child LinkedIn + OBE site
- TrueLayer y Tink whitepapers
- Konsentus "5 years of Open Banking UK" reports
- CMA Banking Order text
- PYMNTS UK Open Banking coverage
