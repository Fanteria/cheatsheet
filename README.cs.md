# Markdown cheat sheet

Tex je také dostupný v [angličtině](README.md).

Tento text je shrnutí syntaxu pro jayk Makrdown, jelikož některé věci, které nepoužívám moc často pravidelně zapomínám, tak jsem si je sepsal. Nadpisy označené kurzívou nejsou součástí základní definice Markdownu a mohou tedy na méně pokročilých platformách pro markdown zůstávat v původním tvaru. Bez toho, aby vytvořili požadovanou grafiku. Na závěr souboru jsou ještě zmíněná některá rošiření, která do markdownu přidává rozšíření [markdown preview enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/), které je dostupné pro [Atom](https://atom.io) [VS Code](https://code.visualstudio.com).

__TOC__
1. [Nadpisy](#titles)
2. [Odstavce](#paragraphs)
3. [Seznamy](#lists)
4. [Tabulky](#tables)
5. [Reference](#references)
6. [_Kód_](#code)
7. [_Emotikony_](#Emotes)

## Nadpisy <a name="titles"></a>
Stejně jako html má i markdown šest úrovní nadpisů.

```
# Nadpis 1. úrovně
## Nadpis 2. úrovně
### Nadpis 3. úrovně
#### Nadpis 4. úrovně
##### Nadpis 5. úrovně
###### Nadpis 6. úrovně
```

Pro nadpis první a druhé úrovně je i alternativní zápis.

```
Nadpis 1. úrovně
=======

Nadpis 2. úrovně
-------
```

## Odstavce <a name="paragraphs"></a>

### Zvýraznění
Markdown obsahuje čtyři druhy zvýraznění textu kurzívu, tečné písmo, přeškrtnuté písmo a blokové citace. Nemá však syntaxi pro písmo podtržené.

#### Kurzíva
Je nutné, aby za znakem `*` nebo `_` nebyla mezera.
```
*první text kurzivou*
_druhý text kurzivou_
```
*první text kurzivou*
_druhý text kurzivou_

#### Tučné písmo
Stejně jako u kurzivy je nutné, aby za znakem `*` nebo `_` nebyla mezera a je nutné aby oba znaky byli stejné.
```
**první text tučným písmem**
__druhý text tučným písmem__
```
**první text tučným písmem**
__druhý text tučným písmem__

#### _Přeškrtnutí_
Přeškrtnutý text je možno v markdownu udělat pomocí párového tagu `~~`

```
~~Přeškrtnutý text~~
```

~~Přeškrtnutý text~~

#### Blokové citace
Blokové citace se vytváří pomocí znaku `>`.

```
> Bloková citace
```

> Bloková citace

Je také je možné je libovolně zanořovat.

```
> Bloková citace
> > Zanořená bloková citace
```

> Bloková citace
> > Zanořená bloková citace



## Seznamy <a name="lists"></a>
Seznamy jsou uspořádané množiny položek a je možné do sebe jednotlivé položky vnořovat pomocí odsazení jednotlivých položek.

```
- položka
    - položka
        1. položka
        2. položka
    - položka
```

- položka
    - položka
        1. položka
        2. položka
    - položka

#### Číslované seznamy
Číslovaný seznam je možné vytvořit pomocí čísla, tečky a mezery.

```
1. první položka
2. druhá položka
3. třetí položka
```

1. první položka
2. druhá položka
3. třetí položka

Je také možné použít libovolná čísla v libovolném pořadí a markdown zachová číslování.

```
1. první položka
1. druhá položka
123. třetí položka
1. čtvrtá položka
```

1. první položka
1. druhá položka
123. třetí položka
1. čtvrtá položka


#### Nečíslované seznamy

Nečíslované seznamy je možné vytvářet pomocí znaků `-`, `+`, `*` a následné mezery.

```
- položka
+ položka
* položka
```

- položka
+ položka
* položka

#### Seznam úkolů
Seznam úkolů je možné vytvořit stejným způsobem jako jakýkoliv jiný seznam, jen se za něj přidají hranaté závorky, mez kterými bude mezera pro nesplněnou položku a `x` (_bez ohledu na velikost_) pro položku splněnou.
```
- [ ] nečíslovaná nesplněná položka
- [x] nečíslovaná splněná položka

1. [ ] číslovaná nesplněná položka
1. [X] číslovaná splněná položka
```

- [ ] nečíslovaná nesplněná položka
- [x] nečíslovaná splněná položka

1. [ ] číslovaná nesplněná položka
1. [X] číslovaná splněná položka



## Tabulky <a name="tables"></a>
Tabulky je možné vytvářet pomocí `|`, které oddělují jednotlivé sloupce a `-`, které oddělují hlavičku tabulky od zbytku. Také je možné měnit zarovnání tabulky v oddělení hlavičky pomocí `:` tak jak je to vidět v příkladu.

| Hlavička      |      Tabulky      | Příkladu |
| ------------- |:-----------------:| --------:|
| první sloupec |   je zarovnaný    |  do leva |
| druhý sloupec | má text zarovnaný | na střed |
| třetí sloupec |   je zarovnaný    |  v pravo |

Není však nutné držet přísné zarovnání, markdown si s tím i tak poradí.

Horší | Zarovnání | Také funguje
--- | --- | ---
*do tabulek je samozřejmě* | `možné vkládat` | **i formátovaný text**
3 | 3 | 3

## Reference <a name="references"></a>

#### _Zmínky_
Na githubu popřípadě jiných stránkách je možné vkládat do textu odkazy na ostatní uživatele pomocí `@nick`. Využívá se toho například diskuzích nebo při hlášení chyb.

#### _Detail_
Vytvoření tzv. detailu. Jedná se o text, který je nejprve skrytý a je ho možné kliknutím rozblit. Tato vlastnost není obsažena v jazyce markdown, je tedy nutné využít html.

```html
<details>
    <summary>Detail</summary>
    Informace v detailu.
</details>
```

<details>
    <summary>Detail</summary>
    Informace v detailu.
</details>

#### Odkazy <a name="links"></a>

Odkazy je možné v markdownu tvořit pomocí kombinace `[]` obsahujících text, který se zobrazí a `()` obsahujících adresu.

```
[Odkaz na google](https://www.google.com)
```

[Odkaz na google](https://www.google.com)

Zároveň je možné možné k odkazům také vkládat poznámky, které se objeví po najetí kurzoru na odkaz. Poznámku je nutné dát do `""` za adresu.

```
[Duck duck go je taky super](https://duckduckgo.com "A nepersonalizuje data.")
```

[Duck duck go je taky super](https://duckduckgo.com "A nepersonalizuje data.")

Ještě je možnost použít návěští a mít skutečný odkaz kdekoliv dál. Pak se návěští dává do `[]` a při jeho pozdějším definování se adresa odděluje pomocí `:`.

```
[Bing][1]
[Yahoo][Dokonce nezalezi na velikosti pismen ani mezerach]

Jakákoliv text meztím.

[1]: https://www.bing.com
[Dokonce Nezalezi Na Velikosti Pismen Ani Mezerach]: https://consent.yahoo.com
```

[Bing][1]
[Yahoo][dokonce nezalezi na velikosti pismen ani mezerach]

[1]: https://www.bing.com
[Dokonce nezalezi na velikosti pismen ani mezerach]: https://consent.yahoo.com

V markdownu není funkcionalita pro generování obsahu, je však možné využít odkazování se části souboru. Část na kterou je možné odkazovat se vytvoří pomocí

```html
<a name="links"></a>
```

Na tuto část je možné se následně odkazovat pomocí běžného odkazu `[Odkazy](#links)`, což vytvoží běžný odkaz viz [Odkazy](#links).

#### Obrázky
Obrázky se vkládají podobně jako odkazy, je však nutné před `[]` dát `!`.

![Text v případě nenačtení obrázku](https://www.neexistující_adresa.cz)
![](https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)

#### Videa
Vkládání videí do markdownu není podporováno, je sice možné vložit ho pomocí kombinace odkazu a obrázku.

```
[![Obrázek se nenačetl](ADRESA_OBRAZKU)](ADRESA_VIDEA)
```

Je však mnohem spolehlivější vložit ho pomocí html.

```
<a href="http://www.youtube.com/watch?feature=player_embedded&v=ID_VIDEA_NA_YOUTUBE" target="_blank">
<img src="http://img.youtube.com/vi/ID_VIDEA_NA_YOUTUBE/0.jpg"
alt="Obrázek nenalezen" width="240" height="180" border="3" />
</a>
```

<a href="http://www.youtube.com/watch?feature=player_embedded&v=_bYFu9mBnr4" target="blank">
<img src="http://img.youtube.com/vi/_bYFu9mBnr4/0.jpg" alt="Obrázek nenalezen" width="240" height="180" border="3" />
</a>

#### Audio
Stejně jako pro video ani pro audio nemá markdown pro audio podporu. Zde bych však doporučoval html kód

```
<audio controls="controls">
  <source type="audio/mp3" src="filename.mp3"></source>
  <source type="audio/ogg" src="filename.ogg"></source>
  <p>Your browser does not support the audio element.</p>
</audio>
```

## _Kód_ <a name="code"></a>
Markdown umožňuje snadné vlkádání kódu programů pomocí ` `` `.

#### _Řádkový_
Pokud chceme mít kód vložený oprostřed řádky, pak mezi direktivu ` `` ` se vloží příslušný kód.
```
`std::cout << "Hello world." << std::endl;`
```

Kód `std::cout << "Hello world." << std::endl;` nám vypíše do standartního výstupu "Hello world." a odřádkuje.

#### _Blokový_
Místo jednoduchého ` `` ` je tato direktiva vložena třikrát. Navíc je možné nastavit jméno jazyku a tak zajistit správné zvýraznění.

<pre><code>
```c++
#include <iostream>

int main()
{
    std::cout << "Hello world." << std::endl;
    return 0;
}
```
</code></pre>

```c++
#include <iostream>

int main()
{
    std::cout << "Hello world." << std::endl;
    return 0;
}
```

## _Emotikony_ <a name="Emotes"></a>
Markdown umí používat i základní sadu emotikonů a to pomocí kódu emotikonu a `:`

```
:smile:
```

:smile:

Seznam emotikonů je množné najít [zde](https://www.webfx.com/tools/emoji-cheat-sheet/).
