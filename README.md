# ðŸ¥¶ Congelou

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

[![Congelou](guia/assets/banner.jpg)](https://inematds.github.io/congelou/guia/)

Curta de **38s com efeito time freeze**, feito 100% pela **assinatura Kling AI** via CLI oficial `kling`:
coloco um frango para assar, tomo um cafÃ©, abro o forno, o frango sai **vivo**, eu me assusto e **tudo congela**.
Quando o tempo volta, vem o estrago.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo + como repetir com outro assunto): **https://inematds.github.io/congelou/guia/**

ðŸŽ¬ VÃ­deos: [v1 original](guia/assets/congelou.mp4) Â· [v2 freeze total + paradas](guia/assets/congelou_v2.mp4) Â· [v3 gato no microondas (4K, 2 congelamentos)](guia/assets/microondas.mp4)

## Como funciona

```
foto do rosto â†’ keyframe k1 â†’ clipe A â†’ Ãºltimo quadro â†’ clipe B â†’ clipe C (freeze) â†’ clipe D â†’ ffmpeg â†’ final
```

| Arquivo | FunÃ§Ã£o |
|---|---|
| `keyframe.sh` | still inicial com o seu rosto (Nano Banana Pro dentro da Kling) |
| `clip.sh` | um clipe Kling 3.0 (1080p, Ã¡udio nativo, plano Ãºnico) + baixa + Ãºltimo quadro |
| `fetch.sh` | baixa o resultado, mede o Ã¡udio, gera contact sheet e `keyframes/X_last.png` |
| `montar.sh` | junta os clipes, 1920Ã—1080/24fps, loudnorm -14 LUFS |
| `prompts/` | `k1.txt`, `A.txt`â€¦`D.txt` e o template `freeze_effect_template_en.md` |
| `LOG.md`, `job_ids.txt` | registro de cada geraÃ§Ã£o e custo |

```bash
kling login
./keyframe.sh ref/nei.jpg prompts/k1.txt
./clip.sh A keyframes/k1.png 5
./clip.sh B keyframes/A_last.png 8
./clip.sh C keyframes/B_last.png 15
./clip.sh D keyframes/C_last.png 10
./montar.sh A B C D
```

Custo medido (plano Pro): 12 crÃ©ditos/s no Kling 3.0 1080p com Ã¡udio. O filme todo saiu por ~476 crÃ©ditos.

---
[INEMA.CLUB](https://inema.club)

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>