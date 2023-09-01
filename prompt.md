Generate a webpage

Localization:

- Selected language: en
- Supported languages: en, es, cs

Data (en | es | cs):

- Title: Take your space | Gana tu espacio | Vzít si prostor
- Description: Mexican graffiti and urban art | Grafiti & Arte urbano mexicano | Graffiti & pouliční umění Mexika
- Trailer URL: https://youtu.be/-MFLoG6FGuw | https://youtu.be/aZEsKBo_-Zs | https://youtu.be/g9z8c1FoblA

Content:

- Localized top header image `header`
  - Use `<data.title> | <data.description>` as alternative text
  - Scale to full viewport width
  - Responsive sizes 640w and 1008w and 1920w
  - Add 3% vertical margin at bottom
- Playable YouTube trailer
  - Scale iframe to full viewport width with aspect ratio 16:9
- Footer:
  - Social links:
    - Facebook: https://facebook.com/ganatuespaciodoc
      - Use white on facebook blue with 5% rounded corners and small padding
  - Language switcher:
    - Lower case list of supported language selectors
      - Each has horizontal margin 1em
      - Separated with dark gray `|`
      - Current language is not a link, other languages link to localized pages

Page style:

- 1 column, vertically centered content, no margins
- Font family: Tahoma, sans-serif
- Colors:
  - Background: black
  - Text: gray tone having contrast ratio of 4.5 on background

Page properties:

- Localization:
  - Language selectors: english, español, česky
  - Localized page URLs: `/` for en, `/<code>` for any other supported language
  - Localized images: `.<language>` is appended to image name (as a first name modifier)
  - On page load, the language is determined from language code in URL, cookie `locale` and browser language
    - Not supported languages are ignored
    - If default language is detected, we're ok
    - If any other supported language is detected, page switches to that language
  - After switching language the selected language code is stored in cookie `locale`
    and page is redirected to the localized version
- Meta:
  - Title: `data.title`
  - Description: `data.description`
  - Favicons: 180x180 apple touch PNG icon and 16x16 + 32x32 PNG favicons located in /
  - Manifest: site.webmanifest
  - Theme and MS tile color: #111
  - Open Graph:
    - Title: `data.title`
    - Description: `data.description`
    - Link 1200x630 + 630x630 preview images `/images/preview.<language>.<width>x<height>.jpg`
- Assets:
  - Naming: use lowercase, separate words with dashes
  - Image location: /images
  - Image type: WebP with fallback to JPEG
  - Responsive images: `.<width>` is appended to image name (as a last name modifier)

Code style:

- Minify the page

Hints:

- To set iframe aspect ratio, set parent container CSS properties width and aspect ratio, and set iframe HTML attributes width and height to 100%
- Aspect ratio property needs space around `/` operator
- For non-responsive image type fallback use `picture` tag with `img` tag fallback containing fallback format
- For responsive image type fallback use `picture` tag with:
  - `source` for each image type with:
    - `srcset` for all image resolutions
  - `img` tag with:
    - `src` linking the fallback type
    - `srcset` for all image resolutions in the fallback type

Output:

- Check if the generated page ends with `</html>`, if not then finish generating the page
  - Repeat until the check succeeds
- Write `Done` after you finish generating the code
