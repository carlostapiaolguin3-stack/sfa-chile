# SFA Chile

Lo que necesitas saber sobre el Sistema de Finanzas Abiertas (SFA) de Chile, ordenado, actualizado y sin humo. Para PYMES, creators, devs y cualquiera que quiera entender qué cambia y cuándo.

Mantenido por [Carlos Tapia](https://carlostapia.cl), profesional con experiencia en banca y tecnología en Chile. **Proyecto personal e independiente.** No representa a ningún empleador, banco ni fintech. MIT. Actualizado al 2026-05-18.

---

## Qué es el SFA, en una línea

La ley chilena obliga a bancos, AFPs, aseguradoras y emisores de tarjetas a compartir tu data financiera con terceros autorizados, si tú autorizas. Empieza en julio 2027.

Eso es todo. El resto es detalle.

---

## Por qué este repo

El contenido público sobre SFA en Chile hoy es de tres tipos: técnico-jurídico (Carey, Garrigues), vendor-side (Shinkansen, Fintoc) o institucional (CMF, FinteChile). Nadie habla en castellano de oficina para el dueño del café, la ferretería, el estudio de diseño o el SaaS chico que va a tener que tomar decisiones cuando esto prenda.

Este repo es eso. Trabajo en banca y tecnología pero mantengo este proyecto en tiempo personal, sin vincularlo a ningún empleador, banco ni fintech. Sin agenda comercial: no vendo infraestructura, ni consultoría SFA, ni servicios financieros. Si encuentras algo útil, contribuye con un PR.

---

## Empieza por acá

Si tienes una PYME o cobras con tarjeta:
- [Cuánto te puede ahorrar el SFA (calculadora)](./para-pymes/calculadora.md)
- [Checklist de preparación](./para-pymes/checklist.md)
- [FAQ](./para-pymes/faq.md)
- [Plantilla de email a tu banco](./para-pymes/plantillas/email-banco-roadmap-sfa.md)

Si quieres entender cómo funciona:
- [Calendario CMF](./roadmap.md)
- [Actores: PSIP, PSBI, IPI, IPCP en simple](./actores.md)
- [Comparativa con Brasil, UK, México, Perú/Colombia](./comparativas/)

Si eres dev o quieres construir algo:
- [Stack técnico: FAPI 2.0, OAuth2, mTLS](./stack-tecnico/fapi-2.0.md)
- [Herramientas open source](./stack-tecnico/herramientas-oss.md)
- [Recursos Open Finance Brasil (el modelo que copia Chile)](./stack-tecnico/recursos-brasil.md)

Para monitorear:
- [Dashboard de implementación + estado real](./DASHBOARD.md)
- [Sandbox voluntario CMF: cómo entrar](./convocatorias/sandbox-cmf.md)

---

## Estado al 2026-05-18

- Ley Fintec 21.521 publicada el 4-ene-2023
- NCG 514 dictada el 3-jul-2024
- Vigencia plena postergada a julio 2027 (era julio 2026)
- Sandbox voluntario CMF abierto desde mayo 2026 con ~10 entidades (BancoEstado, Mercado Pago confirmadas)
- 42 entidades inscritas en el RPSF, 37 autorizadas, 249 en backlog
- Cero APIs SFA productivas en bancos chilenos

Detalle completo en el [dashboard](./DASHBOARD.md).

---

## Cómo contribuir

PRs bienvenidos. Si encuentras un error de data, quieres agregar un caso, sumar una herramienta o aportar una guía, abre un Pull Request. Ver [CONTRIBUTING.md](./CONTRIBUTING.md).

---

## Disclaimer

Esto es contenido educativo. No es asesoría legal ni financiera. Para decisiones de cumplimiento, consulta con tu abogado o con la CMF en leyfintec@cmfchile.cl.
