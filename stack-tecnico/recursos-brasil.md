# Recursos Open Finance Brasil

Brasil es el modelo que copia Chile. Stack técnico idéntico (FAPI 2.0 + OAuth 2.0 + mTLS). Si entrenás con material brasileño hoy, llegas al SFA Chile (jul-2027) con 12 meses de ventaja.

## Por qué Brasil sirve como base

- **Stack técnico idéntico**: FAPI 2.0, mTLS, OAuth 2.0, OpenID Connect
- **Arquitectura similar**: Directorio central + Authorization Servers en cada banco + TPPs registrados
- **Documentación abundante**: 4 años productivo, comunidad activa, material en portugués (entendible para hispanohablante) y traducciones al inglés
- **Lo que NO copia Chile**: ISO 20022 obligatorio (Chile usa JSON sobre OpenAPI 3.1), gobernanza descentralizada (Chile centraliza más en CMF)

## Repos imprescindibles

### Open Finance Brasil GitHub Org

- URL: github.com/OpenBanking-Brasil
- 52 repos oficiales mantenidos por la Estrutura Inicial de Governança
- Licencia: Apache 2.0
- Lo que vas a usar:
  - `specs-seguranca`: spec de seguridad FAPI 2.0 + mTLS aplicada
  - `areadesenvolvedor`: developer portal source
  - `mock-api`: APIs mock para testear sin banco real
  - `OpenAPI`: schemas OpenAPI 3.1 de todas las APIs
  - `OpenBanking-Brasil/openid-fapi-conformance-suite-tests`: tests específicos Brasil

### Apigee openbanking-br

- URL: github.com/apigee/openbanking-br
- Implementación de referencia en Google Cloud Apigee
- Útil si vas a hostear en GCP
- Shared flows + API proxies + ejemplos de policies

### AWS Open Banking Brazilian Reference Architecture

- URL: github.com/aws-samples/openbanking-brazilian-reference-architecture
- Mock APIs corriendo en AWS con mTLS + Lambda Authorizer
- Si vas a hostear en AWS (sa-east-1 idealmente para Chile)

### AWS Open Banking Brazilian Auth Samples

- URL: github.com/aws-samples/openbanking-brazilian-auth-samples
- API Gateway + Lambda Authorizer + FAPI OIDC provider
- Demo de cómo armar el authorization layer

### magnobiet/open-banking-brazil

- URL: github.com/magnobiet/open-banking-brazil
- Awesome list curada (specs, libs, papers, casos, eventos)
- ~500 stars
- Modelo exacto del awesome-sfa-chile que estamos armando acá

## Documentación oficial

- Portal Open Finance Brasil: openfinancebrasil.org.br
- Documentación técnica: openfinancebrasil.atlassian.net
- Developer area: openfinance.org.br/areadesenvolvedor
- Swagger APIs públicas: openbanking-brasil.github.io/openapi/swagger-apis/

## Cronología (para context)

- **may 2020**: Resolución BCN/BCB regulando Open Banking
- **feb 2021**: Fase 1 (datos públicos)
- **ago 2021**: Fase 2 (datos cliente con consentimiento)
- **oct 2021 a sept 2022**: Fase 3 (iniciación de pagos)
- **sept 2022**: Fase 4 (FX, inversiones, seguros)
- **sept 2022**: implementación "completa"

Total: 28 meses de norma a productivo. Chile tiene 36 meses programados.

## Estado actual Brasil (2026)

- 15M usuarios activos (8% de adultos bancarizados)
- 100M+ consentimientos otorgados acumulados
- 13 bancos top obligados, +800 instituciones participando
- PIX como rail dominante de pagos instantáneos (complementa Open Finance)
- Adopción más lenta de lo esperado en lectura de datos. Iniciación de pagos sí pegó

## Lecciones Brasil para Chile

1. **Baja adopción consumer**: la gente no entiende para qué compartir su data. Educación demand-side falló
2. **Performance interbancaria mala**: SLAs no se cumplían, BCB tuvo que sancionar
3. **Consent management caro**: gestión de ciclo de vida de consentimientos consume engineering
4. **PSIPs y PSBIs operan a pérdida**: el costo de cumplimiento FAPI + auditorías come márgenes. Solo Belvo/Pluggy/Klavi sobreviven con escala
5. **Educación financiera no se invirtió**: nadie hizo el equivalente de un "PIX Educa" institucional masivo

Todo eso se va a repetir en Chile salvo que actuemos distinto. Por eso el repo demand-side.

## Comunidad y eventos

- **Comunidade Open Banking Brasil** en GitHub: github.com/open-banking-brasil
- **Bruno Diniz (Spiralem)**: brunodiniz.com — el divulgador top, LinkedIn Top Voice
- **Conferencias**: CIAB FEBRABAN, OpenFinance Brasil annual
- **Podcasts**: Open Banking Talk (en portugués)

## Cómo aprovechar esto en Chile

1. Levantá el mock-api Brasil en docker en tu VPS
2. Configura Keycloak FAPI 2.0 como AS de prueba
3. Cliente Java o Node consumiendo el mock
4. Pasá la conformance suite OpenID
5. Documentá el flow completo en español chileno
6. Cuando salga el Anexo Técnico N°3 Chile (Q3-2026), reemplazás schemas y vas listo

## Pulls Welcome

Si conoces más recursos brasileños útiles (no listados arriba) que sirvan para CL, abre PR.
