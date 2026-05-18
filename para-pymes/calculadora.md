# Calculadora: cuánto te ahorra el SFA

Versión texto. La interactiva (web) viene después.

## Fórmula simple

```
Ahorro mensual = Volumen mensual × (Tasa actual − Tasa SFA estimada)
```

## Tasas de referencia

**Lo que pagas hoy:**

| Medio de pago | Tasa al comercio típica |
|---|---|
| Transbank débito | 1.49% + IVA |
| Transbank crédito | 2.95% + IVA |
| Mercado Pago Point | 2.99% + IVA (varía por tier) |
| Klap / Getnet / Compraquí | 0.99% a 2.9% según volumen y tier |
| Webpay (online crédito) | 2.95% + IVA + $25 CLP fijo |
| Fintoc / Khipu / Etpay / Floid (PSIPs pre-SFA) | ~1% + IVA |

**Lo que pagarías con SFA (estimado):**

| Vía | Tasa estimada |
|---|---|
| PSIP autorizado SFA (oficial) | 0.5% a 0.8% |
| Transferencia directa con QR universal (si llega) | 0.3% a 0.5% |

El estimado se basa en lo que cobran los iniciadores hoy con costo de scraping (~1%). Con APIs oficiales el costo operacional baja y la competencia presiona el precio a la mitad.

## Ejemplos por tipo de PYME

### Cafetería de barrio (ticket promedio $3.500, 1.500 clientes/mes)

- Volumen mensual: $5.250.000 CLP
- 70% paga con débito Transbank: $3.675.000 × 1.49% = $54.756
- 30% paga con crédito Transbank: $1.575.000 × 2.95% = $46.463
- **Total comisiones hoy: ~$101.000 CLP/mes**

Con SFA (todos los clientes pagan vía PSIP, asumiendo 0.7%):
- $5.250.000 × 0.7% = $36.750
- **Ahorro: $64.000 CLP/mes ($768.000/año)**

### Ferretería barrial (ticket promedio $15.000, 800 clientes/mes)

- Volumen mensual: $12.000.000 CLP
- 50% débito, 50% crédito
- Comisiones hoy: $12M × promedio 2.22% = ~$266.400 CLP/mes
- Con SFA 0.7%: $84.000
- **Ahorro: $182.400 CLP/mes ($2.189.000/año)**

### Profesional independiente (kinesiólogo, $30.000 por sesión, 80 sesiones/mes)

- Volumen mensual: $2.400.000 CLP
- 90% crédito (más cómodo en consulta)
- Comisiones hoy: $2.400.000 × 0.9 × 2.95% = ~$63.720 CLP/mes
- Con SFA 0.7%: $16.800
- **Ahorro: $47.000 CLP/mes ($564.000/año)**

### SaaS chico (B2B recurrente, $50.000 CLP/mes × 100 clientes)

- Volumen mensual: $5.000.000 CLP recurrente
- Hoy con Webpay crédito + Toku (cobranza): ~3.5% all-in = $175.000 CLP/mes
- Con SFA + débito directo PSIP: 0.8% = $40.000
- **Ahorro: $135.000 CLP/mes ($1.620.000/año)**

### E-commerce mid-market ($25M CLP/mes)

- Hoy con Webpay crédito + Mercado Pago: promedio 3% = $750.000 CLP/mes
- Con SFA via PSIP: 0.7% = $175.000
- **Ahorro: $575.000 CLP/mes ($6.900.000/año)**

## Cómo armar tu cálculo

1. Baja la cartola de Transbank/MP/Klap del último mes
2. Identifica monto total cobrado + monto comisión deducida
3. Aplica regla de tres: si volumen es X y comisión actual es Y%, con SFA al 0.7% ahorrás (Y − 0.7)% sobre X
4. Multiplica por 12 para anualizado

## Advertencia importante

Estos números son **estimaciones**, no garantías. Las tasas reales del SFA dependen de:

- Cuántos PSIPs lleguen al mercado y cuán competitivos sean
- Si los bancos cumplen con SLAs o cobran fees por uso del rail
- Si la CMF mete tope de tarifa o no
- Tu volumen real (a más volumen, mejor tasa negociada)
- Tu tipo de cobro (online vs presencial, recurrente vs spot)

Para versión interactiva web con tu volumen real, esperá la calculadora live en `carlostapia.cl/sfa` (próximamente).

## Próximos pasos

1. Si el ahorro proyectado te parece relevante: [arrancá el checklist de preparación](./checklist.md)
2. Si quieres que tu banco te confirme su roadmap: [usa la plantilla de email](./plantillas/email-banco-roadmap-sfa.md)
3. Si tienes dudas: revisá la [FAQ](./faq.md)
