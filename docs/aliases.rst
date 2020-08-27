========
Aliases
========

For ease of use, the user can also call on models by their aliases.

lite
-----------------

**class** mitnewsclassify.lite(txt)

Calls ``mitnewsclassify.ensemble.gettags``.

**Parameters**
    * txt (``string``) - The article text

**Returns**
    * tags (``List[str]``) - The predicted tags

medium
-----------------

*class* mitnewsclassify.medium(txt)

Calls ``mitnewsclassify.trisemble.gettags``.

**Parameters**
    * txt (``string``) - The article text

**Returns**
    * tags (``List[str]``) - The predicted tags

badass
-----------------

*class* mitnewsclassify.badass(txt)

Calls ``mitnewsclassify.quadsemble.gettags``.

**Parameters**
    * txt (``string``) - The article text

**Returns**
    * tags (``List[str]``) - The predicted tags