# LeafTags
Um sistema completo de prefixos para servidores de Minecraft, com várias opções configuráveis. 

## Versões
Este plugin funciona em todas as versões a partir da 1.8.

## Tutorial
Este plugin possui um [tutorial oficial](https://youtu.be/Ip27Vz8Jq9Y?t=171) em nosso canal no YouTube!

## Comandos

|Comando         |Descrição                      |Permissão                    |
|----------------|-------------------------------|-----------------------------|
|/tag ou tags |Mostrará a lista de tags do jogador.|Nenhuma    |
|/tag config|Veja a configuração atual de tags.|`OP ou permissão total`|

## Download

Você pode encontrar o plugin pronto para baixar [**aqui**](https://github.com/leafcodebr/LeafTags/releases).

## Configuração

O plugin possui as configurações bem fáceis e completas. Você pode ver as configurações padrões [clicando aqui](https://github.com/leafcodebr/LeafTags/tree/main/configs).

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

## Compatibilidade
- PermissionsEx/LuckPerms - alterar prefix/tag quando ter o cargo alterado.

## Informações
- É possível utilizar o banco de dados MySQL para armazenar a ultima tag utilizada do jogador. [Recomendado para BungeeCord]
- Caso o jogador perca a permissão da tag atual, terá-lo alterado para a maior tag(tag máxima) que ele possui. 
- Cores Hex (ou RGB) - a partir da 1.16 é permitido utilizar cores #hex **(&#00000)**

## Dependências

- [LeafCore](https://github.com/leafcodebr/LeafCore/releases) - necessário para o funcionamento de todos os plugins Leaf.
- [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) - para aplicar placeholders e registra-los. (OPCIONAL)

## API - para desenvolvedores.
**Exemplo de uso:**
```java
/* Retornará a API para uso */
LeafTagsAPI api = LeafTags.getAPI();

/* Fará que quando o jogador entrar, não terá o prefix setado */
api.setDisableAutoTag(true);

/* Fará que o comando /tag não funcione (RECOMENDADO DESATIVA-LO PELA CONFIG.YML). */
api.setDisableCommand(true);

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

