# WebScraper

## Project implementation steps

## Stages 1-3

1. Provide url of the prodcut ' s opinions page.
2. Send request to provided url.
3. Fetch prodcut name.
4. Fetch all opinions from the webpage.
5. Parse opinions to extract required data.
6. Check if there is next page with opinions.
7. Repeat steps 4-6 for all pages with opinions about product.
8. Save acquired opinions.

## Project inputs
## Product codes
1. Mysz satechi M1 silver | https://www.ceneo.pl/84869312 
2. LEGO City 60337 Ekspresowy pociąg pasażerski | https://www.ceneo.pl/133523566
3. Urządzenie wielofunkcyjne Canon PIXMA G3410 MegaTank (2315C009) | https://www.ceneo.pl/61030169
4. DeWalt DCMPP568N-XJ | https://www.ceneo.pl/141797721
5. Garmin Instinct 2X Solar Grafitowy (010-02805-00) | https://www.ceneo.pl/151557603

### Opinion structure
|component|name|selector|
|---------|----|--------|
|opinion ID|opinion_id|[data-entry-id]|
|opinion’s author|author|span.user-post__author-name|
|author’s recommendation|recomendation|span.user-post__author-recomendation > em|
|score expressed in number of stars|score|span.user-post__score-count|
|opinion’s content|content|"div.user-post__text"|
|list of product advantages|pros|div.review-feature__item--positive|
|list of product disadvantages|cons|div.review-feature__item--negative|
|how many users think that opinion was helpful|helpful|button.vote-yes > span|
|how many users think that opinion was unhelpful|unhelpful|button.vote-no > span|
|publishing date|publish_date|span.user-post__published > time:nth-child(1)[datetime]|
|purchase date|purchase_date|span.user-post__published > time:nth-child(2)[datetime]|