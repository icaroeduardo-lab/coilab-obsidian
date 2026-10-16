# Cofre do COILAB (Obsidian)

Base de conhecimento do COILAB (Laboratório de Inovação e IA da DPRJ): cultura, treinamentos, cursos, normativos, inventário de IA, projetos e eventos. Este repositório é o próprio cofre do Obsidian; a nota de entrada é `00 Início/Início.md`.

## Como usar no desktop

1. Clone o repositório e abra a pasta como cofre no Obsidian ("Abrir pasta como cofre"):

   ```bash
   git clone https://github.com/icaroeduardo-lab/coilab-obsidian.git
   ```

   Se você já tem uma pasta de cofre, clone dentro dela ou aponte o Obsidian para a pasta clonada.

2. Antes de editar, traga as mudanças mais recentes:

   ```bash
   git pull
   ```

3. Depois de editar, envie suas alterações:

   ```bash
   git add .
   git commit -m "docs: descreva a mudança"
   git push
   ```

Para sincronizar sem usar o terminal, você pode instalar o plugin da comunidade **Obsidian Git**, que faz pull e push pelo próprio Obsidian.

## Estrutura

- `00 Início` – página inicial e mapa do cofre
- `01 Cultura` – valores e práticas do laboratório
- `02 Treinamentos` – trilhas internas (ex.: Letramento em IA)
- `03 Cursos` – anotações de cursos externos
- `04 Pessoas` – fichas de pessoas
- `05 Normativos` – resoluções e políticas
- `06 Inventário de IA` – sistemas de IA em uso
- `07 Projetos` – projetos do laboratório
- `08 Eventos` – eventos e palestras
- `99 Modelos` – modelos usados pelo plugin Templates

As configurações pessoais do Obsidian (layout da área de trabalho, cache) ficam fora do Git via `.gitignore`; só as configurações compartilhadas, como `.obsidian/templates.json`, são versionadas.
