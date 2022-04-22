# 💜 LeafTags
* Versões testadas: **1.7, 1.8**.


## Compatibilidade
Compatibilidade disponível: **A partir de 1_7_R4**

Caso queira ter todas as funcionalidades do plugin disponíveis, utilize um Spigot a partir de 1.8 por utilizarem 1_8_R3 ou superior. (Versões acima de 1_8_R3 podem não funcionar corretamente por enquanto)

## Dependencia
⚠️ Caso você utilize o Spigot 1.7.10, será necessário ter o plugin **[NametagEdit](https://www.spigotmc.org/resources/nametagedit.3836/)** em seu servidor.

## Configuração
* Mensagens, tags e opções configuraveis.
* Compatibilidade com PlaceholderAPI **disponível**!

## Permissões
As Tags por padrão tem suas permissões definidas com **leaftags.tag.nome**, porém é fácilmente modificável! 

## Comandos
### Comando /tag:
* /tag reload - Recarregará a configuração.
* /tag (tag) - Setará a tag selecionada.
* /tags ou /tag - Mostrará suas tags disponíveis.

## Configuração
```yml
# File-tags - Arquivo que será usado para as tags.
File-tags: "default.yml"
Mensagens:
  # Replaces disponíveis: #
  # %tag% - Nome da Tag: "LEAF" #
  # %tag_color% - Cor da Tag: "&a" #
  # %tag_prefix% - Prefixo da Tag: "&5&lLEAF" #
  # %tag_permission%" - Permissão da Tag: "leaftags.tag.leaf" #
  comando_preset:
    - "&a&lTAGS &fUtilize: /tag (tag)!"
    - "&a&lTAGS &fSuas tags disponíveis: %tags%&f."
    - "op:&a&lTAGS &f/tag reload &a- &fRecarregar config."
  sem_permissao:
    - "&c&lERRO &fVocê não tem permissão para usar a tag %tag_prefix%&f!"
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
  Som: "CHICKEN_EGG_POP"
```
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966900700011450448/unknown.png)
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966901569310310400/unknown.png)
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966902307629436968/unknown.png)
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966901846721568828/unknown.png)
