# ê°Å¸Â¥Â¶ Congelou

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

[![Congelou](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

Corto de **38s con efecto time freeze**, hecho 100% con la **suscripciêÂ³n Kling AI** del autor mediante el CLI oficial `kling`:
pongo un pollo a asar, tomo un cafêÂ©, abro el horno, el pollo sale **vivo**, me asusto y **todo se congela**.
Cuando el tiempo vuelve, llega el desastre.

## ê°Å¸ââ GuêÂ­a de uso

GuêÂ­a completa (landing + paso a paso + cêÂ³mo repetir con otra historia): **https://linnoff88-dev.github.io/

ê°Å¸Å½Â¬ Videos: [v1 original](guia/assets/congelou.mp4) êÂ· [v2 congelamiento total + paradas](guia/assets/congelou_v2.mp4) êÂ· [v3 gato en el microondas (4K, 2 congelamientos)](guia/assets/microondas.mp4)

## CêÂ³mo funciona

```
foto del rostro ê¢â â keyframe k1 ê¢â â clip A ê¢â â êÂºltimo cuadro ê¢â â clip B ê¢â â clip C (freeze) ê¢â â clip D ê¢â â ffmpeg ê¢â â final
```

| Archivo | FunciêÂ³n |
|---|---|
| `keyframe.sh` | still inicial con tu rostro (Nano Banana Pro dentro de Kling) |
| `clip.sh` | un clip Kling 3.0 (1080p, audio nativo, plano êÂºnico) + descarga + êÂºltimo cuadro |
| `fetch.sh` | descarga el resultado, mide el audio, genera contact sheet y `keyframes/X_last.png` |
| `montar.sh` | une los clips, 1920êâ1080/24fps, loudnorm -14 LUFS |
| `prompts/` | `k1.txt`, `A.txt`ê¢â¬Â¦`D.txt` y la plantilla `freeze_effect_template_en.md` |
| `LOG.md`, `job_ids.txt` | registro de cada generaciêÂ³n y su costo |

```bash
kling login
./keyframe.sh ref/nei.jpg prompts/k1.txt
./clip.sh A keyframes/k1.png 5
./clip.sh B keyframes/A_last.png 8
./clip.sh C keyframes/B_last.png 15
./clip.sh D keyframes/C_last.png 10
./montar.sh A B C D
```

Costo medido (plan Pro): 12 crêÂ©ditos/s en Kling 3.0 a 1080p con audio. La pelêÂ­cula completa costêÂ³ ~476 crêÂ©ditos.

---
[ARCKHê AI](https://ARCKHê AI)
