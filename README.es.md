# ðŸ¥¶ Congelou

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

[![Congelou](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

Corto de **38s con efecto time freeze**, hecho 100% con la **suscripciÃ³n Kling AI** del autor mediante el CLI oficial `kling`:
pongo un pollo a asar, tomo un cafÃ©, abro el horno, el pollo sale **vivo**, me asusto y **todo se congela**.
Cuando el tiempo vuelve, llega el desastre.

## ðŸ“– GuÃ­a de uso

GuÃ­a completa (landing + paso a paso + cÃ³mo repetir con otra historia): **https://linnoff88-dev.github.io/

ðŸŽ¬ Videos: [v1 original](guia/assets/congelou.mp4) Â· [v2 congelamiento total + paradas](guia/assets/congelou_v2.mp4) Â· [v3 gato en el microondas (4K, 2 congelamientos)](guia/assets/microondas.mp4)

## CÃ³mo funciona

```
foto del rostro â†’ keyframe k1 â†’ clip A â†’ Ãºltimo cuadro â†’ clip B â†’ clip C (freeze) â†’ clip D â†’ ffmpeg â†’ final
```

| Archivo | FunciÃ³n |
|---|---|
| `keyframe.sh` | still inicial con tu rostro (Nano Banana Pro dentro de Kling) |
| `clip.sh` | un clip Kling 3.0 (1080p, audio nativo, plano Ãºnico) + descarga + Ãºltimo cuadro |
| `fetch.sh` | descarga el resultado, mide el audio, genera contact sheet y `keyframes/X_last.png` |
| `montar.sh` | une los clips, 1920Ã—1080/24fps, loudnorm -14 LUFS |
| `prompts/` | `k1.txt`, `A.txt`â€¦`D.txt` y la plantilla `freeze_effect_template_en.md` |
| `LOG.md`, `job_ids.txt` | registro de cada generaciÃ³n y su costo |

```bash
kling login
./keyframe.sh ref/nei.jpg prompts/k1.txt
./clip.sh A keyframes/k1.png 5
./clip.sh B keyframes/A_last.png 8
./clip.sh C keyframes/B_last.png 15
./clip.sh D keyframes/C_last.png 10
./montar.sh A B C D
```

Costo medido (plan Pro): 12 crÃ©ditos/s en Kling 3.0 a 1080p con audio. La pelÃ­cula completa costÃ³ ~476 crÃ©ditos.

---
[ARCKHÉ AI](https://ARCKHÉ AI)
