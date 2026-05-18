# FAPI 2.0, OAuth 2.0, mTLS — el stack que mandata la CMF

## Resumen rápido

El SFA Chile usa exactamente el mismo stack técnico que Open Finance Brasil:

- **OpenAPI 3.1** para schemas
- **OAuth 2.0 + OpenID Connect** para autenticación/autorización
- **FAPI 2.0** (Financial-grade API Security Profile)
- **mTLS sobre TLS 1.3** para todas las comunicaciones
- **JWS** para firma de payloads sensibles

Si sabes FAPI Brasil, sabes FAPI Chile. No hay rueda nueva.

## Qué es FAPI

FAPI = Financial-grade API. Es un perfil de seguridad sobre OAuth 2.0 + OpenID Connect, mantenido por la OpenID Foundation. Diseñado específicamente para APIs financieras donde el riesgo de fraude es alto.

FAPI tiene dos versiones:

- **FAPI 1.0 Advanced**: lo que usa UK Open Banking. Maduro pero más viejo
- **FAPI 2.0**: lo que usa Brasil, lo que va a usar Chile. Más simple, más seguro, mejor performance

Chile saltó a FAPI 2.0 directo, evitando la deuda técnica de UK.

## Qué exige FAPI 2.0

1. **mTLS obligatorio**: el cliente (PSIP/PSBI) presenta certificado X.509 al servidor (banco), y viceversa. Ambos se autentican
2. **PKCE obligatorio**: previene ataques de intercepción de código de autorización
3. **PAR (Pushed Authorization Requests)**: el cliente envía la request de autorización vía POST antes del redirect, no en query params
4. **JAR (JWT Secured Authorization Request)**: la request va firmada
5. **DPoP o mTLS-bound tokens**: el access token está atado al certificado que lo pidió. Si te lo roban, no sirve
6. **No implicit flow, no hybrid flow**: solo authorization code flow + PKCE
7. **Sender-constrained refresh tokens**: idem

## Por qué importa para tú

Si vas a construir un PSBI o PSIP en Chile:

- No puedes usar el OAuth básico de cualquier framework. Necesitas authorization server certificado FAPI 2.0
- Tu cliente necesita librería FAPI 2.0 (no la genérica de OAuth)
- Tu infra necesita gestión de certificados X.509 (CA aprobada por CMF)
- Necesitas pasar la conformance suite oficial de OpenID Foundation antes de operar productivo

## Stack open source recomendado

### Authorization Server

**Keycloak 26.1+**
- Open source, Apache 2.0
- FAPI 2.0 + DPoP certificado oficialmente
- Ya usado en producción por bancos en Brasil
- Repo: github.com/keycloak/keycloak

Setup mínimo:
```
docker run -p 8080:8080 \
  -e KEYCLOAK_ADMIN=admin \
  -e KEYCLOAK_ADMIN_PASSWORD=admin \
  quay.io/keycloak/keycloak:26.1 start-dev
```

Configurar realm con perfil `fapi-2-security-profile` + `fapi-2-dpop-security-profile`.

**Authlete** (SaaS, no OSS)
- Comercial. Lo usa Nubank en Brasil
- Útil si no quieres mantener Keycloak

### Client (TPP side)

- **`openbankingbrasil-tpp-reference`** (Java) en github.com/OpenBanking-Brasil
- Si trabajás Node/TypeScript: librerías genéricas OAuth 2.0 + extender para FAPI 2.0 (PKCE, PAR, mTLS)
- Si trabajás Python: `authlib` cubre OAuth 2.0; sumar mTLS via `requests` + cert; PKCE nativo

### Conformance testing

**OpenID Foundation conformance-suite**
- gitlab.com/openid/conformance-suite
- Java/Maven, Apache 2.0
- Tests para FAPI 1, FAPI 2.0, FAPI-CIBA, Message Signing
- Es la suite oficial de certificación

## Gestión de certificados

En Brasil usan ICP-Brasil. En Chile la CMF aún no definió equivalente — está en el Anexo Técnico N°3 pendiente.

Mientras no haya definición:
- Para sandbox puedes usar certificados self-signed o de Let's Encrypt
- Para producción habrá que esperar la definición CMF (esperable Q3-2026)

## Diferencias prácticas vs Open Banking UK

| Aspecto | UK (FAPI 1.0 Advanced) | Chile (FAPI 2.0) |
|---|---|---|
| Flow | Hybrid flow + JARM | Authorization code + PKCE |
| Token binding | mTLS o private_key_jwt | mTLS o DPoP |
| Authorization request | Direct redirect | PAR obligatorio |
| Complejidad | Alta | Media |
| Performance | Más latente | Mejor |

## Recursos para aprender

### Specs oficiales
- FAPI 2.0 Security Profile: openid.net/specs/fapi-2_0-security-02.html
- FAPI 2.0 Message Signing: openid.net/specs/fapi-2_0-message-signing-03.html
- OAuth 2.1 (resumen de best practices): datatracker.ietf.org/doc/html/draft-ietf-oauth-v2-1

### Tutoriales aplicados
- Keycloak FAPI: keycloak.org/2022/01/fapi
- Open Finance Brasil dev docs: openfinancebrasil.atlassian.net
- Apigee openbanking-br walkthrough: github.com/apigee/openbanking-br

### Mock APIs para practicar
- Open Banking Brasil mock: github.com/OpenBanking-Brasil/mock-api
- AWS reference architecture: github.com/aws-samples/openbanking-brazilian-reference-architecture
- Open Banking UK sandbox: openbanking.org.uk

## Próximos pasos

Si quieres empezar:

1. Monta Keycloak FAPI 2.0 en docker local
2. Bajate el mock-api de Open Banking Brasil
3. Hacé un flujo end-to-end: client → AS → API → response
4. Corré la conformance suite contra tu setup
5. Documentá todo y publicalo

Cuando salga el Anexo Técnico N°3 de Chile (esperado Q3-2026) vas a estar 6 meses adelante.
