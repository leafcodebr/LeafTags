# 💜 LeafTags
* Versões testadas: **1.7, 1.8**.

## Dependencia
É necessário o plugin [LeafCore](https://github.com/leafcodebr/LeafCore/releases/tag/Downloads) para o funcionamento.

⚠️ Caso você utilize o Spigot 1.7.10, será necessário ter o plugin **[NametagEdit](https://www.spigotmc.org/resources/nametagedit.3836/)** em seu servidor.

## Configuração
* Mensagens, tags e opções configuraveis.
* Compatibilidade com PlaceholderAPI **disponível**!

## Permissões
As Tags por padrão terão suas permissões definidas como **leaftags.tag.nome**, porém é fácilmente modificável! 

## Comandos
### Comando /tag:
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
  # Som: Ao utilizar o comando, tocará um som (Deixe vazio para desativar)
  Som: "CHICKEN_EGG_POP"
  # Som_tag: Ao alterar a tag, tocará um som (Deixe vazio para desativar)
  Som_tag: "LEVEL_UP"
```
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372484451336222/javaw_zREkkr5Ox4.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372484963016774/javaw_rIFJtg3AAM.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372485390848020/javaw_rbQzfuiFCf.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372485604737074/javaw_ahlf6jzvwS.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372485818662942/javaw_Ua9bHyklgf.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372486007414794/javaw_9ANh07N2VA.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372486632361984/javaw_bPrklne5HK.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372484757491722/javaw_Ssv4kY7d8B.png)
![configurado](https://cdn.discordapp.com/attachments/967197530351865886/969372486280048700/javaw_SzqYBRg2dp.png)
