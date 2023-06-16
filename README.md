<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Girekomenda nga i-install una ang nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , ug dayon `direnv allow` pagkahuman sa pagsulod sa direktoryo ( [ang .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) awtomatik nga ipatuman pagkahuman sa pagsulod sa direktoryo).

Ang kahulogan mao ang: Intsik nga hubad sa Japanese, Korean, English, English nga hubad sa tanan nga ubang mga pinulongan. Kung gusto nimo nga suportahan ang Intsik ug English, mahimo nimo isulat `zh: en` .

Ang kahulogan mao ang: Intsik nga hubad sa Japanese, Korean, English, English nga hubad sa tanang ubang mga pinulongan. Kung gusto lang nimo suportahan ang Intsik ug English, mahimo nimong isulat `zh: en` .

* [front-end nga code](https://github.com/xxai-art/web)
* [Language pack para sa site sa kinatibuk-an](https://github.com/xxai-art/web/tree/main/i18n)
* [Mga pakete sa pinulongan para sa mga module sa pag-login](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Website nga Multilingual nga Dokumentasyon](https://github.com/xxai-doc)

Ang front-end programming language mao [ang @w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , nga nagdugang sa pipila ka mga feature base sa coffeescript syntax, tan-awa ang [./coffee_plus.md](./coffee_plus.md) .

## Internasyonalisasyon sa mga website ug mga dokumento

Pagtukod sa mosunod nga 3 ka proyekto

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Ang suffix mao ang `.mdt` , mahimo nimong gamiton ang syntax nga susama sa `<+ ./coffee_plus/import.js>` para mag-refer sa external files, ug makamugna og markdown gamit ang suffix `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Ang paghubad sa Markdown dili maghubad sa mga code ug mga link, ug mag-cache sa gihubad nga mga tudling-pulong. Kung ang hubad giusab apan ang orihinal nga teksto wala gibag-o, ang pagpatuman niini pag-usab dili mag-overwrite sa pagbag-o sa hubad.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Mga file sa pinulongan para sa paghubad `yaml` nga mga website.

### Mga Instruksyon sa Automation sa Paghubad sa Dokumento

Tan-awa ang code repository [xxai-art/doc](https://github.com/xxai-art/doc)

Girekomenda nga i-install una ang nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , ug dayon `direnv allow` pagkahuman sa pagsulod sa direktoryo ( [ang .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) awtomatik nga ipatuman pagkahuman sa pagsulod sa direktoryo).

Aron malikayan ang dako nga base sa code nga gihubad ngadto sa gatusan ka mga pinulongan, naghimo ako og usa ka bulag nga base sa code alang sa matag pinulongan ug naghimo og usa ka organisasyon aron tipigan ang code base

Ang pagbutang sa environment variable `GITHUB_ACCESS_TOKEN` ug dayon pagpadagan [sa create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) awtomatik nga maghimo sa code repository.

Siyempre, mahimo usab nimo kini ibutang sa base sa code.

Reperensya sa script sa paghubad [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Ang script code gihubad ingon sa mosunod:

[Ang bunx](https://bun.sh/docs/cli/bunx) usa ka kapuli sa npx, nga mas paspas. Siyempre, kung wala ka naka-install nga bun, mahimo nimong gamiton `npx` .

`bunx mdt zh` naghubad `.mdt` sa zh directory isip `.md` , tan-awa ang 2 ka linked files sa ubos

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` mao ang kinauyokan nga kodigo alang sa paghubad (kung na-install lang `nodejs` , apan wala ma-install `bun` ug `direnv` , mahimo usab nimo nga ipadagan `npx i18n` aron mahubad).

Kini mag-parse [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , ang configuration sa `i18n.yml` niini nga dokumento mao ang mosunod:

```
en:
zh: ja ko en
```

Ang kahulogan mao ang: Intsik nga hubad sa Japanese, Korean, English, English nga hubad sa tanan nga ubang mga pinulongan. Kung gusto nimo nga suportahan ang Intsik ug English, mahimo nimo isulat `zh: en` .

Ang katapusan mao [ang gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , nga nagkuha sa sulod tali sa nag-unang titulo ug sa unang subtitle sa `README.md` sa matag pinulongan aron makamugna og entry `README.md` . Ang code yano ra kaayo, mahimo nimong tan-awon kini sa imong kaugalingon.

Ang Google API gigamit alang sa libre nga paghubad. Kung dili ka maka-access sa Google, palihug i-configure ug itakda ang proxy, sama sa:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Ang script sa paghubad maghimo ug gihubad nga cache sa `.i18n` nga direktoryo, palihug susiha kini sa `git status` ug idugang kini sa code repository aron malikayan ang balikbalik nga paghubad.

Palihug pagdagan `bunx i18n` matag higayon nga imong usbon ang hubad aron ma-update ang cache.

Kung ang orihinal nga teksto ug ang paghubad giusab sa parehas nga oras, ang cache malibog, busa kung gusto nimo nga usbon, mahimo ra nimo usbon ang usa, ug dayon pagdagan `bunx i18n` aron ma-update ang cache.
