# LeafTags
Um sistema completo de prefixos para servidores de Minecraft, com várias opções configuráveis. 


## Comandos

|Comando         |Descrição                      |Permissão                    |
|----------------|-------------------------------|-----------------------------|
|/tag ou tags |Mostrará a lista de tags do jogador.|Nenhuma    |
|/tag config|Veja a configuração atual de tags.|`OP ou permissão total`|

## Download

Você pode encontrar o plugin pronto para baixar [**aqui**](https://github.com/leafcodebr/LeafTags/releases).

## Configuração

O plugin conta com vários arquivos de configuração, que pode ser facilmente manipulado por qualquer pessoa, além de você
poder moldar ao seu modo.

## Placeholders

### PlaceholderAPI

- "%leaftags_player_tag_name%" ~ retornará o nome da tag atual do jogador.
- "%leaftags_player_tag_color" ~ retornará a cor da tag atual do jogador.
- "%leaftags_player_tag_prefix%" ~ retornará o prefix da tag atual do jogador.
- "%leaftags_player_tag_suffix%" ~ retornará o suffix da tag atual do jogador.
- "%leaftags_player_tag_preset%" ~ retornará o preset da tag atual do jogador.

OBS: Caso queira pegar informações da **tag máxima** do jogador, altere "`_tag_`" para "`_maxtag_`"

### Plugins de Chat
- "{leaf_tag}" ~ preset da tag atual do jogador.
- "{leaf_maxtag}" ~ preset da tag máxima do jogador.

## Dependências

- [LeafCore]https://github.com/leafcodebr/LeafCore/releases) - necessário para o funcionamento de todos os plugins Leaf.

## API - para desenvolvedores.
**Exemplo de uso:**
```java
/* Retornará a API para uso */
LeafTagsAPI api = LeafTags.getAPI();

/* Retornará a tag máxima do jogador */
Tag maxTag = api.getMaxTag(player);
/* Retornará a tag atual do jogador */
Tag currentTag = api.getCurrentTag(player);
/* Criará uma nova tag */
Tag newTag = api.createTag(
        "example", //id
        "example", //name
        "&d", //color
        "tag.example", //permission
        "&d[Example] ", //prefix
        " &d[BEAUTIFUL]", //suffix
        "&dExample", //preset
        26, //position
        Arrays.asList("aliases-here", "aliases-here")); //aliases
/* Registrando a nova tag */
api.registerTag(newTag);
/* Aplicando a nova tag ao jogador */
api.applyTag(player, newTag);

/* E por fim... Removendo a tag do servidor */
api.unregisterTag("example");
```

