<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Kabahin sa code sa website kay open source, welcome sa pagtabang sa pag-optimize sa translation.

## front-end nga code

* [front-end nga code](https://github.com/xxai-art/web)
* [Language pack para sa site sa kinatibuk-an](https://github.com/xxai-art/web/tree/main/i18n)
* [Mga pakete sa pinulongan para sa mga module sa pag-login](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Multilingual nga Dokumentasyon sa Website](https://github.com/xxai-doc)

Ang front-end programming language mao [ang @w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , nga nagdugang sa pipila ka mga feature base sa coffeescript syntax, tan-awa ang [./coffee_plus.md](./coffee_plus.md) .

## Internasyonalisasyon sa mga website ug mga dokumento

Pagtukod sa mosunod nga 3 ka proyekto

### [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

Ang markdown template, nga adunay suffix `.mdt` , mahimong magtumong sa external files nga adunay syntax nga susama sa `<+ ./coffee_plus/import.js>` .

[@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

Ang paghubad sa Markdown dili maghubad sa mga code ug mga link, ug mag-cache sa gihubad nga mga tudling-pulong. Kung ang hubad giusab apan ang orihinal nga teksto wala gibag-o, ang pagpatuman niini pag-usab dili mag-overwrite sa pagbag-o sa hubad.

[@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

Mga file sa pinulongan para sa paghubad `yaml` nga mga website.
