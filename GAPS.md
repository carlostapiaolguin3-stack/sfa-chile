# Gaps del mercado SFA Chile

Vacíos que ningún player cubre hoy. Para cada uno: qué falta, por qué no se ha hecho, qué condiciones tendrían que darse para llenarlo.

Información al 2026-05-18. Si encuentras data nueva, abre un Pull Request.

---

## Gap 1: PFM consumer (Personal Finance Management)

**Qué falta:** una app tipo Mint, Fintonic o Maybe Finance para chilenos. Conecta cuentas, muestra dónde se va la plata, alerta de cobros raros, sugiere dónde ahorrar.

**Quién está hoy:** nadie con tracción consumer. Fintonic salió de Chile en 2024 tras el bloqueo de BancoEstado a iniciadores. Ningún banco chileno ofrece PFM nativo decente.

**Por qué nadie lo cubre:**
- Pre-SFA hay que hacer scraping con consentimiento, legalmente gris y técnicamente frágil
- Los bancos no quieren PFMs independientes (muestran al cliente la verdad de sus comisiones)
- Mercado consumer chileno chico (~5M de bancarizados activos), monetización difícil
- Fricción de mantenimiento manual del usuario alta (5-7 productos financieros separados con CSVs/PDFs distintos)

**Qué hace falta para llenarlo:**
- Esperar al SFA vigente (jul-2027) para sync automático
- O capital fuerte para mantener equipo de scraping permanente
- Forkear OSS maduro como Firefly III, Maybe Finance o Actual Budget
- Adaptación a Chile: UF nativo, categorías SII-friendly, importadores específicos por banco

---

## Gap 2: QR universal cross-wallet (post-RedPay)

**Qué falta:** un sticker QR único que cualquier comerciante pueda poner y cualquier cliente con cualquier wallet (MACH, Mercado Pago, Tenpo, Cuenta RUT, Copec Pay) pueda escanear.

**Quién está hoy:** nadie. RedPay murió el 31-jul-2025. Cada wallet opera QR cerrado.

**Por qué nadie lo cubre:**
- Las wallets no quieren interoperar (cada una compite por el cliente)
- Sin mandate regulatorio, no hay incentivo
- Pre-SFA, la única forma es negociar bilateral con cada wallet
- RedPay intentó esto y fracasó

**Qué hace falta para llenarlo:**
- Mandate de la CMF o del BCCh para QR interoperable (no está en la agenda confirmada)
- O un PSIP que orqueste vía SFA: el QR contiene un deep-link que abre la app del usuario y dispara una transferencia SFA
- Capital regulatorio para ser PSIP más acuerdos enterprise con wallets existentes

---

## Gap 3: Scoring crediticio API as a service

**Qué falta:** una API que tome data financiera de una persona o PYME (vía SFA cuando prenda, o vía Belvo/Floid hoy) y devuelva un score crediticio listo para usar por fintech lending.

**Quién está hoy:** Xepelin lo hace interno. Belvo y Floid venden data cruda, no scoring. Datamart hace algo similar para factoring B2B, no consumer.

**Por qué nadie lo cubre:**
- Construir modelos de scoring sólidos toma tiempo y data histórica
- Las fintechs lending lo hacen in-house porque les da edge competitivo
- Sin SFA productivo, el insumo de data está fragmentado

**Qué hace falta para llenarlo:**
- Acceso a data histórica para entrenar (vía partnership con un banco o fintech grande)
- Compliance UAF más CMF como prestador de información crediticia
- Modelo de pricing per-call o subscription B2B
- Diferenciación por nicho vertical (PYME retail, profesional independiente, cooperativas, etc.)

---

## Gap 4: Cobranza recurrente B2C consumer-facing

**Qué falta:** la versión consumer de Toku. Una app o SaaS que permita a un profesional independiente (kinesiólogo, profesor, peluquera) cobrar suscripciones recurrentes sin tener que hacer factura mensual ni perseguir transferencias.

**Quién está hoy:** Toku domina B2B (seguros, educación, real estate, USD 1.800M procesados al año). Para el profesional solo, nadie.

**Por qué nadie lo cubre:**
- Toku enfocó su capital en B2B (ticket más alto, churn más bajo)
- Pre-SFA el cobro recurrente requiere mandato bancario o autorización por cada cobro
- Mercado consumer chico individualmente pero grande en agregado

**Qué hace falta para llenarlo:**
- PSIP autorizado o reseller de Fintoc (que ya tiene débito directo)
- UX simple: cliente firma una vez, le cobran automático cada mes
- Modelo de pricing: porcentaje del cobro más tarifa fija mensual
- Foco vertical: deportes, salud, educación, servicios

---

## Gap 5: Pagos transfronterizos PSIP-to-PSIP LATAM

**Qué falta:** mandar plata Chile-Perú, Chile-Colombia, Chile-México, sin pasar por Wise, Western Union o dLocal. Que un PSIP chileno hable directo con un PSIP peruano vía estándar Open Finance.

**Quién está hoy:** nadie chileno. Prometeo (Uruguay) se acerca pero su core es agregación de data, no payments transfronterizos. Wise, dLocal y Bitso usan rails legacy más crypto.

**Por qué nadie lo cubre:**
- Cada país tiene Open Finance en estados distintos (BR maduro, CL en marcha, MX/PE/CO arrancando)
- Coordinación regulatoria cross-country es pesada
- Volumen de remesas Chile-LATAM es chico vs USA-México

**Qué hace falta para llenarlo:**
- Acuerdos bilaterales entre PSIPs de cada país
- Stack técnico que abstraiga las diferencias entre Open Finance BR/CL/MX/PE/CO
- Liquidity providers en cada moneda local
- Licencias en cada jurisdicción

---

## Gap 6: Verificación de cuenta para alta de clientes (KYC bank)

**Qué falta:** una API que un comercio o fintech pueda usar para verificar "este cliente realmente es dueño de esta cuenta bancaria" sin pedirle al cliente que suba foto de cartola.

**Quién está hoy:** Floid y Fintoc lo intentan tibio. Los bancos lo bloquean (no quieren que terceros vean su data sin pelea).

**Por qué nadie lo cubre bien:**
- Pre-SFA depende de scraping, que es frágil
- Bancos resisten (pierden data si verifican cuenta)
- Sin estándar SFA, cada banco devuelve formato distinto

**Qué hace falta para llenarlo:**
- SFA vigente (jul-2027) hace este caso trivial
- API simple: input RUT más número de cuenta más banco, output: confirma o rechaza
- Compliance UAF para datos personales

---

## Gap 7: Educación demand-side

**Qué falta:** contenido en español chileno, directo, para dueños de PYME y profesionales independientes, sobre qué les conviene del SFA y cómo prepararse.

**Quién está hoy:**
- Leo Soto (Shinkansen): vendor-side, no demand-side
- Prodigio: consultora system integrator para bancos, no demand-side
- FinteChile: gremio supply-side
- CMF: institucional seco

**Por qué nadie lo cubre bien:**
- Los players grandes son vendor-side y tienen conflicto de interés
- Los gremios son lentos
- Los medios de prensa cubren cuando hay noticia, no continuo

**Qué hace falta para llenarlo:**
- Repo público, newsletter, calculadora, videos, comparativas cross-país, plantillas para PYMES
- Consistencia 18 meses mínimo
- Cero agenda vendor (no vender infra ni servicios SFA, para preservar criticismo honesto)

Este repo busca llenar exactamente este gap.

---

## Tabla resumen

| Gap | Inversión inicial | Tiempo a tracción | Riesgo principal |
|---|---|---|---|
| 1. PFM consumer | Bajo | 6-12 meses | Adopción consumer lenta |
| 2. QR universal | Alto | 12+ meses | Necesita mandate regulatorio |
| 3. Scoring API | Medio | 12+ meses | Compliance más acceso a data |
| 4. Cobranza recurrente B2C | Bajo | 3-6 meses | Compite con Toku en agresividad |
| 5. Cross-border PSIP LATAM | Alto | 24+ meses | Coordinación multi-país |
| 6. Verificación cuenta | Bajo | Post-jul-2027 | Compete con Floid y Fintoc |
| 7. Educación demand-side | Muy bajo | 3 meses | Ejecución constante 18+ meses |

---

## Cómo contribuir

Si conoces a alguien intentando llenar uno de estos gaps que no esté listado, o detectas un gap nuevo, abre un Pull Request.
