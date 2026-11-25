# ê°Å¸Â¥Â¶ Congelou

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

[![Congelou](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

Curta de **38s com efeito time freeze**, feito 100% pela **assinatura Kling AI** via CLI oficial `kling`:
coloco um frango para assar, tomo um cafêÂ©, abro o forno, o frango sai **vivo**, eu me assusto e **tudo congela**.
Quando o tempo volta, vem o estrago.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo + como repetir com outro assunto): **https://linnoff88-dev.github.io/

ê°Å¸Å½Â¬ VêÂ­deos: [v1 original](guia/assets/congelou.mp4) êÂ· [v2 freeze total + paradas](guia/assets/congelou_v2.mp4) êÂ· [v3 gato no microondas (4K, 2 congelamentos)](guia/assets/microondas.mp4)

## Como funciona

```
foto do rosto ê¢â â keyframe k1 ê¢â â clipe A ê¢â â êÂºltimo quadro ê¢â â clipe B ê¢â â clipe C (freeze) ê¢â â clipe D ê¢â â ffmpeg ê¢â â final
```

| Arquivo | FunêÂ§êÂ£o |
|---|---|
| `keyframe.sh` | still inicial com o seu rosto (Nano Banana Pro dentro da Kling) |
| `clip.sh` | um clipe Kling 3.0 (1080p, êÂ¡udio nativo, plano êÂºnico) + baixa + êÂºltimo quadro |
| `fetch.sh` | baixa o resultado, mede o êÂ¡udio, gera contact sheet e `keyframes/X_last.png` |
| `montar.sh` | junta os clipes, 1920êâ1080/24fps, loudnorm -14 LUFS |
| `prompts/` | `k1.txt`, `A.txt`ê¢â¬Â¦`D.txt` e o template `freeze_effect_template_en.md` |
| `LOG.md`, `job_ids.txt` | registro de cada geraêÂ§êÂ£o e custo |

```bash
kling login
./keyframe.sh ref/nei.jpg prompts/k1.txt
./clip.sh A keyframes/k1.png 5
./clip.sh B keyframes/A_last.png 8
./clip.sh C keyframes/B_last.png 15
./clip.sh D keyframes/C_last.png 10
./montar.sh A B C D
```

Custo medido (plano Pro): 12 crêÂ©ditos/s no Kling 3.0 1080p com êÂ¡udio. O filme todo saiu por ~476 crêÂ©ditos.

---
[ARCKHê AI](https://ARCKHê AI)

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>