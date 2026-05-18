# Bancos y emisores chilenos vs SFA

Estado al 2026-05-18. Si encontrás info nueva, abre PR.

## Bancos obligados (todos en Grupo 1)

| Banco | Sandbox CMF | Portal developers | Open Banking activo | Contacto Open Banking |
|---|---|---|---|---|
| BancoEstado | SÍ (confirmado público) | No portal público | Vía scraping bloqueado/desbloqueado | leyfintec@cmfchile.cl |
| Santander Chile | No confirmado | No portal CL | Vía aggregators | LinkedIn empleados |
| BCI | No confirmado | developers.bci.cl + apimarket.bci.cl | Sí desde 2017, sandbox + Fintech Program | Pablo Da Rold (Head Open Banking, ganó Silver Fintech Americas 2026) |
| Banco de Chile | No confirmado | apistore.bancochile.cl | Portal sí, doc pobre | Vía web del banco |
| Itaú Chile | No confirmado | No portal CL | Vía aggregators | LinkedIn |
| Falabella | No confirmado | No portal | Vía aggregators | LinkedIn |
| BICE | No confirmado | No portal | Limitado | Web |
| Security | No confirmado | No portal | Limitado | Web |
| Scotia | No confirmado | No portal | Vía aggregators | LinkedIn |
| Consorcio | No confirmado | No portal | Limitado | Web |
| Internacional | No confirmado | No portal | Limitado | Web |
| HSBC Chile | No confirmado | No portal CL | Vía aggregators | Casa matriz |
| JP Morgan Chile | No confirmado | No portal CL | Limitado | Casa matriz |
| Ripley | No confirmado | No portal | Limitado | Web |

## Emisores de tarjetas no bancarios (Grupo 1)

| Emisor | Producto | Sandbox CMF | Notas |
|---|---|---|---|
| Tenpo | Wallet prepago | No confirmado | Aprobada por CMF como CPF |
| MACH (BCI) | Wallet + ahora MachBank | No confirmado | 6M+ usuarios, ahora también TC |
| Mercado Pago | Wallet + acquirer | SÍ (confirmado público) | 7/10 prepagos en CL |
| Copec Pay | Wallet | No confirmado | Foco combustibles |
| Tap | Wallet | No confirmado | |
| Fintoc | Acquirer + recién CPF (cód 764 may-2026) | No confirmado | Nuevo emisor formal |

## Cooperativas y AFP (Grupo 2)

| Entidad | Tipo | Notas |
|---|---|---|
| Coopeuch | Cooperativa | Ya activa con piloto Demo Day CCS + 6 startups SFA |
| Coocretal | Cooperativa | Sin actividad pública SFA |
| Provida | AFP | Grupo 2 |
| Habitat | AFP | Grupo 2 |
| Capital | AFP | Grupo 2 |
| Cuprum | AFP | Grupo 2 |
| Modelo | AFP | Grupo 2 |
| Planvital | AFP | Grupo 2 |
| Uno | AFP | Grupo 2 |

## Aseguradoras (Grupo 2)

Las top: BICE Vida, Consorcio Seguros, Sura, Mapfre, MetLife, Penta. Sin actividad pública específica SFA todavía.

## Bancos sistémicos (CMF mar-2026)

Estos 5 cargan con escrutinio adicional pero NO plazo más temprano en SFA:
- Santander Chile
- BCI
- Banco de Chile
- BancoEstado
- Itaú Chile

## Players con portales developer activos

### BCI

URL: developers.bci.cl + apimarket.bci.cl

Tiene desde 2017. APIs públicas hoy:
- Cajeros automáticos
- Sucursales
- Indicadores económicos (UF, USD, cobre)

APIs detrás de programa Fintech con due diligence:
- Cuentas, pagos, créditos
- Hasta USD 40k de financiamiento a pilotos

Contacto: Pablo Da Rold (Head Open Banking BCI), ganó Silver Fintech Americas 2026.

### Banco de Chile

URL: apistore.bancochile.cl

Portal existe con sandbox público. Documentación pobre, no clara cobertura.

## Lo que pasa con los demás

- Santander: developer.santander.co.uk es solo UK. No hay portal CL
- BancoEstado: no tiene portal público. Acceso solo vía scraping del flow Cuenta RUT
- Itaú, Falabella, BICE, Security: sin portal público
- HSBC, JP Morgan: portales internacionales, no CL específico

## Episodios públicos relevantes

### Bloqueo BancoEstado a iniciadores (ago 2024)

BancoEstado implementó nuevo estándar de ciberseguridad que bloqueó scraping de Khipu, Etpay, Fintoc, Fintonic y Floid. Tras presión gremial y recurso de protección de Khipu a Corte Suprema, hubo acuerdos parciales. Fintonic salió de Chile permanentemente. El resto opera de forma limitada.

Conclusión: pre-SFA los bancos pueden bloquear cuando quieran. Post-SFA no podrán.

### Demo Day Coopeuch + CCS (oct 2025)

Coopeuch fue el primer caso público de cooperativa adoptando rol piloto de IPI. 6 startups participaron: Datamart, Floid, Enrólate, Synaptic, Infocheck, Frigate (este último ecuatoriano, no chileno).

Demuestra que cooperativas van más rápido que bancos top.

## Cómo contribuir a este mapa

Si trabajás en un banco o tienes info de su roadmap SFA real (vs vapor de marketing), abre PR. Anónimo está OK si la fuente es válida.

## Fuentes

- CMF Foro SFA participantes
- Apertura sandbox CMF: chocale.cl
- BCI developers + Pablo Da Rold LinkedIn
- Banco de Chile apistore
- DF cobertura bloqueo BancoEstado vs iniciadores
- CCS Coopeuch Demo Day comunicación oficial
