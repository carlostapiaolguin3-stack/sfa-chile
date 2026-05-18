# México — CoDi y Ley Fintech

## Resumen ejecutivo

México publicó la Ley Fintech en 2018, una de las primeras de LATAM. La parte de Open Finance se atascó por falta de mandate operativo de la CNBV. CoDi (el equivalente PIX) fracasó por la misma razón: no obligó a bancos a integrarse con UX usable. El contraejemplo de lo que Chile NO debe hacer.

## Diferencias México vs Chile

| Aspecto | México | Chile |
|---|---|---|
| Ley | Ley Fintech 2018 | Ley 21.521 (Fintec) 2023 |
| Regulador | CNBV + Banxico | CMF |
| Sistema de pagos instantáneos | CoDi (Banxico, 2019) | Sin equivalente |
| Open Finance | Lento, sin manuales finales | NCG 514 + Anexo Técnico (pendiente) |
| Stack técnico | No definido formalmente | FAPI 2.0 |
| Sandbox | Sí, pero adopción baja | Voluntario abierto may-2026 |

## Cronología

| Hito | Fecha |
|---|---|
| Ley Fintech publicada | mar 2018 |
| ITF / Fondos Pagos Electrónicos | abr 2018 |
| CoDi lanzado | sept 2019 |
| Disposiciones Open Finance (Art. 76) | 2020 (vagas) |
| Manuales técnicos publicación | ATRASADOS, sin fecha final |
| CNBV publica APIs ATM como primera fase | 2020 (testimonial) |

## Por qué CoDi fracasó

1. **Sin mandate de adopción**: Banxico hizo CoDi pero NO obligó a los bancos a darle UX prominente en sus apps. Bancos lo escondieron
2. **Cap de USD 8.000 por transacción**: chico para B2B, irrelevante para PYME mediana
3. **Sin branding consumer fuerte**: la gente no sabe qué es CoDi vs SPEI vs transferencia
4. **Sin incentivo bancario**: bancos prefieren cobrar comisión por SPEI tradicional
5. **No es equity-free**: Banxico tampoco cobra, pero tampoco hay quien empuje
6. **PIX brasileño llegó después y arrasó**: comparativa pública mostró el fracaso

Resultado: 5 años después, CoDi tiene <2M transacciones/mes vs 6.300M/mes de PIX en Brasil.

## Por qué Open Finance México se atascó

1. **CNBV no es el operador del directorio**: lo delegó al sector privado, que nunca se coordinó
2. **Manuales técnicos no salieron**: las "disposiciones secundarias" quedaron vagas. Sin specs claras, nadie implementa
3. **Mandate ambiguo**: la Ley Fintech dice "podrán" no "deberán" para datos transaccionales
4. **Bancos top no quieren**: BBVA, Santander, Banorte no tienen incentivo. Si cumplen, pierden mindshare
5. **Sin push político continuo**: una vez publicada la Ley Fintech, el gobierno se olvidó

## Players relevantes México

### Bancos
BBVA México, Santander México, Banorte, Citibanamex, HSBC, Banco Azteca, Banco Inbursa

### Aggregators / Open Finance
- **Belvo**: HQ en CDMX, es el principal aggregator LATAM
- **Finerio Connect** (Nick Grassi): aggregator + PFM enterprise
- **Prometeo** (UY pero con México fuerte)

### Bancos digitales
- **Nubank México**, **Albo**, **Klar**, **Fondeadora**, **Cuenca**

### Players fintech ITF
- **Konfío**, **Bitso**, **Clip**, **Kueski**, **Stori**

### Referentes públicos
- Finerio Connect blog: enciclopedia divulgativa de facto
- No hay un "Bruno Diniz mexicano". Hueco abierto

## Recursos

- CNBV: cnbv.gob.mx (institucional, lento)
- Banxico CoDi: banxico.org.mx/sistemas-de-pago/codi.html
- Finerio Connect blog: blog.finerioconnect.com
- Asociación Fintech México (AFICO): fintechmexico.org

## Lo que Chile NO debe copiar

1. **No dejar manuales técnicos en limbo**: si Anexo Técnico N°3 se demora otro año, somos México
2. **No usar "podrán" en la Ley**: nuestro mandate dice "deberán" pero el cumplimiento en plazos es lo que importa
3. **No delegar el directorio al sector privado**: la CMF debe operarlo o pegarse mucho
4. **Si la CMF dice "sandbox voluntario", pegate al sandbox**: en MX nadie se preocupó del sandbox y eso fue señal del fracaso
5. **Sin branding consumer = adopción muerta**: lección directa

## Lo que sí podemos copiar de México

1. **Finerio Connect**: armaron blog técnico-divulgativo y se volvieron referencia. Modelo replicable en CL para tú
2. **Belvo en HQ CDMX pero LATAM**: si vas a hacer aggregator, no te limites a Chile desde día 1

## Lecciones para tú

- Hueco "Bruno Diniz / Finerio Connect" en CL está vacante
- Si la CMF replica el atascamiento mexicano (postergación 2027, después 2028, después 2029), tu repo gana relevancia cada año
- México demostró que "tener Ley" no es suficiente. Lo que importa es ejecución + educación + UX

## Fuentes

- CNBV reportes anuales
- Banxico CoDi stats
- Finerio Connect blog
- Konsentus "5 years of Open Banking in Mexico"
- AFICO reportes
- iupana cobertura MX continua
