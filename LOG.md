# LOG â€” congelou (frango vivo + time freeze)

Via: **assinatura Kling AI do usuÃ¡rio** (CLI `kling`, conta SVIP/Pro). Nada de Magnific/RunComfy.
Ref de rosto: `ref/nei.jpg` (cÃ³pia de ~/projetos/explicavideos/guia/assets/nei.jpg).

- 2026-09-25 14:5x k1 still (gemini-3-pro-image, 2k 16:9) OK â€” 20 crÃ©ditos (7973.8 â†’ 7953.8)
- 2026-09-25 clip A submetido (kling-video-v3_0, 5s, 1080p, audio, single shot)
- 14:55 clip A OK (60 crÃ©d, 5.04s, audio aac) â†’ A_last.png; clip B submetido (8s)
- 14:59 clip B OK (96 crÃ©d, 8.04s) â†’ B_last.png; clip C submetido (15s, freeze, single shot)
- 15:04 clip C OK (180 crÃ©d, 15.04s, freeze funcionou: frango suspenso + Ã³rbita) â†’ C_last.png; clip D submetido (10s, estrago)
- 15:10 clip D OK (120 crÃ©d, 10.04s; cozinha deriva um pouco pro genÃ©rico) â†’ montagem
- 15:12 FINAL congelou_final.mp4 38.0s 1920x1080, -14.8 LUFS. Total ~476 crÃ©ditos Kling (7973.8 â†’ 7497.8). Capa refeita com quadro real do freeze (Codex gerou folha congelada, off-topic).
- 15:15 publicado: repo linnoff88-dev/congelou (e6d507a), guia PT/EN/ES 200; portal 6a4feae, ARCKHÉbuscas f6d2bb4, ARCKHÉpro-mono 10af3aa
- 16:09 V2 pedida: galinha sai na hora, freeze total (inclusive ele, sÃ³ cÃ¢mera), volta em cÃ¢mera muito lenta â†’ natural. Reusa A,B. C2 submetido (12s)
- 16:10 V3 pedida: prato no microondas, sai gato vivo assustado, eu viro/derrubo tudo. Estilo v2 (freeze total + rampa slow-mo).
- 16:11 k3 OK (20 crÃ©d); M1 submetido (8s)
- 16:13 C2 OK (144 crÃ©d, 12s; freeze total + Ã³rbita dramÃ¡tica; fundo clareia no fim) â†’ D2 submetido (10s)
- 16:14 M1 OK (96 crÃ©d, 8s) â†’ M2 submetido (12s, gato + freeze)
- 16:15 D2 OK (120 crÃ©d, 10s; cozinha deriva p/ genÃ©rica) â†’ montagem v2
- 16:18 M2 OK (144 crÃ©d) mas Ã³rbita termina de cabeÃ§a p/ baixo e prato desliza no freeze â†’ corta em 8.0s, M3 parte de M2_cut.png; v2 montada 41.2s
- 16:22 M3 OK (120 crÃ©d, 10s) â†’ montagem v3
- 16:24 v3 microondas.mp4 32.2s -14.5 LUFS publicada no guia. CrÃ©ditos restantes 6853.8
- 16:28 v2 ATUALIZADA a pedido: cÃ¢mera lenta interpolada â†’ 4 paradas (anda 0.3s / trava 0.8â†’0.4s, som some na trava). 37.6s. Sem custo Kling. Backup slow-mo em build/.
- 17:02 V3 REFEITA (usuÃ¡rio nÃ£o gostou): gato sai ANTES de pÃ´r o prato, derruba o prato; congelamentos em 4K nÃ­tidos, vÃ¡rios momentos; sem interpolaÃ§Ã£o
- 17:04 k4 OK (20 crÃ©d). N1 submetido 4K 4s (medir custo 4K)
- 17:08 N1 OK 4K (3856x2148) 4s = 140 crÃ©d â†’ 4K custa 35 crÃ©d/s (~3x 1080p)
- 17:10 N1_nitido OK (20 crÃ©d) â†’ N2 freeze 1 submetido 4K 8s
- 17:15 N2 (260 crÃ©d) FALHOU: prato continua caindo no freeze e cÃ¢mera quase parada. Troca: freeze = still 4K nÃ­tido + movimento de cÃ¢mera no ffmpeg; Ã¡udio do N2 reaproveitado
- 17:18 F1 (freeze 1) OK: still 4K 5504px nÃ­tido + push-in ffmpeg 8s, som do N2 (custo 20). N3 submetido 4K 4s a partir de F1
- 17:24 N3 OK 4K (140 crÃ©d) mas giro borrado ~2.5s â†’ usar sÃ³ N3[0:2.2]. F2 (impacto do prato, still 4K gerado) OK 20 crÃ©d. N5 submetido 4K 8s a partir de F2
- 20:04 N5 OK 4K 8s (280 crÃ©d). Montagem v3 nova 4K: N1 F1 N3c F2 N5
- 20:05 v3 NOVA publicada: microondas.mp4 4K 29s -14.7 LUFS (N1 F1 N3c F2 N5). Custo v3 refeita â‰ˆ 880 crÃ©d (N2 260 perdido). Saldo 6023.8
