# 💜 LeafTags
* Versões testadas: **1.7, 1.8**.


## Compatibilidade
Compatibilidade disponível: **A partir de 1_7_R4**

Caso queira ter todas as funcionalidades do plugin disponíveis, utilize um Spigot a partir de 1.8 por utilizarem 1_8_R3 ou superior. (Versões acima de 1_8_R3 podem não funcionar corretamente por enquanto)

## Dependencia
⚠️ Caso você utilize o Spigot 1.7.10, será necessário ter o plugin **[NametagEdit](https://www.spigotmc.org/resources/nametagedit.3836/)** em seu servidor.

## Configuração
* Mensagens, tags e opções configuraveis.
* ⚠️ Compatibilidade com PlaceholderAPI em breve disponível.

## Permissões
As Tags por padrão tem suas permissões definidas com **leaftags.tag.nome**, porém é fácilmente modificável! 

## Comandos
### Comando /tag:
* /tag reload - Recarregará a configuração e as tags.
* /tag (tag) - Setará a tag selecionada.
* /tags ou /tag - Mostrará suas tags disponíveis

## Configuração

<details>
  <summary>config.yml</summary>

```yml
  Mensagens:
  # Replaces disponíveis: #
  # %tag% - Nome da Tag: "LEAF" #
  # %tag_color% - Cor da Tag: "&a" #
  # %tag_prefix% - Prefixo da Tag: "&5&lLEAF" #
  # %tag_permission%" - Permissão da Tag: "leaftags.tag.leaf" #
  comando_preset:
    - "&a&lTAGS &fUtilize: /tag (tag)!"
    - "&a&lTAGS &fSuas tags disponíveis: %tags%&f."
    - "op:&a&lTAGS &f/tag reload &a- &fRecarregar as Tags."
  sem_permissao:
    - "&c&lERRO &fVocê não tem permissão para usar a tag %tag_prefix%&f!"
    - "&fÉ necessário você ter a permissão &c&l%tag_permission%&f!"
  tag_definida:
    - "&a&lFEITO &fSua tag foi setada para %tag_color%%tag%&f!"
Opcoes:
  # Titulo - Quando alterar a Tag, aparecerá um titulo na tela.
  Titulo:
    # enable - True para ativar, False para desativar.
    enable: true
    titulo: "%tag_color%%tag%"
    subtitulo: "&fTag alterada com sucesso!"
  # Som - Quando alterar a Tag, tocará um som. (Deixe vazio para desativar)
  Som: "WOOD_CLICK"
Tags:
  Admin:
    nome: "ADMIN"
    cor: "&4"
    ladder: 1
    prefix: "&4&lADMIN &4"
    suffix: "&7[STAFF]"
    permissao: "leaftags.tag.admin"
    variaveis:
      - "dono"
  Vip:
    nome: "VIP"
    cor: "&a"
    ladder: 2
    prefix: "&a&lVIP &a"
    suffix: "&7[VIPS]"
    permissao: "leaftags.tag.vip"
    variaveis: []
  Membro:
    # Nome - Nome da Tag (Exemplo: Leaf)
    nome: "Membro"
    # Cor - Cor da Tag (Exemplo: &a)
    cor: "&7"
    # Ladder - A posição na Tablist.
    ladder: 30
    # Prefix - Visual da Tag quando aplicada (Exemplo: &a&lLEAF&a Player)
    prefix: "&7"
    # Suffix - Em breve compatibilidade com placeholderAPI
    suffix: "&a[LEAF]"
    # Permissão - Permissão necessária para usar a tag (Caso esteja vazio, não precisará de permissão)
    permissao: ""
    # Variáveis - Formas de usar a tag (Exemplo: /tag [variavel])
    variaveis:
      - "player"
      - "jogador"
```
