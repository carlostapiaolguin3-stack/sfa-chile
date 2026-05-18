# Checklist: como prepararte para el SFA si tienes una PYME

5 pasos en orden. Ninguno requiere ser tecnico ni gastar plata todavia.

## Paso 1: entiende cuanto te puede ahorrar

Hoy pagas comision por cada cobro con tarjeta. Con el SFA vas a poder ofrecer al cliente que te pague directo desde su cuenta bancaria, mucho mas barato.

Ejemplo concreto:
- Vendes $5.000.000 CLP al mes con tarjeta de credito
- Comision Transbank: ~2.95% = $147.500 CLP/mes en fee
- Con SFA (estimado): ~0.5-0.8% = $25.000 - $40.000 CLP/mes
- Ahorro mensual: entre $107.000 y $122.500 CLP
- Ahorro anual: entre $1.284.000 y $1.470.000 CLP

Si tu ticket promedio es bajo (cafe, kiosko, peluqueria), el ahorro es proporcionalmente todavia mayor. Calculadora interactiva proximamente en este repo.

## Paso 2: identifica con que banco trabajas y cuando le toca

- Banco Estado, BCI, Santander, Chile, Itau, Falabella, BICE, Security, Scotia: todos en Grupo 1, obligados a publicar APIs entre los meses 5 y 18 desde julio 2027.
- Cooperativas (Coopeuch, Coocretal): Grupo 2, ~15 meses despues que el Grupo 1.
- AFP, aseguradoras: Grupo 2.

En la practica: si tu banco principal esta en el Grupo 1, podes empezar a usar SFA entre **diciembre 2027 y enero 2029**.

## Paso 3: pidele a tu banco su roadmap SFA

Hoy, sin SFA vigente, los bancos no estan obligados a contestarte. Pero **preguntarles formalmente sirve para dos cosas**:

1. Si todos los clientes preguntan, los bancos suben SFA en su prioridad interna.
2. Sabes con que tiempo real cuentas para planificar.

Plantilla de email lista en este repo: [plantillas/email-banco-roadmap-sfa.md](./plantillas/email-banco-roadmap-sfa.md).

## Paso 4: evalua tu stack actual de cobro

Que herramientas usas hoy para cobrar:

| Herramienta | Que va a pasar con SFA |
|---|---|
| Transbank Webpay | Sigue funcionando pero perdera competitividad. Vas a poder ofrecer alternativa via PSIP |
| Mercado Pago | Sigue. MP es a la vez emisor y posible PSIP |
| Klap / Getnet / Compraqui | Siguen, pero compiten con PSIPs sub-1% |
| Khipu / Fintoc / Etpay / Floid | Estos ya son PSIPs de facto. Con SFA pasan a estandar oficial y bajan precios |
| Efectivo / transferencia manual | Se va a digitalizar mucho mas facil con PSIPs |

Si hoy ya usas Fintoc o Khipu para algo: estas adelantado. Cuando SFA prenda solo migras al estandar oficial.

## Paso 5: monitorea el SFA

El calendario CMF puede cambiar (ya se postergó 12 meses). Para no perderte:

- Sigue este repo en GitHub (botón "Watch")
- Sigue a la CMF en LinkedIn
- Sigue a FinteChile y Shinkansen para perspectiva de la industria
- Revisa medios fintech (Tekios, iupana, LatamFintech, DF Banca-Fintech)

---

## Bonus: que NO hacer

- **No contrates "consultoria SFA" todavia.** El SFA no esta vigente y nadie tiene experiencia real implementandolo en Chile. Las consultoras que ofrecen "te preparamos para SFA" estan vendiendo aire o reciclando docs de Brasil.
- **No cambies de banco solo por el SFA.** Todos los bancos chilenos van a estar obligados. Cambia por otras razones (comisiones actuales, atencion, productos).
- **No instales todavia software complejo de Open Banking.** Hasta que la CMF publique el Anexo Tecnico final (esperado Q3-2026), cualquier integracion la vas a tener que rehacer.

---

## FAQ resumida

**¿El SFA me obliga a hacer algo?**
No. El SFA te DA derechos (compartir tu data si queres, cobrar mas barato si queres). No te obliga a usarlo.

**¿Tengo que pedir permiso a la CMF para usar SFA?**
No, tú como cliente final. Si tú eres PROVEEDOR de servicios (PSBI o PSIP), entonces si — debes inscribirte en el RPSF.

**¿Mis datos van a estar mas seguros o menos?**
Mas seguros. Hoy compartes tu clave del banco con la fintech (modelo scraping). Con SFA, no compartes la clave: el banco autentica al cliente y autoriza el acceso al tercero. Mucho mejor.

**¿Mi banco puede negarme dar acceso a SFA?**
No. Si esta en el listado de obligados y tú consentiste, debe darte el servicio.

**¿Cuando empieza realmente?**
Julio 2027 (postergado de julio 2026). Sandbox voluntario abierto desde mayo 2026.
