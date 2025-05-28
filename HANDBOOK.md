# Flag 1

Úkolem je napsat url podle těchto instrukcí.

|protokol | doména     | port | cesta                   | dotaz      |
|---------|------------|------|-------------------------|------------|
|HTTPS |    vsechno.cz | 443 | hracky/auto-na-ovladani | barva=modra |

**Výsledek vypadá takto:**
```
https://www.vsechno.cz/hracky/auto-na-ovladani?barva=modra
```
**Výsledeek v haxagon formatu:**
```
haxagon{https://www.vsechno.cz/hracky/auto-na-ovladani?barva=modra}
```

# Flag 2

Úkolem je zakodovat url pomocí url-encodingu dá se to přepsat ručně, ale doporučuji použít online nástroj.

**Výsledek vypadá takto:**
```
https://haxagon.xyz/pro%C4%8D%20mi%20to%20nefunguje
```
**Výsledeek v haxagon formatu:**
```
haxagon{https://haxagon.xyz/pro%C4%8D%20mi%20to%20nefunguje}
```
# Flag 3

Úkolem je poznat, že se jedná o base64 a pomocí nějakého online nástroje z toho udělat obrázek na kterém je zobrazena vlajka.

**Vlajka na obrázku:**
```
haxagon{skibidy_base_64}
```
