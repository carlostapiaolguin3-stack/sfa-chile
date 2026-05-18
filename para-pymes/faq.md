# FAQ — Preguntas frecuentes para PYMES sobre el SFA

## Basicas

**¿Que es el SFA?**
Sistema de Finanzas Abiertas. Es la pieza de la Ley Fintec chilena que obliga a bancos, AFPs, aseguradoras y cooperativas a compartir tu informacion financiera con terceros autorizados, **si tú lo autorizas**.

**¿Cuando arranca?**
Julio 2027 (postergado de julio 2026). Sandbox voluntario abierto desde mayo 2026.

**¿Quien lo regula?**
La Comision para el Mercado Financiero (CMF), via la Norma de Caracter General N°514 (NCG 514).

**¿Es como PIX de Brasil?**
No exactamente. PIX es un sistema de pagos instantaneos operado por el Banco Central de Brasil. El SFA chileno es un sistema de intercambio de datos + iniciacion de pagos via APIs, operado por bancos privados bajo regulacion CMF. El SFA permitiria a un PSIP construir algo parecido a PIX, pero PIX en si requeriria que el Banco Central de Chile opere un switch propio (no esta en planes hoy).

## Para mi negocio

**¿Es obligatorio para mi PYME?**
No. El SFA te DA derechos, no te obliga a nada. Podes seguir cobrando con Transbank/MP/Klap como hoy si queres.

**¿Cuanto me puedo ahorrar?**
Estimacion: si hoy pagas 2.95% de comision al adquirente, con SFA via PSIP podrias pagar ~0.5-0.8%. En una PYME que vende $5M CLP/mes con tarjeta, son ~$1.2-1.5M CLP/año de ahorro.

**¿Tengo que comprar software o tecnologia?**
No. Tú como PYME no implementas SFA. Lo implementan los bancos y los PSIPs/PSBIs. Tú elegis usarlo o no.

**¿Mis clientes van a poder pagarme con SFA?**
Si, cuando esten disponibles los PSIPs autorizados (esperable Q4-2027 / Q1-2028). Tú contratas un PSIP (tipo Fintoc o uno nuevo), tu cliente paga via su cuenta bancaria con un click, y tú recibis la plata directo, mas rapido y mas barato.

**¿Mi banco me puede negar el acceso al SFA?**
No. Si tú consentiste y la institucion esta en el listado de obligados (todos los bancos lo estan en el Grupo 1), debe darte el servicio.

## Tecnicas y de cumplimiento

**¿Mis datos van a estar seguros?**
Mas seguros que hoy. Hoy si usas Fintoc o Khipu para algo, tenes que entregar tu clave del banco al proveedor (modelo scraping). Con SFA, no compartes clave: el banco te autentica directamente y autoriza el acceso al tercero usando OAuth 2.0 + FAPI 2.0.

**¿Como controlo que mi data se use bien?**
El SFA exige **consentimiento dinamico**: tú defines a quien le das acceso, a que datos especificos, por cuanto tiempo, y podes revocar en cualquier momento. Cada consentimiento tiene un maximo de 12 meses y debe renovarse.

**¿Que pasa si un proveedor usa mal mi data?**
La CMF puede sancionar y multar al PSBI/PSIP. Tú podes denunciarlo via SERNAC + CMF. Si hay daño civil, podes demandar.

**¿Que diferencia hay con un PSIP y un banco?**
Un PSIP NO custodia tu plata. Solo inicia ordenes de pago desde tu cuenta hacia un tercero. El banco sigue siendo donde tu plata vive. Si el PSIP quiebra, tu plata sigue en tu banco intacta.

## Comparativa con otros pais

**¿Como funciona en Brasil (Open Finance Brasil)?**
Brasil arranco en 2021. Hoy tiene 15M usuarios activos (8% de adultos bancarizados). Funciona, pero la adopcion fue mas lenta de lo esperado. Tomo 4 años llegar a esos numeros.

**¿Como funciono en Reino Unido (Open Banking UK)?**
UK arranco en 2018. Hoy tiene ~12M usuarios activos. PISPs como TrueLayer y Tink (esta ultima vendida a Visa en 2022) capturaron la mayor parte del valor.

**¿Y en Mexico (CoDi)?**
CoDi (2019) fracaso por falta de mandate fuerte a los bancos. Es el contraejemplo de lo que NO hacer.

## Sobre este repo

**¿Quien mantiene este repo?**
Carlos Tapia (carlostapia.cl) como proyecto educativo independiente. No es vendor ni representa a ningun banco / fintech.

**¿Como puedo contribuir?**
Abre un Pull Request en GitHub con mejoras, correcciones, casos nuevos, o data actualizada. Ver [CONTRIBUTING.md](../CONTRIBUTING.md).

**¿Esto es asesoria legal o financiera?**
No. Es informacion educativa. Para decisiones de cumplimiento normativo consulta con tu abogado o la CMF directamente.
