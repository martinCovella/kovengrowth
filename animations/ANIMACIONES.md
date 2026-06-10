# Animaciones — Koven Growth

## Estado actual

| Card | Imagen EN | Imagen ES | EN listo | ES listo | Tipo |
|------|-----------|-----------|----------|----------|------|
| Performance (+31%/+24%) | en1.png | es1.png | ⬜ | ⬜ | Count-up overlay |
| Dashboard chart (+18%) | en2.png | es2.png | ✅ | ⬜ | SVG line draw + count-up |

## Estructura de archivos

```
animations/
  en/
    card-en1.html   ← +31% / +24% / 4-8 weeks  (count-up overlay)
    card-en2.html   ← chart line + +18% + Revenue + AOV  (SVG anim)
  es/
    card-es1.html   ← igual que en1 pero con es1.png + texto ES
    card-es2.html   ← igual que en2 pero con es2.png + texto ES
  ANIMACIONES.md    ← este archivo
```

## Cómo adaptar EN → ES

Para cada card, los únicos cambios necesarios son:
1. `src="../../images/en/enX.png"` → `src="../../images/es/esX.png"`
2. Textos de labels en el HTML (si aplica)
3. Los valores numéricos y la lógica JS son idénticos

## Configs de animación

### card-en2 / card-es2 (Dashboard chart)
- Duración línea: 2500ms
- Hold final: 1500ms
- KPI (Conversion Rate): 0% → +18%, sincronizado con progreso del chart
- Revenue: €0 → €11,298 | delay 300ms | duración 2000ms
- AOV: €0.00 → €72.45 | delay 500ms | duración 1800ms
- Easing: easeOutCubic

### card-en1 / card-es1 (Performance card)
- Loop: 3500ms total (~1.6s pausa post-animación)
- +31%: delay 150ms | duración 1500ms
- +24%: delay 420ms | duración 1500ms
- 4 weeks: delay 700ms | duración 900ms
- 8 weeks: delay 750ms | duración 1100ms
- Easing: easeOutCubic
