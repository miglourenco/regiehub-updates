# RegieHub — atualizações de firmware

Firmware publicado para os equipamentos da RegieHub (8&Pico Soluções Audiovisuais). A RegieHub lê o
`manifest.json` deste repositório, avisa quando há firmware novo e atualiza os equipamentos a partir do
hub.

| Equipamento | Placa | Como se atualiza |
| --- | --- | --- |
| `tally` | ESP32-C3 Super Mini | a RegieHub envia o `.bin` para o portal de cada tally |
| `beltpack` | Seeed XIAO ESP32-S3 | a RegieHub envia o `.bin` com a assinatura; o beltpack só aceita imagens assinadas e mais novas do que a que tem |

- Os binários são compilados sem redes nem passwords de origem. Uma atualização mantém as redes guardadas
  em cada equipamento.
- Cada versão é uma release (`tally-0.3.6`, `beltpack-0.3.2`, …) com o `.bin`.
- `manifest.json`: a última versão de cada equipamento, com o URL, o tamanho, o SHA-256, as notas e, no
  beltpack, a assinatura (ECDSA P-256).

Publicado com `firmware/tools/publish_firmware.py` (repositório privado da RegieHub).
