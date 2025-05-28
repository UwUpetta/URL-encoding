
# 📚 Teorie o enkódování dat

Enkódování (neboli kódování) je proces převodu dat z jednoho formátu do jiného za účelem jejich uchování, přenosu nebo zajištění kompatibility mezi různými systémy. Existuje mnoho typů enkódování v závislosti na použití. Níže jsou vysvětleny některé běžné formáty.

---

## 🌐 URL Encoding (Percent Encoding)

Používá se pro zakódování speciálních znaků v URL adresách, které by jinak měly speciální význam (např. `?`, `&`, `=`, mezery atd.).

- Nealfanumerické znaky se nahrazují procentem (`%`) následovaným dvěma hexadecimálními číslicemi.
- Např. mezera (` `) se zakóduje jako `%20` nebo jako `+` (v některých případech).

**Příklad:**

```
https://example.com/search?q=hello world
```

Zakódováno jako:

```
https://example.com/search?q=hello%20world
```

---

## 🔤 Unicode

Unicode je standard pro reprezentaci znaků z většiny světových jazyků.

- Každý znak má jedinečný kódový bod (např. `U+0041` pro `A`).
- Unicode může být reprezentován v různých formátech jako UTF-8, UTF-16, UTF-32.
- UTF-8 je nejčastěji používané zakódování – používá proměnný počet bajtů (1 až 4).
- Unicode se používá i pro reprezentaci **emoji** (např. 😀 = `U+1F600`).

**Příklad:**

- Znak `č` má kódový bod `U+010D`
- V UTF-8: `0xC4 0x8D`
- Emoji `🚀` → `U+1F680`

---

## 🔢 Hexadecimální kódování (Hex)

Zobrazuje binární data jako řetězec hexadecimálních (základ 16) číslic.

- Každý bajt (8 bitů) je zobrazen jako dvě hexadecimální číslice.
- Často se používá při zobrazení binárních souborů nebo hashů (např. MD5, SHA).

**Příklad:**

- Text: `Hi`
- ASCII: `H = 72`, `i = 105`
- Hex: `48 69`

---

## 📦 Base64 Encoding

Používá se pro převod binárních dat na text, zejména při přenosu přes protokoly, které nejsou binárně bezpečné (např. e-mail, JSON).

- Zakódovává každé 3 bajty do 4 znaků z abecedy (A–Z, a–z, 0–9, +, /).
- Výstupní délka je vždy násobkem 4, **doplňuje se pomocí znaků `=`**.
- **Base64 se často používá pro zakódování obrázků** nebo jiných binárních dat, např. při vložení obrázku do HTML nebo CSS.
- **Také se používá pro zobrazení obrázků přímo v URL**, např. při generování QR kódů nebo v data URI schématu.

**Příklad:**

- Text: `Man`
- ASCII: `M = 77`, `a = 97`, `n = 110`
- Binárně: `01001101 01100001 01101110`
- Rozdělení: `010011 010110 000101 101110`
- Base64: `TWFu`

**Příklad použití v HTML:**

```html
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAA..." />
```

**Příklad v URL:**

```
data:image/jpeg;base64,/9j/4AAQSkZJRgABAQE...
```

---

## 🧠 Shrnutí

| Formát       | Použití                                       | Příklad                                  |
|--------------|------------------------------------------------|------------------------------------------|
| URL Encoding | Bezpečný přenos dat v URL                      | `hello world` → `hello%20world`          |
| Unicode      | Reprezentace globálních znaků a emoji          | `🚀` → `U+1F680` (UTF-8: `F0 9F 9A 80`)   |
| Hex          | Zobrazení binárních dat                        | `Hi` → `48 69`                           |
| Base64       | Textová reprezentace binárních dat, obrázky    | `Man` → `TWFu`, obrázky v HTML/URL       |
