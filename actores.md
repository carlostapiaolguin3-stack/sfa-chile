# Actores del SFA — PSIP, PSBI, IPI, IPCP explicados

El SFA tiene una sopa de letras. Aca te la traducimos.

## Diagrama base

```
+--------------------------+
|  Personas / PYMES        |
|  (dueñas de su info)     |
+--------------------------+
       |              |
       | consentimiento|
       v              v
+--------------+   +--------------+
|     IPI      |   |    PSBI      |
| (banco que   |   | (quien quiere|
|  guarda data)|   |  ver la data)|
+--------------+   +--------------+
       \                  /
        \   APIs FAPI    /
         \    SFA       /
          v            v
       +----------------+
       |   Directorio   |
       |      CMF       |
       +----------------+
```

## IPI — Instituciones Proveedoras de Informacion

Son los que **tienen tu data financiera y la guardan**.

Ejemplos: Banco Santander, BCI, BancoEstado, Itau, Falabella, Banco de Chile, BICE, Security, Tenpo, Mach, Mercado Pago, AFP Provida, AFP Habitat, BICE Vida, Consorcio Seguros, etc.

**Grupo 1** (los primeros obligados): bancos + emisores de tarjetas (Tenpo, Mach, Mercado Pago, Copec Pay, etc.).
**Grupo 2** (despues): cooperativas (Coopeuch, Coocretal), aseguradoras, AGFs.

Obligacion: **publicar APIs FAPI 2.0 que permitan que terceros consulten tu data si tu lo autorizas**.

## IPCP — Instituciones Proveedoras de Cuentas de Pago

Son IPIs que ademas **administran cuentas desde las que se pueden iniciar pagos**.

En la practica: bancos + emisores de tarjetas de pago con provision de fondos (Tenpo, Mach, Mercado Pago).

Obligacion adicional: aceptar instrucciones de pago de PSIPs autorizados.

## PSBI — Prestadores de Servicios Basados en Informacion

Son los que **leen tu data financiera para ofrecerte un servicio**.

Ejemplos posibles (cuando el SFA prenda):
- Una app que compara tus cuentas y te dice donde estas perdiendo plata
- Un sistema de scoring crediticio que mira tu historial bancario
- Un PFM (Personal Finance Manager) como Mint o Fintonic
- Un servicio de contabilidad que se conecta directo a tus cuentas
- Una verificacion de ingresos para arriendos o creditos

Equivalente internacional: en Reino Unido se llaman **AISP** (Account Information Service Providers). En Brasil se llaman **Transmissor / Receptor de Dados**.

**Requisito:** estar inscrito en el Registro de Prestadores de Servicios Financieros (RPSF) de la CMF.

## PSIP — Prestadores de Servicios de Iniciacion de Pagos

Son los que **inician pagos en tu nombre, desde tu cuenta bancaria, hacia un tercero**.

Ejemplos:
- Pagar una compra online via transferencia bancaria sin pasar por Transbank
- Cobrar suscripciones recurrentes via debito directo automatizado
- Pagar boletas y facturas con un click

Hoy en Chile esto lo hacen **Fintoc, Khipu, Etpay, Floid** con un workaround tecnico (scraping autorizado por el usuario). Con el SFA, lo van a hacer via APIs oficiales FAPI 2.0.

Equivalente internacional: en Reino Unido se llaman **PISP** (Payment Initiation Service Providers). En Brasil se llaman **Iniciador de Pagamento**.

**Requisito:** ser PSF inscrito en la CMF con capital y garantia proporcionales al volumen transado.

## PSC — Prestadores de Servicios de Certificacion

Son los que **emiten los certificados digitales que firman las comunicaciones** entre IPIs y PSBIs/PSIPs.

Equivalente: en Europa se llaman QTSP (Qualified Trust Service Providers). En Brasil, ICP-Brasil.

En Chile la CMF aun no define quien sera el equivalente. Es uno de los temas pendientes del Anexo Tecnico N°3.

## Como interactuan

Caso 1: leer info (PSBI)

```
Tu (Pedro)        ----> PSBI "MiFinanzas.cl"
                        "Quiero ver mis cuentas"
PSBI MiFinanzas.cl ----> Directorio CMF
                        "Autenticame con Pedro"
Directorio CMF    ----> IPI BancoEstado
                        "Pedro quiere darte acceso"
IPI BancoEstado   ----> Tu (Pedro)
                        "Confirmas?"
Tu (Pedro)        ----> IPI BancoEstado: "Si"
IPI BancoEstado   ----> PSBI MiFinanzas.cl
                        "Aca esta la data"
```

Caso 2: iniciar pago (PSIP)

```
Tu (Pedro)        ----> Comercio "Cafeteria del Barrio"
                        "Quiero pagar $5.000 con transferencia"
Comercio          ----> PSIP "PagoFacil.cl"
                        "Cobra $5.000 a Pedro"
PSIP PagoFacil.cl ----> IPCP Banco de Chile
                        "Pedro quiere transferir $5.000 a Cafeteria"
IPCP Banco Chile  ----> Tu (Pedro)
                        "Confirmas?"
Tu (Pedro)        ----> IPCP Banco Chile: "Si"
IPCP Banco Chile  ----> Comercio: "Plata transferida"
```

## Diferencia clave con el sistema actual

**Hoy** (sin SFA):
- Para que una fintech vea tu data, tiene que pedirte tu **usuario y clave del banco** y hacer scraping (modelo Fintoc, Khipu).
- El banco no esta obligado a aceptarlo. Puede bloquear, cambiar el sitio, agregar captcha (caso BancoEstado vs Khipu/Etpay/Floid en 2024).
- Cero estandar tecnico. Cada fintech reinventa el wheel.

**Con el SFA** (post jul-2027):
- Las APIs son **obligatorias y estandarizadas**.
- El banco NO puede bloquear si tu consentiste.
- La autenticacion la hace el banco (mas seguro, no compartes clave).
- La fintech tiene que estar inscrita y certificada (mas confianza).

## Glosario rapido

- **FAPI 2.0**: Financial-grade API Security Profile. Estandar tecnico que mandata la CMF.
- **OAuth 2.0**: protocolo de autorizacion. Es como las apps te piden "iniciar sesion con Google".
- **mTLS**: Mutual TLS. Doble verificacion (cliente Y servidor presentan certificados).
- **NCG 514**: Norma de Caracter General N°514 de la CMF que regula el SFA.
- **CMF**: Comision para el Mercado Financiero, el regulador.
- **Consentimiento dinamico**: tu autorizacion tiene fecha de inicio y fin, y debe renovarse cada cierto tiempo (max 12 meses).
- **RPSF**: Registro de Prestadores de Servicios Financieros.

Para mas detalle ver [glosario completo](./recursos/glosario.md).
