# 💜 LeafTags
* Versões disponíveis: **1.8**.
* Versões testadas: **1.8.8, 1.15.2, 1.16.5, 1.18.2**.

## Dependencia
É necessário o plugin [LeafCore](https://github.com/leafcodebr/LeafCore/releases/tag/Downloads) para o funcionamento.

## Configuração
* Mensagens, tags e opções configuraveis.
* Compatibilidade com PlaceholderAPI **disponível**!

## Comandos
|Comando         |Descrição                      |Permissão                    |
|----------------|-------------------------------|-----------------------------|
|/tag ou /tags        |Exibe as tags do jogador |`Nenhuma`           |
|/tag (tag)    |Selecione uma Tag disponível |`Nenhuma`       |

## Placeholders
|Placeholder        |Descrição                      |Resultado/Exemplo                    |
|----------------|-------------------------------|-----------------------------|
|%leaftags_player_tag_name%        |Nome da tag atual do jogador.|`Admin`           |
|%leaftags_player_tag_colorx%    |Cor da tag atual do jogador. |`&c`       |
|%leaftags_player_tag_prefix%    |Prefixo da tag atual do jogador. |`&c[Admin] &c`       |
|%leaftags_player_tag_suffix%    |Suffix da tag atual do jogador. |`&6[PVP]`       |
|%leaftags_player_tag_preset%    |Preset da tag atual do jogador. |`&cAdmin`       |

A tag máxima é utilizada por exemplo para mostrar o cargo do jogador.

Para pegar a informação da tag máxima do jogador, troque o `_tag_` das placeholders para `_maxtag_`. **(SIMPLES E FÁCIL)**

## Configuração
Os arquivos de tags ficarão na pasta 'tags' dentro da pasta LeafTags!
```yml
MySQL:
  Host: 'localhost'
  Usuario: 'root'
  Senha: ''
  Porta: 3306
  Database: 'leaf_tags'
  Tabela: 'leaf_tags'
# File-tags: Arquivo que será usado para as tags.
File-tags: "default.yml"
# Log-tag: Irá anunciar no console caso alguém mude de tag.
Log-tag: true
Mensagens:
  # Replaces disponíveis: #
  # %tag% - Nome da Tag: "LEAF" #
  # %tags% - Lista de tags (comando_preset)
  # %tag_color% - Cor da Tag: "&a" #
  # %tag_prefix% - Prefixo da Tag: "&5&lLEAFTAGS" #
  # %tag_permission%" - Permissão da Tag: "leaftags.tag.leaf" #
  comando_preset:
    - "%leaf_prefix% &fSuas tags: %tags%"
  sem_permissao:
    - "%leaf_prefix% &fVocê não tem permissão para usar a tag %tag_prefix%&f!"
  tag_definida:
    - "%leaf_prefix% &fSua tag foi setada para %tag_color%%tag%&f!"
  tag_nao_encontrada:
    - "%leaf_prefix% &fTag '%tag%' não foi encontrada!"
  tag_ja_definida:
    - "%leaf_prefix% &fVocê já está usando esta tag!"
  "mundo_bloqueado":
    - "&cVocê não pode alterar sua tag neste mundo!"
Tag_lista:
  # Visual: Visual da tag na lista do /tags.
  Visual: "%tag_color%%tag%"
  # Virgula: Como será a virgula separando as tags na lista do /tags.
  Virgula: "&f,"
Opcoes:
  # Titulo: Quando alterar a Tag, aparecerá um titulo na tela.
  Titulo:
    # Enable: 'true' para ativar e 'false' para desativar.
    enable: true
    titulo: "%tag_color%%tag%"
    subtitulo: "&fTag alterada!"
  # Som: Ao utilizar o comando, tocará um som (Deixe vazio para desativar)
  Som: "CHICKEN_EGG_POP"
  # Som_tag: Ao alterar a tag, tocará um som (Deixe vazio para desativar)
  Som_tag: "LEVEL_UP"
  # Tag_click Caso esteja 'true', as tags poderão ser selecionadas por click.
  Tag_click: true
# Block-Mundos: Caso o jogador esteja em algum destes mundos, ele não poderá alterar a tag.
Block-Mundos:
  - "partida01"
```

