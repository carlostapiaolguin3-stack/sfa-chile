# Perú y Colombia — Yape, Plin, Bre-B

## Resumen ejecutivo

Perú no tiene marco formal de Open Finance, pero Yape y Plin (wallets sobre rails Visa/Mastercard) lograron interoperabilidad por presión del BCRP en 2023. Colombia lanzó Bre-B en oct 2025, el "PIX colombiano", con buena tracción inicial (34.6M usuarios en 6 meses). Casos opuestos: PE construyó sin regulación, CO sí con regulación.

## Perú: Yape y Plin

### Cronología
| Hito | Fecha |
|---|---|
| Yape lanzado (BCP) | 2017 |
| Plin lanzado (Interbank, BBVA, Scotiabank, BanBif) | 2020 |
| BCRP exige interoperabilidad | feb 2023 |
| Interoperabilidad productiva | sept 2023 |
| 15M+ usuarios totales | 2026 |

### Cómo funcionan
- **Yape**: wallet sobre BCP que permite enviar plata a cualquier número de celular peruano
- **Plin**: lo mismo pero coalición de 4 bancos (Interbank + BBVA + Scotiabank + BanBif)
- Corren sobre rails Visa/Mastercard, NO sobre rail propio del Banco Central
- Liquidación T+0 dentro de horario bancario

### Lo que funcionó
1. **UX simple**: enviar plata por celular sin saber cuenta bancaria
2. **Adopción masiva**: 60%+ de adultos bancarizados PE usan al menos una
3. **Comercios chicos**: street vendors aceptan Yape/Plin como cash
4. **Interoperabilidad forzada por BCRP**: 2023 obligación, no opcional

### Lo que NO funcionó
1. **Sin rail propio del Banco Central**: depende de Visa/MC, costo subyacente alto
2. **Sin Open Finance formal**: data no es portable
3. **Cap de monto bajo**: tickets grandes siguen siendo SPEI/transferencia tradicional
4. **No es PSIP-PSIP**: no hay tercero que pueda iniciar pago en nombre del cliente

### Players Perú
- **BCP / Credicorp**: dueño de Yape + Krealo (CVC). Invirtió en Shinkansen Chile
- **Interbank + Plin coalición**
- **Tunki, Lukita, Bim**: wallets menores
- **Belvo, Prometeo**: aggregators con cobertura PE

## Colombia: Bre-B

### Cronología
| Hito | Fecha |
|---|---|
| Decreto Banco República | jul 2024 |
| Bre-B lanzamiento | oct 2025 |
| 5M usuarios | dic 2025 |
| 20M usuarios | mar 2026 |
| 34.6M usuarios (64% población adulta) | abr 2026 |

### Cómo funciona
- Sistema de pagos instantáneos operado por el Banco de la República
- Cuenta vía Llaves (alias humano-friendly: celular, email, cédula)
- 24/7/365, gratuito P2P, 0.33% P2B para comercios chicos
- Stack ISO 20022 + RTGS
- Modelo idéntico al PIX brasileño

### Lo que está funcionando
1. **Mandate fuerte**: Banco de la República obligó a 50 entidades el día 1
2. **Branding único**: "Bre-B" como marca consumer pública
3. **Llaves UX**: registrar tu celular como llave es trivial
4. **Adopción agresiva**: 34.6M en 6 meses supera ritmo de adopción PIX

### Lo que es muy temprano para evaluar
- Si Bre-B reemplaza tarjetas en e-commerce (PIX tardó 2 años en hacerlo)
- Si las comisiones se mantienen bajas o se inflan
- Si entran PISPs/PSBIs de Open Finance encima de Bre-B

### Players Colombia
- **Bancolombia, Davivienda, Banco de Bogotá, BBVA Colombia**: top bancos
- **Nequi (Bancolombia), Daviplata (Davivienda), Movii**: wallets digitales
- **Rappi**: marketplace + pagos
- **Quanto, Skandia, Tpaga**: fintech

## Diferencias clave PE vs CO vs CL

| Aspecto | Perú | Colombia | Chile |
|---|---|---|---|
| Sistema instant payments | Yape + Plin (privado) | Bre-B (Banco República) | Ninguno definido |
| Rail | Visa/MC | Propio Banco República | Va a montarse sobre TEF + SFA |
| Open Finance | Sin marco formal | En desarrollo | NCG 514 vigente jul 2027 |
| Branding consumer | Yape (privado), Plin (coalición) | "Bre-B" (Banco República) | "SFA" (CMF, sin awareness aún) |
| Mandate adopción | Tibio (interop sí, lo demás no) | Fuerte | Fuerte en ley, pendiente en plazos |

## Lecciones para Chile

### De Perú
- Adopción masiva consumer es posible sin Open Finance formal, si la UX es buena
- Coalición de bancos puede funcionar (Plin) si la presión regulatoria es real (BCRP feb 2023)
- Dependencia de Visa/MC es deuda a largo plazo. Chile debería evitarla con SFA + PSIP directo

### De Colombia
- Mandate fuerte + branding único + 24/7 + gratuito = fórmula PIX que funciona
- Pre-vigencia comunicación masiva ayuda (Banco República hizo campaña 6 meses pre-launch)
- Si el Banco Central opera el rail, los privados no lo sabotean

### Oportunidades editoriales en la región

- En Perú no hay un divulgador independiente que ocupe el rol entre Yape, Plin y el usuario PYME. Las marcas mismas dominan el discurso
- En Colombia Bre-B es muy nuevo, hay espacio para divulgación independiente pero el Banco de la República también juega ese rol
- En Chile nadie ocupa el rol de educador demand-side. Ventana abierta para contenido independiente

## Fuentes

- BCRP Yape/Plin reports
- Banco de la República Colombia Bre-B stats
- iupana cobertura LATAM continua
- Konsentus análisis comparativos
- Infobae Bre-B vs Pix vs CoDi
- ecollect Bre-B análisis
