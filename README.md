# 💜 LeafTags
* Versões testadas: **1.7, 1.8**.


## Compatibilidade
Compatibilidade disponível: **1_7_R4, 1_8_R3 +**

Caso queira ter todas as funcionalidades do plugin disponíveis, utilize um Spigot a partir de 1.8 por utilizarem 1_8_R3 ou superior. (Versões acima de 1_8_R3 podem não funcionar corretamente por enquanto)

## Dependencia
É necessário o plugin [LeafCore](https://github.com/leafcodebr/LeafCore/releases/tag/Downloads) para o funcionamento.

⚠️ Caso você utilize o Spigot 1.7.10, será necessário ter o plugin **[NametagEdit](https://www.spigotmc.org/resources/nametagedit.3836/)** em seu servidor.

## Configuração
* Mensagens, tags e opções configuraveis.
* Compatibilidade com PlaceholderAPI **disponível**!

## Permissões
As Tags por padrão terão suas permissões definidas com **leaftags.tag.nome**, porém é fácilmente modificável! 

## Comandos
### Comando /tag:
* /tag reload - Recarregará a configuração.
* /tag (tag) - Setará a tag selecionada.
* /tags ou /tag - Mostrará suas tags disponíveis.

## Configuração
Os arquivos de tags ficam na pasta 'tags' dentro da pasta LeafTags!
```yml
# File-tags: Arquivo que será usado para as tags.
File-tags: "default.yml"
Mensagens:
  # Replaces disponíveis: #
  # %tag% - Nome da Tag: "LEAF" #
  # %tag_color% - Cor da Tag: "&a" #
  # %tag_prefix% - Prefixo da Tag: "&5&lLEAFTAGS" #
  # %tag_permission%" - Permissão da Tag: "leaftags.tag.leaf" #
  comando_preset:
    - "%leaf_prefix% &fSuas tags: &f%tags%."
  sem_permissao:
    - "%leaf_prefix% &fVocê não tem permissão para usar a tag %tag_prefix%&f!"
  tag_definida:
    - "%leaf_prefix% &fSua tag foi setada para %tag_color%%tag%&f!"
  tag_nao_encontrada:
    - "%leaf_prefix% &fTag '%tag%' não foi encontrada!"
  tag_ja_definida:
    - "%leaf_prefix% &fVocê já está usando esta tag!"
Opcoes:
  # Titulo: Quando alterar a Tag, aparecerá um titulo na tela.
  Titulo:
    # Enable: 'true' para ativar e 'false' para desativar.
    enable: true
    titulo: "%tag_color%%tag%"
    subtitulo: "&fTag alterada!"
  # Som: Ao utilizar o comando, usará um som (Deixe vazio para desativar)
  Som: "CHICKEN_EGG_POP"
```
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966900700011450448/unknown.png)
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966901569310310400/unknown.png)
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966902307629436968/unknown.png)
![configurado](https://cdn.discordapp.com/attachments/957444296733253653/966901846721568828/unknown.png)
