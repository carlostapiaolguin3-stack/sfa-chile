# Glosario SFA Chile

Términos en orden alfabético.

## A

**AISP (Account Information Service Provider)**: equivalente UK del PSBI chileno. Lee tu data financiera con tu consentimiento.

**Anexo Técnico**: documento de la NCG 514 que define los estándares técnicos (FAPI 2.0, OAuth 2.0, mTLS, OpenAPI 3.1). Anexo N°3 en consulta pública.

**API (Application Programming Interface)**: forma estandarizada en que dos sistemas se hablan. El SFA exige APIs FAPI 2.0 obligatorias entre bancos y terceros.

## B

**BCCh (Banco Central de Chile)**: emisor de moneda, regulador del sistema de pagos. Participa como observador en el Foro SFA de la CMF.

**Bre-B**: sistema de pagos instantáneos de Colombia, equivalente al PIX brasileño. Lanzado oct-2025.

## C

**Capital mínimo**: requerimiento patrimonial para inscribirse en el RPSF. Para PSIP/PSBI va entre UF 5.000 y UF 30.000 según volumen transado.

**CCA / CCBV (Cámara de Compensación de Bajo Valor)**: infraestructura que liquida transferencias TEF entre bancos chilenos.

**CMF (Comisión para el Mercado Financiero)**: regulador de bancos, valores, seguros, fondos y servicios financieros en Chile. Operador del SFA.

**CoDi (Cobro Digital)**: sistema de pagos instantáneos de México, equivalente fallido del PIX brasileño.

**Consentimiento dinámico**: autorización del cliente que tiene fecha de inicio y fin, ámbito específico, y se puede revocar en cualquier momento. Máximo 12 meses sin renovar.

## D

**Débito directo**: mecanismo por el cual un comercio o servicio cobra automáticamente de tu cuenta bancaria con tu autorización previa. PSIPs lo implementan vía SFA.

**Directorio CMF (Directorio de Participantes)**: registro central operado por la CMF donde se inscriben IPIs, PSBIs y PSIPs autorizados. Maneja los certificados digitales.

**DPoP (Demonstrating Proof of Possession)**: técnica que ata un access token al cliente que lo pidió. Si te roban el token, no sirve sin la clave privada.

## F

**FAPI 2.0 (Financial-grade API Security Profile)**: perfil de seguridad mandatado por la CMF para APIs SFA. Sobre OAuth 2.0 + OpenID Connect. Define mTLS, PKCE, PAR, JAR.

**Fintech**: empresa que combina tecnología y servicios financieros. En Chile, las que ofrecen servicios regulados deben inscribirse en el RPSF.

## I

**IPI (Institución Proveedora de Información)**: banco, AFP, aseguradora, cooperativa o emisor de tarjeta que guarda tu data financiera y debe publicarla vía APIs SFA. Grupo 1: bancos + emisores tarjetas. Grupo 2: cooperativas + AFP + aseguradoras.

**IPCP (Institución Proveedora de Cuentas de Pago)**: IPI que además administra cuentas desde las que se pueden iniciar pagos. En la práctica, bancos y emisores de tarjetas prepago.

**ISO 20022**: estándar internacional de mensajería financiera. Brasil lo usa para Open Finance. Chile NO lo usa (usa JSON sobre OpenAPI 3.1).

## J

**JWS (JSON Web Signature)**: estándar para firmar payloads JSON. FAPI 2.0 lo exige para autorizar requests sensibles.

## L

**LBTR (Liquidación Bruta en Tiempo Real)**: sistema del BCCh para liquidación de transferencias de alto valor en tiempo real. No es retail. Ley 21.641 (2024) permite entrada de no-bancos.

**Ley Fintec (Ley 21.521)**: ley chilena que regula servicios financieros tecnológicos. Publicada 4-ene-2023.

## M

**mTLS (Mutual TLS)**: variante de TLS donde cliente Y servidor presentan certificados. FAPI 2.0 lo exige.

## N

**NCG (Norma de Carácter General)**: instrumento regulatorio de la CMF. Las relevantes para SFA son NCG 502, 503, 504, 514 y 559.

## O

**OAuth 2.0**: protocolo estándar de autorización. Base sobre la que se construye FAPI.

**Open Banking**: término genérico para apertura de APIs bancarias. UK fue el primero (2018).

**Open Finance**: evolución de Open Banking que incluye AFP, seguros, fondos. Brasil lo llama así. Chile lo llama SFA.

**OpenAPI 3.1**: estándar de especificación de APIs REST. La CMF lo mandata para describir contratos SFA.

## P

**PAR (Pushed Authorization Request)**: técnica de FAPI 2.0 donde el cliente envía la request de autorización vía POST antes del redirect, no en query params.

**PFM (Personal Finance Management)**: software que te ayuda a entender tus finanzas. Mint, Fintonic, Maybe son ejemplos. Vacío de mercado en Chile post salida de Fintonic 2024.

**PIX**: sistema de pagos instantáneos del Banco Central de Brasil. Lanzado nov-2020. 90% de adultos lo usan.

**PKCE (Proof Key for Code Exchange)**: técnica que previene intercepción de código de autorización. FAPI 2.0 lo exige.

**PSC (Prestador de Servicios de Certificación)**: emite certificados digitales que firman comunicaciones SFA. En Brasil ICP-Brasil. En Chile pendiente de definir.

**PSBI (Prestador de Servicios Basados en Información)**: tercero autorizado que lee tu data financiera de los IPIs vía APIs SFA. Equivalente al AISP de UK.

**PSIP (Prestador de Servicios de Iniciación de Pagos)**: tercero autorizado que inicia pagos en tu nombre desde tus cuentas. Equivalente al PISP de UK.

**PSP (Prestador de Servicios de Pago)**: término genérico para acquirers, emisores y wallets de pago.

## R

**RPSF (Registro de Prestadores de Servicios Financieros)**: registro de la CMF donde se inscriben los prestadores regulados por la Ley Fintec.

**RTGS (Real-Time Gross Settlement)**: liquidación bruta en tiempo real, transacción por transacción. PIX brasileño y Bre-B colombiano usan RTGS.

## S

**Sandbox**: ambiente de prueba donde fintech pueden probar productos sin estar plenamente regulados. CMF abrió uno voluntario para SFA en mayo 2026.

**SFA (Sistema de Finanzas Abiertas)**: la implementación chilena de Open Finance, definida por la NCG 514 sobre la Ley Fintec.

**Shinkansen**: empresa chilena fundada por Leo Soto. Primera Cámara de Pagos Fintech aprobada por CMF (ene-2024). Infra B2B de pagos. Leo Soto lidera el Consejo de Finanzas Abiertas de FinteChile.

**SUDEBAN**: regulador venezolano del sistema bancario. Distinto del rol CMF.

## T

**TEF (Transferencia Electrónica de Fondos)**: transferencia bancaria estándar en Chile. Hoy NO es instantánea (puede tardar minutos a horas).

**Toku**: fintech chilena de cobranza recurrente B2B. USD 1.800M procesados/año, valuación USD 175M. Caso de éxito invisible.

**TPP (Third Party Provider)**: término UK/EU para PSBI/PSIP. El tercero que consume APIs Open Banking.

## V

**Variable Recurring Payments (VRP)**: feature de Open Banking UK que permite cobros recurrentes con consentimiento dinámico. El feature más interesante a copiar en Chile.

## W

**Webpay**: pasarela de pago de Transbank para e-commerce. Líder en Chile con 74% del mercado e-commerce.

## Y

**Yape**: wallet peruana del BCP. 15M+ usuarios. Compite/interopera con Plin.

## Otros términos

**ACR**: Authentication Context Class Reference. Usado en OAuth/OIDC para indicar nivel de autenticación requerido.

**ASPSP (Account Servicing Payment Service Provider)**: término UK para el banco que guarda la cuenta. Equivalente al IPI/IPCP chileno.

**CIBA (Client-Initiated Backchannel Authentication)**: flow OAuth donde la autenticación se hace por separado del canal del cliente. Útil para call centers y dispositivos sin browser.

**JARM (JWT-secured Authorization Response Mode)**: forma de devolver la respuesta de autorización firmada. UK lo usa. Chile no la mandata.

**SCA (Strong Customer Authentication)**: requerimiento europeo PSD2 de autenticación multifactor. FAPI 2.0 lo asume implícitamente.

---

Faltan términos? Abre un PR.
