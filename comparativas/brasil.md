# Brasil — Open Finance Brasil

## Resumen ejecutivo

Brasil arrancó en 2021, hoy es el referente mundial de Open Finance. Chile copia el stack técnico (FAPI 2.0 + mTLS + OAuth 2.0) y la arquitectura (Directorio central + APIs obligatorias). Lo que Chile NO copia: PIX (sistema de pagos instantáneos operado por el BCB) y la gobernanza descentralizada.

## Diferencias clave Brasil vs Chile

| Aspecto | Brasil | Chile |
|---|---|---|
| Operador del switch instantáneo | Banco Central (PIX) | Sin equivalente. SFA va sobre rails bancarios + PSIPs |
| Regulador | BCB (Banco Central) | CMF |
| Ley habilitante | Ley 12.865/2012 + Resolución 2020 | Ley 21.521/2023 |
| Plazo norma a productivo | 28 meses | 36 meses (postergado) |
| Bancos obligados | Top 13 + voluntarios | Grupo 1 (todos bancos) + Grupo 2 (cooperativas/AFP/aseguradoras) |
| Stack técnico | FAPI 1.0 → FAPI 2.0 | FAPI 2.0 directo |
| ISO 20022 obligatorio | Sí | No (JSON sobre OpenAPI 3.1) |
| Capital mínimo IP | R$2M (~USD 400k) | UF 5.000-30.000 según tramo |
| Branding | "Open Finance Brasil" oficial | "SFA" oficial, sin marca consumer |

## Cronología Brasil

| Hito | Fecha |
|---|---|
| Ley 12.865 | 2012 (habilitante) |
| Resolución BCN/BCB | mayo 2020 |
| Fase 1 (datos públicos) | feb 2021 |
| Fase 2 (datos cliente) | ago 2021 |
| Fase 3 (iniciación pagos) | oct 2021 a sept 2022 |
| Fase 4 (FX, inversiones, seguros) | sept 2022 |
| Implementación completa | sept 2022 |
| 100M consentimientos acumulados | 2025 |
| 15M usuarios activos | 2026 |

## Lo que funcionó

1. **PIX (paralelo a Open Finance)**: instant payments del BCB, 90% de adultos lo usan. P2P gratuito, P2B 0.33%. Reemplazó tarjetas en e-commerce
2. **Mandate fuerte**: BCB obligó a top 13 bancos día 1, no negociación
3. **Branding único**: la marca "Open Finance Brasil" la maneja el BCB, no compite con 12 marcas privadas
4. **Iniciación de pagos**: pegó fuerte. Pluggy, Belvo, Klavi se volvieron infra crítica
5. **Stack técnico claro**: FAPI 2.0 + ICP-Brasil + Directorio centralizado. Sin ambigüedad

## Lo que NO funcionó

1. **Adopción consumer de lectura de datos**: 8% de bancarizados en 4 años. La gente no entiende por qué compartir su info
2. **Performance interbancaria**: SLAs incumplidos, downtime en bancos legacy
3. **Costo de cumplimiento**: PSBIs y PSIPs operan a pérdida. Solo escala salva
4. **Educación financiera**: no se invirtió suficiente. CMF/BCB no hicieron campañas masivas
5. **Gestión de consentimientos**: drop-off del 30-40% al renovar cada 12 meses

## Players brasileños relevantes

### Bancos
- Itaú, Bradesco, Santander, Banco do Brasil, Caixa, Nubank, BTG Pactual, XP

### Infraestructura / Aggregators
- **Pluggy**: USD 6M raised, +400 clientes, foco LATAM (incluye CL)
- **Belvo**: USD 74M raised total, ahora cubre BR/MX/CO/CL
- **Klavi**: aggregator chico pero técnico
- **Quanto**: data + iniciación pagos
- **Iniciador**: PSIP especializado
- **Cuore**: tooling para fintechs

### Bancos digitales con Open Finance nativo
- **Nubank**: usa Authlete como AS, FAPI 2.0 desde día 1
- **C6 Bank**, **Inter**, **PicPay**

### Vendor enterprise
- **Sensedia**: API management líder en BR para Open Finance
- **NRD**, **Provider IT**, **CI&T**

### Referentes públicos
- **Bruno Diniz** (Spiralem): el divulgador top, LinkedIn Top Voice. Casi el "Diniz chileno" que el SFA va a generar acá
- **João Lima** (Iniciador): voz técnica
- **Carolina Cury** (Banco Central): voz oficial

## Recursos para aprender

- Portal: openfinancebrasil.org.br
- Docs técnicos: openfinancebrasil.atlassian.net
- GitHub org: github.com/OpenBanking-Brasil
- Awesome list: github.com/magnobiet/open-banking-brazil
- Bruno Diniz: brunodiniz.com

## Lo que Chile debería aprender

1. **Mandate fuerte day-1**: no negociar con bancos por features. Que CMF use poder regulatorio
2. **Educar al consumidor antes**: campaña masiva 6 meses pre-vigencia
3. **Branding único**: que CMF defina marca consumer "SFA" como marca de confianza, no las wallets propias
4. **Iniciación de pagos primero**: Brasil la dejó para fase 3. Chile la pone como hito intermedio prioritario, mejor
5. **Que el PIX-equivalente venga después o nunca**: SFA + PSIPs cubre 80% del use case sin necesidad de rail propio del BCCh

## Lecciones para tú como operador

- Brasil tardó 5 años en tener creator que monetice educación (Diniz). Chile tiene espacio igual
- El segmento PYME demand-side estuvo desatendido durante el rollout brasileño. Ventana 18 meses para tú
- El Directorio + sandbox son donde se cocina todo. Estar dentro temprano paga

## Fuentes

- openfinancebrasil.org.br
- Bruno Diniz LinkedIn + brunodiniz.com
- Sensedia reports anuales
- BIS Bulletin sobre Open Finance LATAM
- World Bank Pix Case Study (mayo 2022)
- HBS Case "Instant Payment Mandate" sobre BCB
