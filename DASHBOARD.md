# Dashboard de implementación SFA Chile

Estado real, no normativo. Al **2026-05-18**.

Cada acción tiene 3 etiquetas:
- **HACER YA**: condiciones cumplidas, ejecutable hoy
- **BLOQUEADO**: depende de algo externo, ver "Condición precedente"
- **OBSERVAR**: vivo pero sin acción requerida todavía

---

## Hitos macro

| Hito | Fecha | Estado | Notas |
|---|---|---|---|
| Ley Fintec 21.521 publicada | 4-ene-2023 | OK | Diario Oficial |
| Título III vigente | 3-feb-2023 | OK | BCN |
| NCG 514 dictada | 3-jul-2024 | OK | CMF |
| Consulta pública modificación NCG 514 | 12-nov-2025 a 12-dic-2025 | OK | Cerrada |
| Consulta pública Anexo Técnico v2 | hasta 9-feb-2026 | OK | Cerrada |
| **Publicación NCG 514 modificada (texto final)** | esperada Q2-Q3 2026 | PENDIENTE | Sin fecha exacta confirmada |
| **Publicación Anexo Técnico N°3 final** | esperada Q3-2026 | PENDIENTE | Hasta que no salga, ningún stack es definitivo |
| Sandbox + Directorio CMF habilitados | ~oct-2026 | OBSERVAR | 9 meses pre-vigencia |
| Sandbox voluntario CMF Fase 1 | ABIERTO desde may-2026 | HACER YA | leyfintec@cmfchile.cl |
| Piloto voluntario | oct-2026 hasta vigencia | OBSERVAR | |
| **Vigencia plena SFA** | ~jul-2027 | OBSERVAR | Postergada de jul-2026. Riesgo de 2do retraso a 2028 |
| Piloto obligatorio (SLA reducido) | 2 meses post-vigencia | OBSERVAR | |
| IPI Grupo 1 publica APIs | meses 5-18 desde vigencia | OBSERVAR | dic-2027 a ene-2029 |
| IPI Grupo 2 publica APIs | 15 meses post-vigencia | OBSERVAR | ~oct-2028 |

---

## Acciones para tú hoy

### 1. Mandar mail a leyfintec@cmfchile.cl pidiendo info del sandbox

- **Estado:** HACER YA
- **Costo:** 10 minutos
- **Condición precedente:** ninguna
- **Bloquea otras acciones:** no
- **Por qué importa:** te metés en el radar CMF, accedes a documentación temprana, ganas contexto

### 2. Mandar mail a hola@fintechile.org pidiendo entrar al Comité SFA

- **Estado:** HACER YA
- **Costo:** 10 minutos + ser asociado/partner FinteChile
- **Condición precedente:** ninguna real (la asociación se evalúa caso a caso)
- **Bloquea otras acciones:** no
- **Por qué importa:** entras a la mesa donde se cocina la implementación. Networking + voz oficial

### 3. Registrarse en charly.io de Start-Up Chile

- **Estado:** HACER YA
- **Costo:** 15 minutos
- **Condición precedente:** ninguna
- **Bloquea otras acciones:** no
- **Por qué importa:** cuenta lista para el próximo batch (sept-oct 2026), sin presión de postular ahora

### 4. Forkear `magnobiet/open-banking-brazil` y empezar `awesome-sfa-chile`

- **Estado:** HACER YA
- **Costo:** 1 día para la primera versión decente
- **Condición precedente:** ninguna
- **Bloquea otras acciones:** no
- **Por qué importa:** primer activo de autoridad técnica. Google indexa awesome-lists muy bien

### 5. Forkear `firefly-iii/firefly-iii` para demo PFM chileno

- **Estado:** HACER YA
- **Costo:** 1 fin de semana para deploy + locale es-CL + importador 1 banco
- **Condición precedente:** ninguna
- **Bloquea otras acciones:** no
- **Por qué importa:** killer demo de "monté un Mint chileno en 1 finde con OSS". Tu vehículo de autoridad

### 6. Lanzar newsletter "SFA en Tu Negocio" (Substack)

- **Estado:** HACER YA
- **Costo:** 2 hrs setup + 2 hrs/semana
- **Condición precedente:** ninguna
- **Bloquea otras acciones:** no
- **Por qué importa:** activo recurrente de tracción. Métrica clara (subs) para evaluar a mes 3

### 7. Mandar email a Pablo Da Rold (BCI Open Banking) vía LinkedIn

- **Estado:** HACER YA
- **Costo:** 15 minutos
- **Condición precedente:** ninguna
- **Por qué importa:** primer contacto con la persona del lado banco que más sabe. Te abre puertas

---

## Acciones que NO puedes hacer todavía (BLOQUEADAS)

### 8. Inscribirse como PSIP o PSBI en RPSF

- **Estado:** BLOQUEADO
- **Condición precedente:** NCG 514 vigente + apertura formal del registro PSIP/PSBI
- **Fecha estimada habilitación:** Q1-2027 (6 meses pre-vigencia)
- **Costo cuando se habilite:** capital UF 5.000-30.000 + garantía proporcional + S.A. giro exclusivo + 6 meses CMF + 6 meses marcha blanca
- **Acción mientras tanto:** entender NCG 502 + montar Keycloak FAPI 2.0 sandbox para entrenar

### 9. Conectarse a APIs oficiales SFA de bancos chilenos

- **Estado:** BLOQUEADO
- **Condición precedente:** Anexo Técnico N°3 final + bancos publicando APIs
- **Fecha estimada habilitación:** dic-2027 al menos
- **Acción mientras tanto:** entrenar con specs Open Finance Brasil (idénticas en stack: FAPI 2.0 + OAuth 2.0 + mTLS)

### 10. Postular Semilla Expande CORFO

- **Estado:** BLOQUEADO (convocatoria cerrada)
- **Condición precedente:** próximo llamado Q1 2027
- **Costo cuando se habilite:** preparar memoria + cofinanciamiento 25%

### 11. Postular UDD CFO Academy / Invest Tech

- **Estado:** BLOQUEADO (convocatorias cerradas may-2026)
- **Acción mientras tanto:** monitorear próximo Go! Startup UDD

### 12. Construir SFA Sandbox Tracker con instituciones inscritas

- **Estado:** PARCIALMENTE BLOQUEADO
- **Condición precedente:** que la CMF publique listado de participantes del sandbox (hoy no lo hace)
- **Acción mientras tanto:** monitorear vía Tekios + LatamFintech + scraping de prensa, armar versión preliminar manualmente

### 13. Construir Calculadora SFA con tasas reales de PSIPs

- **Estado:** PARCIALMENTE BLOQUEADO
- **Condición precedente:** PSIPs autorizados publicando tarifas oficiales (Fintoc y Khipu ya publican)
- **Acción mientras tanto:** armar versión con estimaciones razonables + comparación contra Webpay/MP/Klap

### 14. Postular Start-Up Chile BIG 12 (esta semana)

- **Estado:** HACER YA pero NO RECOMENDADO
- **Condición precedente:** producto con tracción medible + dedicación exclusiva 4 meses + presencia en Chile
- **Razón para esperar:** Triggers/Scheduler no tienen métricas duras todavía, 7 días es apurado, próximo batch sept-oct 2026 te da 4-5 meses para juntar clientes paying

---

## Riesgos y dependencias

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Segundo retraso del SFA a 2028 | Media | Alto | Diversificar contenido cross-país, no atar todo a fecha chilena |
| CMF publica Anexo Técnico distinto al esperado | Baja | Medio | Apostar a FAPI 2.0 estándar (es lo que dicen las consultas) |
| BancoEstado/Santander sabotean adopción | Media | Medio | Documentar incumplimientos públicamente, presión via Bancada Startup |
| Shinkansen captura todo el mindshare técnico | Alta | Bajo (no es mi target) | Posicionarme demand-side donde Leo no juega |
| Fintoc lanza producto demand-side primero | Media | Alto | Velocidad de ejecución 90 días + diferenciación tono educador |
| El sandbox CMF nunca abre o se mantiene cerrado al público | Baja | Bajo | El sandbox ya abrió may-2026 |

---

## Métricas a trackear

| Métrica | Objetivo 3 meses | Objetivo 6 meses | Objetivo 12 meses |
|---|---|---|---|
| Subs newsletter | 500 | 1.500 | 5.000 |
| Stars repo sfa-chile | 50 | 200 | 800 |
| PRs externos al repo | 5 | 20 | 60 |
| Gremios PYME con licencia del boletín | 0 | 1 | 3 |
| Speaking en eventos sectoriales | 0 | 1 | 3 |
| Contactos en CMF/FinteChile/bancos | 5 | 15 | 30 |
| MRR del boletín (paid + B2B2C) | 0 | $500k CLP | $3M CLP |

Punto de corte: si en 3 meses no hay 500 subs + 1 gremio interesado, cierre limpio.

---

## Próximos updates de este dashboard

- Cuando salga NCG 514 modificada (esperado Q2-Q3 2026)
- Cuando salga Anexo Técnico N°3 final (esperado Q3-2026)
- Cuando la CMF publique listado de participantes del sandbox
- Cuando se anuncie próximo batch Start-Up Chile (sept-oct 2026)
- Cuando se anuncie próximo Demo Day Coopeuch+CCS (esperable Q4-2026)

PRs bienvenidos cuando detectes cambios antes que yo.
