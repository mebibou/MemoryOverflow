# MemoryOverflow - Cards & Editions

MemoryOverflow game is based on cards. Each one is unique and can be used in many different ways according to the strategy of the player.
Cards are grouped by editions which represent different themes.

 - [Editions](#editions)
 - [Create a new card](#create)
 - [Improve/Fix existing card](#fix)

## <a name="editions"></a> Editions

Here are the list of all editions:
* [Fundamentals edition](https://github.com/CodeCorico/MemoryOverflow/blob/master/cards/fundamentals/)

## <a name="create"></a> Create a new card

To be used by the [generator](https://github.com/CodeCorico/MemoryOverflow/blob/master/generator/), each card has a generic configuration.
It's possible to create cards in differents programming languages and translations.

### The folder structure

A card must be located inside an edition. Each card is composed of files inside a folder name.

Here is the folder configuration:
```
/cards/[edition name]/[card name]/
    -> README.md
    -> [card name].md
    -> [card name].en_EN.po
    -> [card name].[translation].po
```

A card *must have* these files. It's possible to add all of the translation you want but you need to have JavaScript format and english translation by default.

#### README.md file

This file describe the card and its spirit.
Its include:
* Its name
* Its type
* Its languages supported
* Its translations supported
* A link to its configuration file
* Its changelog

#### [card name].md file

This file is a Markdown format. It describe in details the card divided in sections by title.

Here is the format:
```markdown
# title

The full title of the card

# status

Status can only be: "working", "deprecated" or "played"

# edition

The name of the card edition

# type

Type can only be: "variable", "code", or "event"

# author

The full name of the author followed by its Twitter account

# code:javascript

This block is only used for a card with "variable" or "code" type.

Write the specific code of your card and many other informations.

You can add all of the formatting tags like {code}
Use &{} to encapsulate your translated texts

# code:php

You can add all of the codes syntax you want. PHP, Java, C++, etc

# description

This block is used only for a card with "event" type.

Write the card action description here.

You can add all of the formatting tags like {code}{/code}
Use &{} to encapsulate your translated texts

```

All translated text need to be encapsulated by &{my text}.

#### [card name].[translation].po files

Translations files are used to translate encapsulated texts inside card configuration.

A translation file use the international ISO language code in a [Gettext format](http://www.gnu.org/software/gettext) (.po):
```
[card name].en_EN.po -> English format
[card name].fr_FR.card -> French format
...
```

## <a name="fix"></a> Improve/Fix existing card

If a card needs to be fixed, you can:
* Contact the original author of the card so that he corrects himself.
* Add an [issue](https://github.com/CodeCorico/MemoryOverflow/issues).
* Send a new PR linked to your issue (see the [Contribution guidelines](https://github.com/CodeCorico/MemoryOverflow/blob/master/CONTRIBUTING.md))