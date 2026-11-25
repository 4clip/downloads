# Airo · site e downloads

**Português.** Este repositório publica o site do Airo, switcher de vídeo ao vivo para igrejas, em
<https://airo-app.github.io>, e guarda nas [releases](https://github.com/airo-app/airo-app.github.io/releases)
os instaladores públicos.

**English.** This repository hosts the Airo website, a live video switcher for churches, at
<https://airo-app.github.io>, and holds the public installers in its
[releases](https://github.com/airo-app/airo-app.github.io/releases).

## Downloads

| Sistema / System | Arquivo / File | Requisitos / Requirements |
| --- | --- | --- |
| macOS | [Airo-macOS-arm64.dmg](https://github.com/airo-app/airo-app.github.io/releases/latest/download/Airo-macOS-arm64.dmg) | macOS 13+, Apple Silicon |
| Windows | [Airo-Windows-x64.zip](https://github.com/airo-app/airo-app.github.io/releases/latest/download/Airo-Windows-x64.zip) | Windows 10/11, x64 |
| Linux | [Airo-Linux-x86_64.AppImage](https://github.com/airo-app/airo-app.github.io/releases/latest/download/Airo-Linux-x86_64.AppImage) | Linux x86_64 |

Os links acima apontam sempre para a versão mais recente.
The links above always point to the latest version.

## Estrutura / Layout

Tudo é HTML, CSS e JS sem build. / Plain HTML, CSS and JS, no build step.

- `index.html`: a página inicial. O português está no HTML; o inglês, no dicionário `AIRO_EN` do
  próprio arquivo (abra com `?i18n-debug` e rode `airoMissingTranslations()` para ver o que falta).
  / The home page. Portuguese lives in the HTML, English in the `AIRO_EN` dictionary in the same file.
- `docs.html`: a documentação da API, com os dois idiomas no HTML (`data-l="pt"` e `data-l="en"`).
  / The API documentation, with both languages in the HTML.
- `assets/site.css`: o estilo comum às páginas (cores, navegação, rodapé). / Styles shared by the pages.
- `img/`: capturas do app, ícones e as fotos das cenas de exemplo. / App screenshots, icons and the sample scene photos.
- `404.html`, `favicon.svg`, `.nojekyll`.

As páginas guardam a escolha de idioma em `localStorage` (`airo-site-lang`); sem escolha, seguem o
idioma do navegador. `?lang=pt` ou `?lang=en` no endereço força um idioma.
The pages remember the language in `localStorage`; otherwise they follow the browser language.

## Créditos das fotos / Photo credits

As fotos `img/cena-*.jpg` são do [Unsplash](https://unsplash.com), sob a
[Licença Unsplash](https://unsplash.com/license) (uso livre, inclusive comercial), recortadas em 1280×720.
The `img/cena-*.jpg` photos come from Unsplash under the Unsplash License, cropped to 1280×720.

| Arquivo / File | Foto / Photo | Fotógrafo / Photographer |
| --- | --- | --- |
| `cena-pulpito.jpg` | [pHb0Ztr2CFE](https://unsplash.com/photos/pHb0Ztr2CFE) | Thiago BF |
| `cena-geral.jpg` | [x08J-q2Lv-o](https://unsplash.com/photos/x08J-q2Lv-o) | AMONWAT DUMKRUT |
| `cena-louvor.jpg` | [9nR_eUa8PNU](https://unsplash.com/photos/9nR_eUa8PNU) | Liana S |
| `cena-avisos.jpg` | [7KhbREQPFD4](https://unsplash.com/photos/7KhbREQPFD4) | Erika Giraud |
| `cena-pregador.jpg` | [EUUCzZ-eMVI](https://unsplash.com/photos/EUUCzZ-eMVI) | AMONWAT DUMKRUT |

O código do aplicativo fica num repositório privado; as releases daqui são cópias das de lá.
The app's source lives in a private repository; the releases here are copies of the ones there.
