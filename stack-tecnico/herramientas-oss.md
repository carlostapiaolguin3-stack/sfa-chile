# Herramientas Open Source para el ecosistema SFA Chile

Curado de la comunidad. PRs bienvenidos.

## Authorization Servers FAPI 2.0

### Keycloak

- Repo: github.com/keycloak/keycloak
- Stars: ~25k
- Licencia: Apache 2.0
- Stack: Java
- Estado: certificado FAPI 2.0 + DPoP desde 26.1.0
- Encaje SFA: el stack default open source para PSBI/PSIP. Ya certificado para Open Finance Brasil

### Authlete (mencion comercial relevante)

- Sitio: authlete.com
- Modelo: SaaS comercial
- Estado: certificado FAPI Brasil
- Usado por: Nubank en Brasil
- Encaje SFA: alternativa SaaS si no quieres mantener Keycloak

### Tyk FAPI Accelerator

- Repo: open-core
- Sitio: tyk.io
- Alternativa open-core para gateway

### WSO2 Open Banking

- Stack enterprise con accelerators FAPI 1.0 Advanced
- Licencia comercial cara

## Reference implementations Open Banking / Finance

### Open Finance Brasil GitHub (oficial)

- Repo: github.com/OpenBanking-Brasil
- Licencia: Apache 2.0
- Contiene: 52 repos con specs OpenAPI, conformance suite, mocks, certificate management
- Encaje SFA: la base para fork/españolizacion. El stack tecnico chileno es FAPI 2.0 idem Brasil

### Apigee openbanking-br

- Repo: github.com/apigee/openbanking-br
- Stars: ~80
- Implementacion Google Cloud Apigee de las specs Open Banking BR (shared flows, API proxies)

### AWS openbanking-brazilian-reference-architecture

- Repo: github.com/aws-samples/openbanking-brazilian-reference-architecture
- Stars: ~150
- Licencia: MIT-0
- Mock APIs Open Banking corriendo en AWS con mTLS

### AWS openbanking-brazilian-auth-samples

- Repo: github.com/aws-samples/openbanking-brazilian-auth-samples
- Stars: ~60
- API Gateway + Lambda Authorizer + FAPI OIDC provider

### magnobiet/open-banking-brazil (awesome-list)

- Repo: github.com/magnobiet/open-banking-brazil
- Stars: ~500
- Licencia: MIT
- Awesome list curada (specs, libs, casos, papers)
- Encaje SFA: **modelo exacto a replicar como awesome-sfa-chile**

### Open Banking UK

- Repo: github.com/OpenBankingUK
- 22 repos oficiales (specs, model bank, conformance)
- Sandbox UK (v3.1.11 / v4.0 FAPI 1.0) sirve como benchmark vs SFA

### Mastercard open-banking-eu-postman-collections

- Repo: github.com/Mastercard/open-banking-eu-postman-collections
- Postman collections para AIIA (PSD2 EU)

### postman-toolboxes/open-banking-uk-public

- Repo: github.com/postman-toolboxes/open-banking-uk-public
- Postman collection oficial publica UK
- Forkeable como postman-sfa-chile cuando se libere Anexo N°3

### adorsys/open-banking-gateway

- Repo: github.com/adorsys/open-banking-gateway
- Stars: ~390
- Gateway RESTful que abstrae multiples APIs bancarias (PSD2, XS2A, HBCI)
- Empaquetable como "TPP starter kit chileno"

## Conformance / Testing

### OpenID Foundation conformance-suite

- Repo: gitlab.com/openid/conformance-suite (mirror github.com/openid-certification/conformance-suite)
- Licencia: Apache 2.0
- Tests FAPI 1.0, FAPI 2.0 Security Profile + Message Signing, FAPI-CIBA
- Stack: Java/Maven
- El estandar de certificacion oficial

## PFM Consumer (Personal Finance Management)

Espacio vacio en Chile post salida Fintonic 2024.

### Maybe Finance

- Repo: github.com/maybe-finance/maybe
- Stars: ~45k
- Licencia: AGPLv3
- Stack: Rails + Postgres
- Estado: recientemente open-sourceado tras levantar USD 1M
- Encaje: forkear, agregar conector SFA cuando exista, traducir UX a CL

### Firefly III

- Repo: github.com/firefly-iii/firefly-iii
- Stars: ~17k
- Licencia: AGPL-3.0
- Stack: PHP/Laravel
- Importadores CSV (la banca CL exporta CSV)
- Comunidad i18n acepta PRs es-CL

### Actual Budget

- Repo: github.com/actualbudget/actual
- Stars: ~17k
- Licencia: MIT
- YNAB-style envelope budgeting, sync local-first
- Ideal demo para creators sin cloud

### GnuCash

- Repo: github.com/Gnucash/gnucash
- Stars: ~6k
- Licencia: GPL
- Desktop, contabilidad doble entrada
- Audiencia: contadores PYME CL

### Ghostfolio

- Repo: github.com/ghostfolio/ghostfolio
- Stars: ~6.5k
- Licencia: AGPLv3
- Portfolio tracker (acciones, cripto, commodities)
- Para creators trading-savvy

## Reconciliation / Ledger

### Blnk

- Repo: github.com/blnkfinance/blnk
- Stars: ~2k
- Licencia: Apache 2.0
- Stack: Go
- Ledger + reconciliation engine open source
- Producto base para "ledger as a service" PYME

### OCA/account-reconcile

- Repo: github.com/OCA/account-reconcile
- Licencia: AGPL
- Modulos Odoo conciliacion bancaria

### akaunting

- Repo: github.com/akaunting/akaunting
- Stars: ~9k
- Licencia: GPL
- Contabilidad PYME en PHP, modulo Banking/Reconciliations

## Fraud detection / AML

### Marble

- Repo: github.com/checkmarble/marble
- Stars: ~600
- Licencia: Elastic 2.0
- Decision engine real-time fraud + AML
- SOC 2 Type II
- Alternativa OSS a Comply Advantage. Lo mas interesante para ecosistema SFA-CL

### Jube

- Repo: github.com/jube-home/aml-fraud-transaction-monitoring
- Licencia: AGPLv3
- AML + fraud ML real-time

### OpenSanctions

- Repo: github.com/opensanctions/opensanctions
- Licencia: MIT
- Listas KYC/sanctions consolidadas globales
- Imprescindible para cualquier PSBI/PSIP

## Consent management

### WSO2 Open Banking Accelerator

- Repo: github.com/wso2/financial-services-accelerator
- Licencia: Apache 2.0
- Modulo consent management enterprise

### ConsentStack/cmp

- Repo: github.com/ConsentStack/cmp
- Licencia: MIT
- Plataforma consent dev-focused, ligera. Forkeable

### OpenBankProject/OBP-API

- Repo: github.com/OpenBankProject/OBP-API
- Stars: ~750
- API platform que cubre consents UK/Berlin/OBP

## Dashboards / BI

### Metabase

- Repo: github.com/metabase/metabase
- Stars: ~40k
- Licencia: AGPL
- Dashboards plug-and-play sobre Postgres
- Tutorial "Metabase + Firefly III para PYME chilena"

### Apache Superset

- Repo: github.com/apache/superset
- Stars: ~62k
- Licencia: Apache 2.0
- Mas enterprise

### Lightdash, Evidence, Rill

- Varias alternativas modernas BI open source

## Como contribuir a esta seccion

Si conoces una herramienta OSS relevante para el ecosistema Open Finance / SFA Chile, abre un PR agregandola con:

- Repo URL
- Stars aproximadas
- Licencia
- Stack tecnico
- Caso de uso especifico para Chile
