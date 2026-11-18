# Pendências — Antes do Amanhecer (`Jogo-Roguelite-AntesDoAmanhecer`)

Este documento rastreia o estado técnico implementado (Sprints 1 a 12 + Polish), as melhorias opcionais e as entregas finais de mídia/publicação.

---

## 1. Concluído e Verificado (Engenharia & Qualidade)
- [x] **Core Roguelite & Grade Espacial (`SpatialHashGrid`):** Movimentação, colisão otimizada para hordas densas, gemas de XP e nível do jogador.
- [x] **Sistemas de Combate & Evoluções:** 5 armas iniciais, 5 evoluções definitivas (baús), 3 fusões secretas, passivas e chefes (*Mapinguari*, *Cuca*, *Hora Morta*).
- [x] **Áudio Procedural & Juice:** Sintetizador PCM 16-bit integrado (`AudioManagerNode`) sem arquivos externos, tremor de câmera, *hit-stop*, partículas de poeira e números de dano em pool (`DamageNumberPool`).
- [x] **Metagame, Loja & Estágios:** 3 cenários, bestiário/grimório desbloqueável, loja *Candeeiro*, bênçãos de marcos e persistência JSON (`SaveSystem`).
- [x] **Acessibilidade & Opções:** Controle de intensidade de tremor, *hit-stop*, números de dano e modo de fotossensibilidade (`SettingsManagerNode`).
- [x] **Correção de Autoloads & Compilação Limpa:** Resolvidos conflitos de shadowing (`SettingsManagerNode` / `AudioManagerNode`) e sintaxe de `theme_override` em runtime nos scripts de UI/FX.
- [x] **Bot de Autojogo & Suíte de 14 Testes (`58/58` passando):** Balanceamento determinístico validado com semente fixa (`CA-01` a `CA-16`).
- [x] **Pipeline de CI/CD (`.github/workflows/godot-ci.yml`):** Execução automática das 14 suítes de testes em Godot 4.7.2 headless e verificação de cold-boot.

---

## 2. Melhorias Futuras Opcionais (Backlog Técnico)
- [ ] **Integração de Shaders Customizados:** Adicionar shader de vinheta dinâmica na transição da *Hora Morta* e contorno iluminado nos chefes.
- [ ] **Suporte a Conquistas Steam/itch.io:** Conectar os marcos já rastreados no `SaveSystem` à API de plataformas de distribuição.

---

## 3. Dependências Externas (Mídia, Arte Final & Publicação)
- [ ] **Spritesheets e Ilustrações Finais:** Substituir a arte vetorial/geométrica provisória por pixel art ou sprites ilustrados definitivos do folclore brasileiro.
- [ ] **Trilha Sonora e Masterização:** Composição e importação da trilha musical adaptativa para cada fase da noite.
- [ ] **Publicação de Builds (`export_presets.cfg`):** Exportação final assinada para Windows, Linux e Web (HTML5) e upload na página do itch.io / Steam.
